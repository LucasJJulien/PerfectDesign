<p align="center">
    <a href="" alt="Perfectionary Logo">
    <img src="https://github.com/LucasJJulien/PerfectDesign/blob/main/media/logowhite.png?raw=true" height="173"/></a>
</p>

<h1 align="center"> PerfectDesign </h1>
<p align="center"> The simple, uniform, and direct CSS library. </p>

> [!CAUTION]  
> Currently in pre-alpha. Most aspects are underdeveloped, and in some scenarios, severly so.

## What is PerfectDesign?
PerfectDesign is a simple, lightweight, unopinionated (mostly), and dependency-less CSS library delivering core components and nothing more - all in pure css. It uses a naming convention based on uniformity and forthrightness, following a direct syntax: ```{property}-{value}{unit}```. The first letter of each section is extracted: ```d-f``` is ```display: flex```, ```fs-10px``` is ```fontsize: 10px```. Usage is inherently simple and doesn't require installation or package managers (although NPM support is planned) - just link PerfectDesign in your HTML header file. 

## Table of contents
- [Roadmap](#roadmap)
- [Documentation](#documentation)
   - [Quick Start](#quick-start)
   - [Other Start Options](#other-start-options)
- [Contributing](#contributing)
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
- [ ] Expand ReadMe
- [ ] Build documentation
  - [x] Quick Start
  - [x] Other Start Options
  - [ ] Usage
- [ ] Add contributing guidelines
- [ ] Add prebuilt layouts
- [ ] Add support for NPM
- [ ] Add examples/templates
- [ ] Restructure JsDelivr integration
- [ ] Experiment with SASS remake

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

> [!CAUTION]  
> Due to the nature of no dependencies other than JsDelivr for our CDN, tagging specific releases currently does not work. We are working on a solution.

The above links reference the last stable release of PerfectDesign. To pull the latest source code, use the following link - keep in mind the latest code is unstable and can introduce breaking changes.
```css
https://cdn.jsdelivr.net/gh/LucasJJulien/PerfectDesign@main/production/latest/complete.css
```

To pull a previous version, replace main with the version tag. For version 0.10:
```css
https://cdn.jsdelivr.net/gh/LucasJJulien/PerfectDesign@0.1.0/production/latest/complete.css
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
(Coming Soon)

> [!NOTE]  
> Support for npm is planned. Although PerfectDesign was built partly to avoid the complexity of installation, the convenience and centralization of package managers is undeniable. 

## Usage

### Naming Convention
The naming convention in PerfectDesign mimics the very CSS syntax it's referencing - ```{property}-{value}{unit}```, with the first letter of each section extracted. ```row-gap: 10px``` is ```rg-10px```, and ```flex-wrap: wrap``` is ```fw-w```. There are exceptions to this convention, namely when there are duplicates of the first letter extracted. 

### Exceptions

| Property | Execution |
| --- | --- |
| colors | ```color: black``` - ```c-black```, ```background-color: black``` - ```bgc-black``` |
| min, max | ```min-width: 10px``` - ```minw-10px```, ```max-height: 20px``` - ```maxh-20px``` |

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

It's organized logically with eight main folders:

[`base`](/base/) - Contains all of the base css. 

[`core`](/core/) - Core CSS vital to PerfectDesign

[`components`](/components/) - Buttons, cards, etc

[`modules`](/modules/) - Larger scale than components - layouts, component groups

[`production`](/production/) - The files that link everything forever

[`responsive`](/responsive/) - Responsive design

[`src`](/src/) - Javascript source code (Currently void)

[`testing`](/testing/) - Grounds for experimentation

Base and core can be difficult to differentiate at first. 

<details>
  <summary>Complete Structure</summary>

  ```text
  perfectdesign/
  ├── base/
  │   ├── layout
  │   ├── structure
  │   ├── style
  │   ├── utilities
  ├── core/
  │   ├── global.css
  ├── modules/
  │   ├── components
  │   ├── layout
  ├── production/
  │   ├── latest
  │   ├── local
  │   ├── stable
  ├── responsive/
  │   ├── mobile
  └── src/
      ├── js
  ```
</details>

## Versioning
To adhere with the universal philosophies this very project is based on, PerfectDesign is released under [the Semantic Versioning guidelines](https://semver.org/).

## License
This project is released under the ```MIT license```, hereby granting anyone to use, distribute, or modify this project for, but not limited to, commercial purposes. See the license tab for further information. 
