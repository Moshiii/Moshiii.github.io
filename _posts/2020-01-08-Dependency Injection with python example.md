# Overview

Dependency Injection(DI) is a software engineering technique for defining the dependencies among objects. Basically, the process of supplying a resource that a given piece of code requires. The required resource is called dependency.
There are various classes and objects defined when writing code. Most of the time, these classes depend on other classes in order to fulfill their intended purpose. These classes, or better-used word Components, knows the resources it needs and how to get them. DI handles defining these dependent resources and provides ways to instantiate or create them externally. Dependency Container is used to implement this behavior and holds the map of dependencies for the components.
If object A depends on object B, object A must not create import object B directly. Instead of this, object A must provide a way for injecting object B. The responsibility of object creation and dependency injection are delegated to external code.

# Why use Dependency Injection in your code?

* Flexibility of configurable components — As the components are externally configured, there can be various definitions for a component(Control on application structure).
* Testing Made Easy — Instantiating mock objects and integrating with class definitions is easier.
* High cohesion — Code with reduced module complexity, increased module reusability.
* Minimalistic dependencies — As the dependencies are clearly defined, easier to eliminate/reduce unnecessary dependencies.


# Implementing DI in Python
Dependency Injection in Python is a little different from general static language DI. Python has a microframework library for DI, called dependency_injector. This package has two main entities: containers and providers.
Providers describe how objects are accessed. Containers are simply a collection of providers. The most commonly used provider types are: Singleton, Configuration and Factory.

## Example
Following example demonstrate the usage and implementation of DI in Python. Create a file named email_client.py containing EmailClient class which depends on the config object.

```
class EmailClient(object):
    
    def __init__(self, config):
        self._config = config
        self.connect(self._config)
        
    def connect(self, config):
        # Implement function here
        pass
```

Now to define these above dependencies externally, create new containers.py file. Import the dependency_injector package and classes to be used in DI.

```
from dependency_injector import providers, containers
from email_client import EmailClient
from email_reader import EmailReader
```

Add class Configs to the file. This class is a container with a configuration provider which provides all the configuration objects.

```
class Configs(containers.DeclarativeContainer):
    config = providers.Configuration('config')
    # other configs
```

Add another class Clients. This class is a container defining all kinds of clients. EmailClient is created with a singleton provider, asserting a single instance of this class, and defining its dependency on the config object.

```
class Clients(containers.DeclarativeContainer):
    email_client = providers.Singleton(EmailClient, Configs.config)
    # other clients 
```

The third container is Readers class, defining dependency of EmailReader class on EmailClient class.

```
class Readers(containers.DeclarativeContainer):
    email_reader = providers.Factory(EmailReader, client=Clients.email_client)
    # other readers 
```


In total

```

from dependency_injector import providers, containers
from email_client import EmailClient
from email_reader import EmailReader

class Configs(containers.DeclarativeContainer):
    config = providers.Configuration('config')
    # other configs
    
class Clients(containers.DeclarativeContainer):
    email_client = providers.Singleton(EmailClient, Configs.config)
    # other clients
    
class Readers(containers.DeclarativeContainer):
    email_reader = providers.Factory(EmailReader, client=Clients.email_client)
    # other readers
```

In the main.py file, config object is overridden with a given dictionary object. EmailReader class was instantiated without instantiating EmailClient class in main file, removing the overhead of importing or creating it. That part is taken care of by containers file.


For a working example, please refer [here](https://github.com/shivama205/Dependency-Injection-Python/tree/master).
