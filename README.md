<p align="center">
    <a href="" alt="Perfectionary Logo">
    <img src="https://github.com/LucasJJulien/PerfectDesign/blob/main/media/logowhite.png?raw=true" height="173"/></a>
</p>

<h1 align="center"> PerfectDesign </h1>
<p align="center"> The simple, uniform, and direct CSS library. </p>

> [!CAUTION]  
> Currently in pre-alpha. Most aspects are underdeveloped, and in some scenarios, severly so.

## What is PerfectDesign?
PerfectDesign is a simple, lightweight, and dependency-less CSS library delivering core components and nothing more - all in pure css. It uses a naming convention based on uniformity and forthrightness, following a direct syntax: ```{property}-{value}{unit}```. The first letter of each section is extracted: ```d-f``` is ```display: flex```, ```fs-10px``` is ```fontsize: 10px```. Usage is inherently simple and doesn't require installation or package managers (although NPM support is planned) - just link PerfectDesign in your HTML header file. 

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

## Documentation
Full documentation in development. 

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
To have PerfectDesign in your project locally for modification or otherwise, download the source code and reference the directory where it is located. For example: 

```html
<link rel="stylesheet" type="text/css" href="~/exampleproject/css/perfectdesign/production/local/complete.css">
```

The above links reference the last stable release of PerfectDesign. To pull the latest source code, use the following link - keep in mind the latest code is unstable and can introduce breaking changes.
```html
https://cdn.jsdelivr.net/gh/LucasJJulien/PerfectDesign@main/production/latest/complete.css
```

To pull a previous version, replace main with the version tag. For version 0.10:
```html
https://cdn.jsdelivr.net/gh/LucasJJulien/PerfectDesign@0.1.0/production/latest/complete.css
```

To import only the PerfectDesign base files which excludes components, swap ```complete.css``` with ```base.css```. For just the components, use ```components.css```.

> [!NOTE]  
> Support for npm is planned. Although PerfectDesign was built partly to avoid the complexity of installation, the convenience and centralization of package managers is undeniable. 

## Usage
The naming convention in PerfectDesign mimics the very CSS syntax it's referencing - ```{property}-{value}{unit}```, with the first letter of each section extracted. ```row-gap: 10px``` is ```rg-10px```, and ```flex-wrap: wrap``` is ```fw-w```. 

## Contributing
Our coding standards and notes are in development. Until out of prealpha, public contributions will not be accepted.

## Versioning
To adhere with the universal philosophies this very project is based on, PerfectDesign is released under [the Semantic Versioning guidelines](https://semver.org/).

## License
This project is released under the ```MIT license```, hereby granting anyone to use, distribute, or modify this project for,, but not limited to, commercial purposes. See the license tab for further information. 
