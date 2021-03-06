# Markdown-Region

APEX Region Plugin  MarkDown Display. Support code highlight, MathJax, [TOC], anchor,video and audio,sequence diagrams.demo is available [here](https://apex.oracle.com/pls/apex/group/r/demo78/home)

# Features

- converting static Markdown to the HTML
- support code highlight
- support [MathJax](https://www.mathjax.org/)
- support catalog ``[TOC]`` and anchor
- support video/audio
- support sequence diagrams
- easily customizable with JavaScript Initialization Code attribute

# DEMO

demo is available [here](https://apex.oracle.com/pls/apex/group/r/demo78/home)

# Install

Import plugin file **region_type_plugin_com_tjfish_apex_markdownregion.sql** from source directory. 

# Settings

**highlight style** 

You can change the default style for code highlight. The support style are list

- androidstudio
- dark
- default
- github
- github-gist
- lightfair
- vs2015
- xcode

**Showdown-options**

You can customize region with additional parameters by using Initialization Code attribute. Additional options are available here: <https://github.com/showdownjs/showdown/wiki/Showdown-options>.

Example of Initialization Code attribute:

```
function (options){
  options.literalMidWordUnderscores = false;
  options.noHeaderId = true;
  return options;
}
```

# Usage

- Create Region ***Markdown Region***

- Put Markdown code into the static source of the region.
- Run and see it

![usage](./img/usage.png)



# Notes

This plugin is based on https://github.com/mgoricki/apex-plugin-markdown-region. If you want to kown more [see this](https://github.com/mgoricki/apex-plugin-markdown-region)

The used syntax highlighter is [highlight.js](https://highlightjs.org/) with the default set of 32 common languages: Apache, Bash, C#, C++, CSS, CoffeeScript, Diff, HTML-XML, HTTP, Ini, JSON, Java, JavaScript, Makefile, Markdown, Nginx, Objective-C, PHP, Perl, Python, Ruby, SQL .....

If you need more or other languages (189 available) then you can create your custom highlight.js package, rename it to the same file name used in the plugin and upload it to the plugin files. you can also add your css styles by the way