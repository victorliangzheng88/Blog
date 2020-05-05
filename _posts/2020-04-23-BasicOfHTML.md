---
layout: post
title: "Basic of HTML"
date: 2020-04-23 12:00:00 -0500
---

HTML is called Hyper Text Markup Language. HTML is not a programming language, but a markup language, which is essential for making web pages. Hypertext means that a page can contain pictures, links, and even non-text elements such as music and apps. The structure of a hypertext markup language consists of a "head" section that provides information about a web page, and a "body" section that provides the specific content of a web page. Let me start with an example of the structure of the HTML code:

```sh
<!DOCTYPE html>
<html>
	<head>
		<title>	HTML Example </title>
	</head>
	<body>
		<h1>
			HTML Example
		</h1>
		<a href="https://victorliangzheng88.github.io/Blogs/">My Blog</a>
		<br/>
		<p>
			Hi, There!
		</p>
		<img src="WOW.jpg"/>
	</body>
</html>
```

<!DOCTYPE html> declares that this HTML file is an html5 document. Because HTML is a markup language, so it uses a lot of tags and that each tag has a start tag and an end tag. For example, the start tag would something like <html> and an end tag of it would be </html>. You just need to add a “/” in addition to the start tag. HTML code is built on tags, each of which is called an element. Where < HTML > is the root element of an HTML page, the structure of hypertext markup language includes the "head" part, and the "body" part, where the "head" part provides information about the page, the "body" part provides the specific content of the page. <title> is used to define the title of the page. <body></body> is used to define the content of the page. For that, <h1>~<h6> is used to define the size of the heading. There are six levels of heading, just like we have subheadings when we're writing a document, it's all about font sizes, h1 is the largest, and it decreases as the number increase. <a> is used to define links, where the href is the address of the link. content between <a></a> is displayed on the web page with links text content; <br/> is a blank element and is used to break lines.  <p> tags are used to display paragraphs for the page. <img> is used to display the image, where src is the path of the image, which can be a relative path or an absolute path. These are the very basic elements in HTML. I’ve also created a website to demonstrate my portfolio. If interested, you can visit my Github page (https://github.com/victorliangzheng88/victorliangzheng88.github.io) for more information and the webpage that I’ve created is https://victorliangzheng88.github.io.
