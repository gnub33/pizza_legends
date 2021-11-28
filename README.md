# pizza_legends
JS game tutorial by Drew Conley


Part 1 Notes

index.html
the whole of the game will be within the 'game-container' div
canvas tag is where the game will be drawn to
supply aspect ratio (emulating gameboy screen). adjust to art style you are working with
We are adding things to the root directory for now, but as we grow, this project will get massive. There will be a ton of JS files which will have their own directories



style.css
added resets to standardize settings across browsers
disable scrolling when moving character with arrow keys by using 'overflow: hidden'
game-container is the home that houses the entire game (assets, code, UI).
outline property allows us to see container
'margin: 0 auto' moves container to center of screen
scale up game container with transform to increase size of game


init.js
loading images onto screen and drawing pixel data onto canvas
created an overworld instance

overworld.js
JS classes because it mirrors patterns used in other major game engines
class Overworld is top level parent component
how canvas works in html: if you want to draw pixel data from an image onto a canvas context, you first load that image into browser in memory
canvas drawing works linearly, background images are drawn first, then you layer other images on top
since hero asset is a sprite sheet, modify code to draw only one crop of the sheet. the '.drawImage' function will contain 9 arguments
