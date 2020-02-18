---
permalink: /markdown/
title: "Markdown"
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---

## Locations of key files/directories

* Basic config options: _config.yml
* Top navigation bar config: _data/navigation.yml
* Single pages: _pages/
* Collections of pages are .md or .html files in:
  * _publications/
  * _portfolio/
  * _posts/
  * _teaching/
  * _talks/
* Footer: _includes/footer.html
* Static files (like PDFs): /files/
* Profile image (can set in _config.yml): images/profile.png

<pre>
* Collections of pages are .md or .html files in:
  * _publications/
</pre>

## Tips and hints

* Name a file ".md" to have it render in markdown, name it ".html" to render in HTML.
* Go to the [commit list](https://github.com/academicpages/academicpages.github.io/commits/master) (on your repo) to find the last version Github built with Jekyll. 
  * Green check: successful build
  * Orange circle: building
  * Red X: error
  * No icon: not built

## Resources
 * [Liquid syntax guide](https://shopify.github.io/liquid/tags/control-flow/)
<pre>
 * [Liquid syntax guide](https://shopify.github.io/liquid/tags/control-flow/)
</pre>
## Markdown guide

### Header three

<pre>
### Header three
</pre>

#### Header four

<pre>
#### Header four
</pre>

##### Header five

<pre>
##### Header five
</pre>

###### Header six

<pre>
###### Header six
</pre>

## Blockquotes

Single line blockquote:

> Quotes are cool.
<pre>
> Quotes are cool.
</pre>
## Tables

### Table 1

| Entry            | Item   |                                                              |
| --------         | ------ | ------------------------------------------------------------ |
| [John Doe](#)    | 2016   | Description of the item in the list                          |
| [Jane Doe](#)    | 2019   | Description of the item in the list                          |
| [Doe Doe](#)     | 2022   | Description of the item in the list                          |

<pre>
| Entry            | Item   |                                                              |
| --------         | ------ | ------------------------------------------------------------ |
| [John Doe](#)    | 2016   | Description of the item in the list                          |
| [Jane Doe](#)    | 2019   | Description of the item in the list                          |
| [Doe Doe](#)     | 2022   | Description of the item in the list                          |

</pre>

### Table 2

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|-----------------------------|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=============================|
| Foot1   | Foot2   | Foot3   |

<pre>
| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|-----------------------------|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=============================|
| Foot1   | Foot2   | Foot3   |
</pre>

## Definition Lists

Definition List Title
:   Definition list division.

<pre>
Definition List Title
:   Definition list division.
</pre>

Startup
:   A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.

#dowork
:   Coined by Rob Dyrdek and his personal body guard Christopher "Big Black" Boykins, "Do Work" works as a self motivator, to motivating your friends.

Do It Live
:   I'll let Bill O'Reilly [explain](https://www.youtube.com/watch?v=O_HyZ5aW76c "We'll Do It Live") this one.

## Unordered Lists (Nested)

  * List item one 
      * List item one 
          * List item one
          * List item two
      * List item two
      * List item three
  * List item two
  * List item three
<pre>
  * List item one 
      * List item one 
          * List item one
          * List item two
      * List item two
      * List item three
  * List item two
  * List item three
</pre>

## Ordered List (Nested)

  1. List item one 
      1. List item one 
          1. List item one
          2. List item two
      2. List item two
      3. List item three
  2. List item two
  
<pre>
  1. List item one 
      1. List item one 
          1. List item one
          2. List item two
      2. List item two
      3. List item three
  2. List item two
</pre>

## Buttons

Make any link standout more when applying the `.btn` class.
[Click me](http://www.google.com){: .btn}
## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
[Click me](http://www.google.com){: .notice}

## HTML Tags

### Address Tag

<address>
  1 Infinite Loop<br /> Cupertino, CA 95014<br /> United States
</address>

### Anchor Tag (aka. Link)

This is an example of a [link](http://github.com "Github").

<pre>
This is an example of a [link](http://github.com "Github").
</pre>
### Abbreviation Tag

The abbreviation CSS stands for "Cascading Style Sheets".

*[CSS]: Cascading Style Sheets

<pre>
*[CSS]: Cascading Style Sheets
</pre>
### Cite Tag

"Code is poetry." ---<cite>Automattic</cite>

<pre>
"Code is poetry." ---<cite>Automattic</cite>
</pre>
### Code Tag

You will learn later on in these tests that `word-wrap: break-word;` will be your best friend.

<pre>
You will learn later on in these tests that `word-wrap: break-word;` will be your best friend.
</pre>
### Strike Tag

This tag will let you <strike>strikeout text</strike>.

<pre>
This tag will let you <strike>strikeout text</strike>.
</pre>
### Emphasize Tag

The emphasize tag should _italicize_ text.

<pre>
The emphasize tag should _italicize_ text.
</pre>
### Insert Tag

This tag should denote <ins>inserted</ins> text.

<pre>
This tag should denote <ins>inserted</ins> text.
</pre>

### Keyboard Tag

This scarcely known tag emulates <kbd>keyboard text</kbd>, which is usually styled like the `<code>` tag.

<pre>
This scarcely known tag emulates <kbd>keyboard text</kbd>, which is usually styled like the `<code>` tag.
</pre>

### Preformatted Tag

This tag styles large blocks of code.

<pre>
.post-title {
  margin: 0 0 5px;
  font-weight: bold;
  font-size: 38px;
  line-height: 1.2;
  and here's a line of some really, really, really, really long text, just to see how the PRE tag handles it and to find out how it overflows;
}
</pre>

### Quote Tag

<q>Developers, developers, developers&#8230;</q> &#8211;Steve Ballmer

<pre>
<q>Developers, developers, developers&#8230;</q> &#8211;Steve Ballmer
</pre>
### Strong Tag

This tag shows **bold text**.

<pre>
This tag shows **bold text**.
</pre>

### Subscript Tag

Getting our science styling on with H<sub>2</sub>O, which should push the "2" down.

<pre>
Getting our science styling on with H<sub>2</sub>O, which should push the "2" down.
</pre>

### Superscript Tag

Still sticking with science and Isaac Newton's E = MC<sup>2</sup>, which should lift the 2 up.

<pre>
Still sticking with science and Isaac Newton's E = MC<sup>2</sup>, which should lift the 2 up.
</pre>

### Variable Tag

This allows you to denote <var>variables</var>.

<pre>
This allows you to denote <var>variables</var>.
</pre>
