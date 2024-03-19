---
title: Geekdoc Hugo theme is ten times better than Confluence
description: Review of the main theme features that can significantly improve your team communication
slug: hugo-geekdoc-theme
date: 2023-03-03 10:00:00+0000
image: img.png
draft: false
categories:
- Review
tags:
- Docs
- Tools
- Themes
- Static sites

---

## Intro

Static site generators allow you to create feature-rich websites from just markdown files.
[Hugo](https://gohugo.io/) has a large and growing community of users due to its simplicity and speed of generation.

As a result, there are many useful [Hugo themes](https://themes.gohugo.io/tags/docs/) available for documentation sites,
and currently, [Geekdocs](https://geekdocs.de/) is the best one.

This tool is ideal for creating both internal articles and public documentation.

## Features

### Dark theme

That's it. It's a rare feature for many sites and tools.

### Tabs

It's an underestimated but handy feature for organizing content in a compact way.

You can easily show what's new, allowing users to quickly check old content and return to new.

{{< tabs "zero" >}}
{{< tab "v4 - new" >}} User can view and edit site pages
{{< /tab >}}
{{< tab "v3" >}} User can view site pages  
{{< /tab >}}
{{< /tabs >}}

You can provide a compact description of entities.

{{< tabs "first" >}}
{{< tab "User" >}}## User

Uses the site
{{< /tab >}}
{{< tab "Admin" >}}## Admin

Changes content of the site
{{< /tab >}}
{{< tab "Developer" >}}## Developer

Develops the site
{{< /tab >}}
{{< /tabs >}}

You can compactly show different paths.

{{< tabs "second" >}}
{{< tab "Success" >}}## Success

Good
{{< /tab >}}
{{< tab "Auth error" >}}## Auth error

Show "nono" message
{{< /tab >}}
{{< tab "Internal error" >}}## Internal error

Show "ops" message
{{< /tab >}}
{{< /tabs >}}

### [Mermaid](https://mermaid.js.org/), diagrams as a code

The best [diagram as code]({{< ref "/post/diagrams-as-code-benefits" >}}) tool for all main diagram types and more. 
You can easily generate entity diagrams and other diagram types 
from project source code or SQL, or write them yourself.

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

Since the main platform for documentation is the desktop, 
we can sacrifice mobile UX over compact and interactive content.

{{< columns >}} <!-- begin columns block -->
**Values**

Show key values in a better way.

<---> <!-- magic separator, between columns -->

**Pros and cons**

Compare and list your arguments.

{{< /columns >}}

Show diagram and legend in two columns.

{{< columns size="small" >}}
**Diagram**

```mermaid
erDiagram
    User }o--|| Path : has
```

<--->

**Definitions**

- User - uses the app.
- Path is a list of user-passed screens passed.

{{< /columns >}}

### Expand

{{< expand "Click me" >}}
## Expand

Hiding is not important under spoiler.
{{< /expand >}}

### Progress

![Express work progress or some achievements](progress.png)

### Hints

{{< quote>}}
**Hits are powerful**

You can emphasize important details.
{{< /quote >}}

### Code

```go
func gogo() {
fmt.Println("code blocks")
}
```

## Conclusion

This theme has more useful features out of the box than Confluence. 
These features can improve communication efficiency compared to Google Docs, Confluence, and Miro. 

It can be used for pages about a product and its technical realization.

By using this theme, you can enjoy all the [benefits of static sites]({{< ref "/post/static-sites-better" >}}). 
If you need guidance on using it comfortably and setting it up easily, feel free to contact me. 
I'll be happy to help you out.
