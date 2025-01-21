<p align="center">
    <a href="" alt="Perfectionary Logo">
    <img src="https://github.com/LucasJJulien/PerfectDesign/blob/main/media/logowhite.png?raw=true" height="173"/></a>
</p>

<h1 align="center"> PerfectDesign </h1>
<p align="center"> The simple, uniform, direct, and universal CSS library. </p>

> [!CAUTION]  
> Currently in pre-alpha. Most aspects are underdeveloped, and in some scenarios, severly so.

## What is PerfectDesign?
PerfectDesign is a simple, lightweight, and dependency-less CSS library delivering core utilities, base componentry, and nothing more - all in pure css. It uses a naming convention based on uniformity and forthrightness, following a syntax based directly on the underlying CSS: ```{property}-{value}{unit}```. The first letter of the property and value are extracted: ```d-f``` is ```display: flex```, ```fs-10px``` is ```fontsize: 10px```. Usage is inherently simple and doesn't require installation or package managers (although NPM support is planned) - just link PerfectDesign in your HTML header file. 

The guiding principles of PerfectDesign are as follows: 1. utility first architecture to remove the abstraction and bloat of component-based libraries and 2. freedom, you aren't forced to choose from pre-curated lists like ```text-sm```, although they are available for uniformity.

## Table of contents
- [Roadmap](#roadmap)
- [Documentation](#documentation)
   - [Quick Start](#quick-start)
   - [Other Start Options](#other-start-options)
- [Contributing](#contributing)
- [Bird's Eye View](#bird's-eye-view)
- [Versioning](#versioning)
- [License](#license)

## Roadmap
- [ ] Add table support
- [ ] Add responsive attributes for other devices, namely
  - [ ] Mobile
  - [ ] Tablets
  - [ ] Dynamic
- [ ] Add components
  - [ ] Buttons
  - [ ] Cards
- [ ] Add prebuilt layouts (containers)
- [ ] Add missing flexbox attributes
- [x] Expand ReadMe
- [ ] Build documentation
  - [x] Quick Start
  - [x] Other Start Options
  - [ ] Usage
- [ ] Add contributing guidelines
- [ ] Add prebuilt layouts
- [ ] Add support for NPM
  - [ ] Build system to compile only used CSS
- [ ] Add examples/templates
- [ ] Restructure JsDelivr integration

## Documentation
Full documentation is in development and will be presented on a webpage separate from this readme. Previous documentation releases will be made available. 

## Quick Start
PerfectDesign requires no installation or package managers. Instead, just reference the CSS file in your HTML head section. The production folder contains several CSS files that link PerfectDesign together - this is what you import for most use cases. These automatically reference all the css files distributed across the many organization folders - ```complete.css``` includes the entire project. It can be linked with the following code: 

```html
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/LucasJJulien/PerfectDesign/production/stable/complete.css">
```

Here's a starter template using an HTML 5 doctype:

```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- PerfectDesign CSS -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/LucasJJulien/PerfectDesign/production/stable/complete.css">

    <title>PerfectDesign</title>
    
  </head>
  <body>
  
    <h1>Hello, world!</h1>

  </body>
</html>
```

## Other Start Options

### Local use
To have PerfectDesign in your project locally for modification or otherwise, download the source code and reference the directory where it is located. For example: 

```html
<link rel="stylesheet" type="text/css" href="~/exampleproject/css/perfectdesign/production/local/complete.css">
```

### Using other versions
The above links reference the last stable release of PerfectDesign. To pull the latest source code, use the following link - keep in mind the latest code is unstable and can introduce breaking changes.
```css
https://cdn.jsdelivr.net/gh/LucasJJulien/PerfectDesign@main/production/latest/complete.css
```

Due to the nature of no dependencies other than JsDelivr for our CDN, we've opted not to use tools like WebPack or Parcel for bundling, and as such, tagging specific releases is not possible unless you use PerfectDesign locally. 

However, you can pull the specific files of previous versions. Type the version tag after the @ and then the directory. To reference ```flexbox.css``` from version 0.1.0:
```css
https://cdn.jsdelivr.net/gh/LucasJJulien/PerfectDesign@0.1.0/base/layout/flexbox.css
```

### Importing individual aspects
In a general sense, PerfectDesign can be separated into three sections - all of which can be individually imported if you require only a fraction of what PerfectDesign provides. 

To import the complete library:
```css
complete.css
```

To import only the base files which excludes prebuilt modules or components:
```css
base.css
```

To import only the modules (these function independently from base css):
```css
modules.css
```

### Minified
Minified CSS can also be used:

```html
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/LucasJJulien/PerfectDesign/production/stable/min/complete.css">
```

> [!NOTE]  
> Support for npm is planned. Although PerfectDesign was built partly to avoid the complexity of installation, the convenience and centralization of package managers is undeniable. 

## Usage

### Naming Convention
The naming convention in PerfectDesign mimics the very CSS syntax it's referencing - ```{property}-{value}{unit}```, with the first letter of the property and value extracted. ```row-gap: 10px``` is ```rg-10px```, and ```flex-wrap: wrap``` is ```fw-w```. Units are condensed: pixels ```px```, percent ```p```, rem ```rem```. With CSS that can set multiple properties such as ```columns: 100px 3```, the properties are seperated by an underscore: ```c-100px_3```. Properties with decimal values have the letter ```d (decimal)``` where the period would be. ```font-size: 0.75rem``` would be ```fs-d75rem```. Properties with a whole number and decimal value are portrayed as such: ```font-size: 1.5rem``` is ```fs-1d5rem```. Negative values are indictated with the letter ```n (negative)``` prior to the value. ```letter-spacing: -0.05rem``` is ```ls-nd05rem```. 

There are exceptions to this convention, namely when there are duplicates of the first letter extracted. 

### Exceptions
| Property | Execution |
| --- | --- |
| colors | ```color: black``` - ```c-black```, ```background-color: black``` - ```bgc-black``` |
| min, max | ```min-width: 10px``` - ```minw-10px```, ```max-height: 20px``` - ```maxh-20px``` |

Names like ```vertical-align-center``` are undoubtedly better descriptions than the crappy CSS property names like ```justify-content: center```, but are opinionated and applies best to it's creator. Replicating the names of the CSS properties like ```justify-content``` as ```jc``` carries over the not-so-good naming convention of CSS into HTML, but keeps everything uniform and equivalent to the standard CSS has already set. 

The same goes for names with ```xs``` like ```text-xs```; the best value to be associated with the abbreviation is relative to the person. Although PerfectDesign might implement ```xl, xs, etc``` for ease of use, uniformity, and to build a standard within the library, we have prioritzied freedom over values predefined by the creators.

### Value-based CSS
PerfectDesign increments on an interval of 1, 5, 25, 50, and 100 for numerically based CSS properties. Take for example width in pixels - it increments on an interval of 5 up to 100, base 25 up to 500, and base 100 up to 1000. Why? Because base 5 and 10 are perfect, and well, this is PerfectDesign. Jokes aside (I actually wasn't joking though), there's so little difference between say 50 and 55 pixels that values in between just aren't needed. Additionally, all values on base 5 adds uniformity to the design. 

## Contributing
> [!WARNING]  
> Until out of pre-alpha, public contributions will not be accepted.

```
# Clone the repository
git clone https://github.com/LucasJJulien/PerfectDesign

# Fork the repo

# Create a new branch from main
git checkout -b feature/your-feature-name

# Push your changes
# Create a pull request against the "main" branch
```

### Coding Standards
Please adhere to our coding standards (in development) to uphold our development philosophy. 

## Bird's Eye View
How does it all work under the hood?

PerfectDesign is pure css. It might seem counter intuitive to use such a bad "language" in the name of simplicity when tools like SASS, PostCSS, and Less.js exist. These are great and superficially simplify the process of creating stylesheets, but require installation and end up compiling CSS in the end anyways. This is meant to be dead simple. 

### Organization
It's organized logically with eight main folders:

[`base`](/base/) - Contains all of the base css. 

[`core`](/core/) - Core CSS vital to PerfectDesign

[`components`](/components/) - Buttons, cards, etc (Child of modules)

[`modules`](/modules/) - Larger scale than components - layouts, component groups

[`production`](/production/) - The files that link everything together

[`responsive`](/responsive/) - Responsive design

[`src`](/src/) - Javascript source code (Currently void)

[`testing`](/testing/) - Grounds for experimentation

Base and core can be difficult to differentiate at first. Core contains foundational CSS like global attributes. Base houses all the basic CSS like background-color, row-gap, etc. 

### How does PerfectDesign deliver the CSS?
PerfectDesign has no dependencies other than JsDelivr for the CDN - which isn't really a dependency. The production folder contains CSS files that use the @import tag to "bundle" everything together. We've opted not to use Webpack of Parcel to auto bundle with Github actions in an effort to keep PerfectDesign as simple as possible throughout. 

### Structure Visualized
```text
perfectdesign/
├── base/
│   ├── layout/
│       ├── alignment.css
│       ├── flexbox.css
│       ├── grid.css
│       ├── positioning.css
│       ├── spacing.css
│       └── alignment.css
│   ├── structure/
│       ├── media.css
│       └── size.css
│   ├── style/
│       ├── border.css
│       ├── colors.css
│       ├── fonts.css
│       └── text.css
│   └── utilities/
│       └── zindex.css
├── core/
│   ├── global.css
├── modules/
│   ├── layout.css
│   └── components/
│       ├── buttons.css
│       └── cards.css
├── production/
│   ├── latest/
│   ├── local/
│   ├── stable/
├── responsive/
│   ├── mobile
└── src/
    └── js
```

## Versioning
To adhere with the universal philosophies this very project is based on, PerfectDesign is released under [the Semantic Versioning guidelines](https://semver.org/).

## License
This project is released under the ```MIT license```, hereby granting anyone to use, distribute, or modify this project for, but not limited to, commercial purposes. See the license tab for further information. 
