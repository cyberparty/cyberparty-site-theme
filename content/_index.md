+++
title = "Welcome"
template = "index.html"
+++

This is the Cyberparty Site Theme! It's a Zola site theme I made for my own purposes that I could modify to my liking. As such, it will likely be changed without warning or regard for what other users may want out of it. Regardless, it's public and open source in case you want to modify or use it yourself! 

## Why Zola?

I initially started out trying to make this as a Hugo theme, as I had heard Hugo was a popular static site generation option. Unfortunately, I found that I really, really didn't like the templating language syntax that Hugo used and I found it difficult to work with. Zola was next on my list, and I found its templating language far easier to work with. Being written in Rust is always a plus, also! /shill

## Features

This theme has a few attributes that may make it stand out from some other themes.

#### Adaptive mobile-friendly view

The header bar will switch to a vertical flex style when being viewed at a narrow width, ensuring that you're still able to see both the title and navigation menu even on mobile displays.

#### Consistent across pages

Speaking of the header bar, it's staying there on every page you visit. The only thing that changes across pages is the main page content, as defined by the markdown files you write. 

#### No external dependencies

No calls to any external resources / CDNs for additional resources are made within this theme by default: Everything that is needed is retrieved and served locally. This has the benefit of protecting against compromised third parties, but the drawback of having the load times for *all* resources depend solely on the host: A CDN that's quicker and/or has a server closer to the end user won't be present to pick up the slack on slower hosts. There's not much to be transferred, regardless, so it won't make too much difference.

#### No JavaScript

I feel that my needs are fairly simple and able to be met without the use of JavaScript, so I decided against using it for security and consistency reasons. While using JavaScript is avoided, using CSS hacks to replicate interactivity is also avoided [due to accessibility concerns](https://adrianroselli.com/2023/03/css-only-widgets-are-inaccessible.html). This theme used to feature a CSS-only hamburger menu, but it was dropped due to such concerns, and because making it properly keyboard-accessible included using JavaScript.  

## Source

The source is [located at the theme's GitHub repo](https://github.com/cyberparty/cyberparty-site-theme).