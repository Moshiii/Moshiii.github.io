https://arxiv.org/pdf/1805.05236.pdf

## existing industrial and open-source tools:
QiHoo360 [17], AndroBugs [2], MobSF [13], and QARK [16].

## SOTA limitations

* current studies lack a baseline of sensitive datarelated security weaknesses specific to the core functionality of banking apps to ensure an overall assessment of these apps; 

* the current off-the-shelf services (e.g., Qihoo360 [17]) and open-source tools (e.g., AndroBugs [2]) use syntax-based scanning to perform a security check during app development, which would incur a large number of false positives (e.g., non-sensitive data printed in the log file). 

* Besides, these tools focus on generic categories of apps, not specific to banking apps. 

Even when the weaknesses, such as cryptographic misuses [42] and inappropriate SSL/TLS implementations [40, 45, 51, 65], have been reported for years, it still appears unknown why so many security weaknesses in banking apps are not yet patched [63].


## steps
we first collect 693 banking apps across 83 countries. by applying Ausera, we collected 2,157 security weaknesses in the 693 banking apps.

1. Sensitive data tagging.
2. Function identification.
3. Security weakness detection.

## Implementation of AUSERA

* static program analysis and sensitive data tagging to identify sensitive data and associate them with the corresponding variables in XML/Java code
* Ausera relies on Apktool
* uses partsof-speech (POS) tagger of OpenNLP-1.8.3 [19] to parse the text labels in TextView and EditText,
* (???this is the core of AUSERA and its manual???)manually check on these keywords to retain the ones that are sensitive and relevant to the core functionalities of banking apps
* We employ Word2vec to supplement the keyword

* summarize 12 groups of patterns (e.g., AES/ECB/NoPanding) to depict the communication weaknesses.
* use pattern-based static analysis to find the possible vulnerable patterns in code
* check three aspects for certificate authentication: whether the client side 
1. allows all hostname requests; 
2. bypasses hostname verification; 
3. fails to implement anything in the server verification method (checkServerTrusted).

## RQ
* RQ1: What is the current status of existing tools towards
collecting reliable data-related weaknesses in banking apps
compared with Ausera?

* RQ2: What is the overall security status of banking apps in
terms of data-related weaknesses?

* RQ3: What is the weakness status of banking apps globally
w.r.t. economies and regulations?

* RQ4: How are weaknesses introduced during app evolution
and fragmentation?

* RQ5: What is the gap between academic researchers and
banks in understanding and fixing weaknesses?

## related works

Security assessment of banking apps. In 2015, Reaves et al.
Global analysis of banking apps. Castle et al.
Security analysis of Android apps. TaintDroid, FlowDroid IccTA

## Take away

* Note that, to avoid missing variants of the keywords, we
further employ Word2vec [57] to supplement the corpus of the
keyword database.
