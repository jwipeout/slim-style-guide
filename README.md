# Slim Style Guide

> So if you want to go fast, if you want to get done quickly, if you want your code to be easy to write, make it easy to read. <br>
> -- Robert Martin, Clean Code


This Slim style guide recommends best practices when using the slim language. Just by choosing to use slim you have demonstrated that you believe in easy to read and maintainable code. This guide is here to help with rules and best practices.

Just like any other language people have different opinions and we welcome them. Fork and create a pull request to contribute.

## Table of Contents

- [Spacing](#spacing)
- [Text](#text)
- [Attributes](#attributes)


## Spacing

Use a space between elements that are on the same indentation.

```slim
/ bad - no spaces

.container
  .heading
    h1
      | Article
  #form
  = simple_form_for article do |f|
    = f.error_notification
    = f.input :title
    = f.input :author
    = f.input :body
    = f.button :submit

/ good - space between same indented elements

.container
  .heading
    h1
      | Article

  #form
    = simple_form_for article do |f|
     = f.error_notification

     = f.input :title

     = f.input :author

     = f.input :body

     = f.button :submit
```

## Text

Text inside an element should be on a new line and indented.

```slim
/ bad - on the same line

h1 Hello World

/ good - on new line and indented

h1
  | Hello World
```

Indent multi-line text with a single pipe

```slim
/ bad - many pipes

p
  | This is a multi-line
  | text that is great
  | we love slim

/ good - on new line and indented

p
  | This is a multi-line
    text that is great
    we love slim
```

## Attributes

For html attributes longer then two, put them on their own line.

```slim
/ bad - on the same line

a href='https://www.github.com' class='btn btn' target='_blank'

/ good - on new lines for each attribute

a(
  href='https://www.github.com'
  class='btn btn'
  target='_blank'
)
```
