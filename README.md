## Visual Computing Slides -- colors
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors)

Part of the *Visual Computing* course given at [National University of Colombia](http://www.disi.unal.edu.co/) by [Jean Pierre Charalambos](http://otrolado.info) and [Andres Colubri](http://andrescolubri.net/).

Powered by [reveal](https://github.com/hakimel/reveal.js).

<!--- a long list of students and links to their pages. To come ;) -->

## Installation

 ```sh
 $ git clone https://github.com/VisualComputing/colors.git
 $ cd colors
 $ git checkout gh-pages
 ```

## Folder Structure

    |-- css/
    |-- js/
    |-- plugin/
    |-- lib/
    |-- fig/
    |-- sketches/
    |-- index.html
    |-- source.md
    
Refer to the [reveal folder structure](https://github.com/hakimel/reveal.js#folder-structure) for more details, and to the *Setup* below.

## Setup

External markdown and speaker notes, require that presentations run from a local web server. The following instructions will set up such a server as well as all of the development tasks needed to make edits to the slides source code.

1. Install [Node.js](http://nodejs.org/)

2. Install [Grunt](http://gruntjs.com/getting-started#installing-the-cli)

3. Install dependencies (you must be already on the presentation folder, otherwise ```$ cd colors```)

 ```sh
 $ npm install
 ```

4. Edit the presentation contents using [markdown](http://daringfireball.net/projects/markdown/) in the `source.md`, adding figures to the `fig/` folder and [p5.js skectches](http://p5js.org/) to the `skectches/` folder (detailed instructions below) as needed.

5. Serve the presentation and monitor source files for changes

 ```sh
 $ grunt serve
 ```

6. Open <http://localhost:8000> to view your presentation

 You can change the port by using `grunt serve --port 8001`.

<!---

7. Update to upstream

 ```sh
 $ git remote add reveal.js https://github.com/hakimel/reveal.js.git
 $ git pull reveal.js master
 ```
-->

## [p5.js](http://p5js.org/) sketches

1. Create your js sketch in the ```sketches``` folder, e.g.,


 ```sh
 $ touch sketches/mysketch.js
 ```
 
2. Define a canvas _id_ (e.g., ```mysketch_id```) within your _mysketch.js_ `setup` function:

 ```javascript
 function setup() {
    var myCanvas = createCanvas(400, 400);
    myCanvas.parent('mysketch_id');
 }
 ```

3. Include your sketch as a script in the ```index.html```, e.g., ```<script src="sketches/mysketch.js"></script>```

4. Locate your sketch in the ```source.md``` at the place you want it to be, using the _id_: defined in step *2*, e.g., ```<div id='mysketch_id'></div>```

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/kentcdodds/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars2.githubusercontent.com/u/645599?v=4" width="100px;"/><br /><sub><b>Jean Pierre Charalambos</b></sub>](https://github.com/nakednous)<br />[💻](https://github.com/VisualComputing/colors/commits?author=nakednous "Code") [📖](https://github.com/VisualComputing/colors/commits?author=nakednous "Documentation") [🐛](https://github.com/VisualComputing/colors/issues?q=author%3Anakednous "Bug reports") [🎨](#design-nakednous "Design") [🤔](#ideas-nakednous "Ideas, Planning, & Feedback") [💬](#question-nakednous "Answering Questions") [📢](#talk-nakednous "Talks") [⚠️](https://github.com/VisualComputing/colors/commits?author=nakednous "Tests") [🔧](#tool-nakednous "Tools") |
| :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!