---
title: Geekdocs hugo theme 10x better than confluence
description: Review of main theme features than can significantly improve your team communication
slug: hugo-geekdocs-theme
date: 2023-01-03 00:00:00+0000
image: img.png
draft: true
categories:
- Review
tags:
- Docs
- Tools
- Themes
- Static sites
---

## Intro

Static site generators allows to create very feature rich websites just from markdown files.
[Hugo](https://gohugo.io/) has huge and growing community of users because of its usage simplicity and generation speed. 

This two factors brings us a [lot of useful hugo themes for documentation sites](https://themes.gohugo.io/tags/docs/). And [Geekdocs](https://geekdocs.de/) is best on that moment.  

In my opinion, this tool is ideal for creating both internal articles and public documentation.

## Features

### Dark theme

That's it. It's rare feature for many sites and tools.

### Tabs

Underestimated but very useful feature for content organizing in compact way.

You can show what's new. It allows quickly check old content and back to new.

{{< tabs "zero" >}}
{{< tab "v4 - new" >}} User can view and edit site pages 
{{< /tab >}}
{{< tab "v3" >}} User can view site pages  
{{< /tab >}}
{{< /tabs >}}


You can provide compact entity description.

{{< tabs "first" >}}
{{< tab "User" >}} ## User
 
Uses the site 
{{< /tab >}}
{{< tab "Admin" >}} ## Admin

Changes content of the site 
{{< /tab >}}
{{< tab "Developer" >}} 
# Developer 

Develops the site
{{< /tab >}}
{{< /tabs >}}

You can compactly show different paths.

{{< tabs "second" >}}
{{< tab "Success" >}} ## Success
 
Good
{{< /tab >}}
{{< tab "Auth error" >}} ## Auth error

Show "nono" message
{{< /tab >}}
{{< tab "Internal error" >}} 
# Internal error 

Show "ops" message
{{< /tab >}}
{{< /tabs >}}

### Mermaid, diagrams as a code

Best diagram as a code tool. All main diagram types and more. You can easily get or write by yourself entity diagram generation and other diagram types from project source code or sql.

{{< tabs "diagrams" >}}
{{< tab "Entity" >}} ## Entity relation

```mermaid
erDiagram
    User }o--|| Path : has
    User }o--o{ PromptUI : sees
    PromptUI ||--|| Prompt : rendes
    Path ||--o{ Step : contains
    Step ||--o{ Prompt : contains
    Action ||--o{ Prompt : has
```

You can use it inside tabs or other containers.
{{< /tab >}}
{{< tab "Sequence" >}} ## Sequence
But sequenceDiagram has some little rendering troubles inside tabs :)

```mermaid
sequenceDiagram
    Note over User, AppUI: Rendering
    User->>+AppUI: Open screen
    AppUI-->>User: Show screen
    AppUI->>+PathContainer: Give me prompts
    PathContainer->>PathContainer: Finds current step
    PathContainer-->>-AppUI: Current prompts
    AppUI-->>-User: Show prompts
    
    Note over User, AppUI: Interacting
    User->>AppUI: Use prompted element
    AppUI->>+PathContainer: Action used
    PathContainer->>PathContainer: Set prompt invisible
    PathContainer->>PathContainer: Move to next step
    PathContainer-->>-AppUI: Current prompts
```
{{< /tab >}}
{{< tab "Other" >}}
- git flow
- class diagram
- algorithm
{{< /tab >}}
{{< /tabs >}}

### Columns

Documentation main platform is desktop. So we can sacrifice mobile UX for compact and interactive content.

{{< columns >}} <!-- begin columns block -->
**Values**

Show key values in better way.

<---> <!-- magic separator, between columns -->

**Pros and cons**

Compare and list your arguments.

{{< /columns >}}

Show diagram and tabs in two columns. Allow to interact with diagram

TODO check shortcode inside shortcode

{{< columns size="small" >}}
**Diagram**

```mermaid
erDiagram
    User }o--|| Path : has
```

<--->

**Definitions**

- User - uses the app.
- Path is a list of user passed screens passed.

{{< /columns >}}

### Includes

Another underestimated feature. You can paste common content and page previews by one line.

TODO code and screenshot

### Expand

{{< expand "Click me" >}}
## Expand
Hiding not important under spoiler.
{{< /expand >}}

### Progress

Express work progress or some achievements

![](progress.png)

### Hints

{{< quote>}}
**Hits is powerful**

You can make strong accent on important details.
{{< /quote >}}

### Code

```go
func gogo() {
	fmt.Println("code blocks")
}
```

## Conclusion

Out of the box this theme has more useful features than confluence. That features can improve communication efficiency in comparison with google docs, confluence and miro. It can be used for pages about product and its technical realization. If you need advice about comfortable usage and easy setup, go look at other articles here.