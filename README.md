<p align="center">
    <a href="" alt="Perfectionary Logo">
    <img src="https://github.com/LucasJJulien/PerfectDesign/blob/main/media/logowhite.png?raw=true" height="173"/></a>
</p>

<h1 align="center"> PerfectDesign </h1>
<p align="center"> The simple, uniform, and direct CSS library. </p>

> [!CAUTION]  
> Still in Pre-Alpha. Most aspects are underdeveloped, and in some scenarios, severly so.

## What is PerfectDesign?
PerfectDesign is an inherently simple CSS library delivering all core components and nothing more - all in pure css. It uses a naming convention based on uniformity and forthrightness, following a direct syntax: ```{property}-{value}{unit}```. The first letter of each section is extracted: ```d-f``` is ```display: flex```, ```fs-10px``` is ```fontsize: 10px```. 

## Table of contents
- [Roadmap](#roadmap)
- [Documentation](#documentation)
   - [Start](#start)
   - [Usage](#usage)
- [Contributing](#contributing)
- [Versioning](#versioning)
- [License](#license)

## Roadmap
- Add support for other devices, including but not limited to: mobile phones and tablets
- Add components
- Add missing flexbox attributes
- Expand ReadMe and documentation
- Add table support
- Add prebuilt layouts

## Documentation
Full documentation planned for 1.0 release.

## Start
PerfectDesign requires no installation with a package manager such as npm, instead, just reference the CSS file in your html head section. The production folder contains several CSS files that link PerfectDesign together - this is what you import for most use cases. These automatically reference all the css files distributed across the many organization folders - ```complete.css``` includes the entire project. It can be linked with the following code: 

```html
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/lucasjjulien/perfectdesign@master/production/complete.css">
```

To have PerfectDesign in your project locally for modification or otherwise, download the source code and reference the directory where it is located. For example: 

```html
<link rel="stylesheet" type="text/css" href="~/exampleproject/css/perfectdesign/production/complete.css">
```

To import only the PerfectDesign base files which excludes components, swap ```complete.css``` with ```base.css```. For just the components, use ```components.css```. 

Here's a starter template using an HTML 5 doctype:

```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- PerfectDesign CSS -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/lucasjjulien/perfectdesign@master/production/complete.css">

    <title>PerfectDesign</title>
    
  </head>
  <body>
  
    <h1>Hello, world!</h1>

  </body>
</html>
```

## Usage
The naming convention in PerfectDesign mimics the very CSS syntax it's referencing - ```{property}-{value}{unit}```, with the first letter of each section extracted. ```row-gap: 10px``` is ```rg-10px```, and ```flex-wrap: wrap``` is ```fw-w```. 



