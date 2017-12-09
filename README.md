# TOC-Generator

## What is it
A simple, ready to use javascript to add auto generated, super customizable Table Of Content to any page element.

## How It Works
The TOC-Generator make use of data-toc attribute to determine its parent element. Then, it select all the <h(n)> tag inside and insert a hierarchically ordered list made out of them to the parent's top. Every tabel of content generated this way has a default id="toc-(nth)", where (nth) is an integer corresponding to the nth generated table, and a default class="toc-default".

The *toc_1.0.0.css* contains some basic styling rules to make the TOC-Generator ready to use but you can customize it the way you like by modifying the file, overriding the *.toc-default* class in an external css, or adding your own class using the [TOC-Generator Options](https://github.com/ALF3run/TOC-Generator/#options) below.

## How To Use
Just put the **js** and **css** directory or their content inside your project root direcotry, then import the *toc_1.0.0.css* and *toc_1.0.0.js* in your .html file. Now the TOC-Generator is ready to use.

In your .html file chose the element you want the table of content generated for and add the attribute **data-toc** to it. For example:
```
<div data-toc>
  <h2>Title 1</h2>
  <h3>Title 2</h3>
  <h2>Title 3</h2>
  <!-- more content -->
</div>
```

## Options
You can modify some aspects of the generated tabel of content by adding the data- attribute below to the same element where **data-toc** is:
1. **data-toc-id** - override the default toc generated id if setted to a not empty value;
2. **data-toc-class** - allow to add any custom class to your generated table of content. It does not override the default *.toc-default* class;
3. **data-toc-header** - override the default toc header with a user defined one. If set to *none* (not case sensitive!) it will remove the header.

## Future Features
- [ ] Custom container: user can set the element wherein the table of content will be appended.
