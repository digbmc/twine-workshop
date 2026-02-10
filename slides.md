---
title: Creative Coding with Twine
date: February 11, 2026
author: Alice McGrath
subtitle: Experimental Literature Course
format: 
    revealjs:
        theme: moon
        controls: true
        #embed-resources: true
css: "https://alicemcgrath.digital.brynmawr.edu/pres/a3.css"
editor:
    render-on-save: true
---

# Outline

- Introduction
- Twine editing interface
- Customization basics
- Publishing guide

## Hypertext!

- In the early days of the internet, the idea of 'hypertext' revolutionized book forms
- Rather than a linear narrative (a scroll) or a sequential but segmented narrative (a book), hypertext enabled new forms of interactivity, multilinearity, and a network-based arrangement
- Internal references (i.e. footnotes and other paratext, Choose-your-own-adventure, etc.) have already done this, but suddenly it was possible at a new scale
- Fun fact: Vladimir Nabokov's *Pale Fire* (1962) was almost used to demonstrate an early hypertext system in an IBM presentation in 1969

## Hypertext Literature

An experimental form of fiction that digs into this multilinearity, mostly early-mid 1990s, distributed via CD-Rom

- *Patchwork Girl: A Modern Monster* by Shelley Jackson

> "In hypertext, everything is there at once and equally weighted. It is a body whose brain is dispersed throughout the cells, fraught with potential, fragile with indecision, or rather strong in foregoing decisions, the way a vine will bend but a tree can fall down.[[7]](https://en.wikipedia.org/wiki/Patchwork_Girl_\(hypertext\)#cite_note-7)"
	- Jackson, "Stitch Bitch: the patchwork girl", 1997

## So what?
- All of the internet is hypertext: context is created by hyperlinks that can be followed backwards and forwards and read in any order
- [Twine](https://twinery.org/) is designed to make it easy to build interactive fiction without knowing how to code
- It's used to create interactive fiction and text-based games that evoke this early hypertext era


## Twine
- Open-source tool for creating interactive fiction, games, and hypertext narratives
- Output is simple HTML (Hyper Text Markup Language) that can be deployed on any web server
- No-code editor that uses simple markup
- 4 "story formats" that change the functionality and style: we are focusing on Harlowe

# Twine Editor Interface

## Before we begin
- Story format options
	- **Harlowe** - default format. This is what we are using for this workshop.
	- Chapbook - also beginner-friendly
	- SugarCube & Snowman - designed for advanced users and more customization
- You can download the application or use it in browser (if you use it in browser, backup and save often)
- You can also use a text editor and a markup language called "Twee"

## Getting started
1. Navigate to [https://twinery.org/](https://twinery.org/)
2. Click 'Use in your browser'
3. In the top-left corner, click `+ New` and give your story a name
4. The editor has an overall map with a single passage -- double click to edit
5. Enter some text and rename your passage
6. Click `Test From Here` to preview your game in a new tab

## Basics
- Link to a new passage using double square brackets `[[pasage name]]`
- Use hash marks to create headers: `# Header 1` and `## Header 2`
- Use `**` for `**bold**` and `*` for `*italic*`
- Use the WYSIWYG editor for other types of customizations

## Vocab

- Markup - How data is structured, displayed, organized
- Story - Twine project, website, or game
- Passage - A contained section of a Twine story that can be linked to
- Macro - A 'function' or bit of code used to enhance text functionality, indicated with parentheses
- Hook - the passage of text that a macro acts on, indicated with square brackets
`(font: "Arial")[This text will be in Arial.]`
- Variable - A container for values and words that can change within the game
`(set: $myName to "Alice") Hello, $myName!`  
- Function - "if this then this" - takes input and produces output

## Tips

- Preview your work often to make sure the functionality is what you want
- Export your work often to save it somewhere safe
- Create an outline or storyboard before you try to build complex functionality
- To check your story format: from the story editor, select 'Details' and select 'Harlowe 3.3.9'

## Your turn!

Create a few passages and practice linking between them. Explore the editor interface options to try out more complex stuf.

# Customization
Make your twine pretty and interactive

## Things to try
- Style customizations
- Hide and show page content with links
- Variety and randomness
- Variables and conditionals

## Macros
You can create macros using buttons in the main editor or by using text markup

- Change the background - `(bg:purple)[Text]`
- Change the text color - `(color:yellow)[Text that is yellow]`
- Add some whimsy - `(text-style:"shudder")[Text that moves]`

## Usage examples

Go to the [how-to](/#how-to) section of the home page for more

```md
(link: "Click here please")[Thank you for clicking!]
(display: "Cellar") <!-- Display a passage -->
(set: $points to it + 1)
The weather was (either: "snowy", "rainy", "sunny")
```

## Your turn!

Give your game a makeover with some styling and customization.

Need inspiration? Check out the [Digital Scholarship Adventure Game](https://digitalscholarship.brynmawr.edu/game/) or [Critters](https://alicetmcgrath.com/fun/)

## Advanced: HTML
- Twine is designed to be text-based, however, you can add images using html if they are hosted somewhere else:
```html
<img src="exampleurl.com/cat.jpg" alt="a cat in a box">
```
- Other HTML syntax may work (but will sometimes break)

## Advanced: Style
- If you have some experience with CSS, you can apply style to the whole story by going to **Story** -> **Stylesheet**
- Use CSS selectors `tw-passage` `tw-story` and `tw-link` to apply style changes to your entire site
- Macros are recommmended for this purpose see [these instructions](https://twinery.org/cookbook/css/storyformats/harlowe.html)

# Deployment
How to let others play your game

## Options

- Domain of One's Own - digital.brynmawr.edu - webhosting for BMC (Haverford Sites for HC)
- GitHub Pages - github.com - 

## Export your game
- From the Twine top menu, go to **Build** -> **Publish to File** to export your game as html
- Open it in a browser app to play it locally

## Filenames
- By default, the filename of your game will include the title
- Edit the filename so it has no spaces in it - this will be part of your URL
- *Pro tip*: change the filename to `index.html`

## Log in to Domain of One's Own
- Navigate to [digital.brynmawr.edu](https://digital.brynmawr.edu/) and click on "Get Started" to log in
- If you haven't already, choose a domain name that is relatively short and unique

## Upload your game
- From your DoOO Dashboard, locate the "File Manager"
- Navigate to the folder called "public_html"
- Create a new sub-folder called "game"
- Upload your game to the "game" folder

## Sharing your game
- Your game should now be public at [yourdomain.digital.brynmawr.edu/game/filename.html]()
- If you changed the filename to index, your url will be [yourdomain.digital.brynmawr.edu/game]()
- Congratulations, you are a published author of interactive fiction!

## Resources
- [Twine Cookbook]([https://twinery.org/cookbook/](https://twinery.org/cookbook/))
- Harlowe documentation: [https://twine2.neocities.org/](https://twine2.neocities.org/) - this is the standard story template
- [Twine and Interactive Fiction Handbook (slides)](https://docs.google.com/presentation/d/1bNzxW39pYul2yVieuxaSsnB5SAexOde1Higr9mxs7EA/edit)
- [Programming Historian: Interactive Text Games Using Twine](https://programminghistorian.org/en/lessons/interactive-text-games-using-twine)

## Get help!
- Come to Digital Scholarship Office Hours, 1-3 PM in the Carpenter DMCL!
- Email digitalscholarship@brynmawr.edu or help@brynmawr.edu

