# What is demoChanceTool?

demoChanceTool is a simple enviornment setup with your basic file structure including index.html, /js, and /css, that shows how the Ruby Chance tool works.  Chance is a Ruby Build tool that automates image sprites and merges all CSS files into one master/theme.css file. 

You can look at the original Chance code developed by Josh Holt here: https://github.com/joshholt/Chance

## How to Install?
Either clone this project or download the zip file.

### ATTENTION: Mountain Lion Users

You'll need to do the following steps to get the demoChanceTool to work you'll need to run the following 3 commands to update RMagick gem.

```html
$ brew remove imagemagick
```
```html
$ brew install imagemagick
```
```html
$ sudo xcode-select -switch /Applications/Xcode.app/Contents/Developer/
```

### Basic Setup

#### File Structure/Layout

```html
|-- demoChanceTool
|	|-- chance
|		|-- lib
|		|-- scripts
|	|-- js
|	|-- theme
|		|-- images
|			|--400x300
|	|-- index.html
```

#### Setup

1. Edit ./demo file located in the chance/ directory by updating the PATH to match where you cloned your project on your computer, otherwise, Chance won't work.  Make sure to replace where it says ~/Desktop/Brad\ Kahl/GIT/demoChanceTool/theme to match your PATH.  Look at the example below to see what code exist within the ./demo file.

```html
ruby chance.rb -i ~/Desktop/Brad\ Kahl/GIT/demoChanceTool/theme -o ~/Desktop/Brad\ Kahl/GIT/demoChanceTool/prod-theme --prefer-smaller-download
```

## How to Use?

Open up terminal and run the following commands to get chance to output your master/sprite files.

```html
$ cd demoChanceTool/chance/
```
```html
$ ./demo
```

### Things To Note
1. You can make as many CSS files that you want and add as many directory's to the image/ directory within the theme/ directory of your project for organizationally purposes.  As long as it's within the theme/ directory, your golden.
2. You do not need to remove the prod-theme/ directory every time you want to run Chance, the Chance tool is smart enough to update your code on run.











