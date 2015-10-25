Scene
==========

RPG Maker MV's `Stage` class extends `PIXI.Stage`

## API Documentation

### Properties

#### `dirty`
Whether the stage is dirty and needs to have interactions updated

#### `interactionManager`
The interaction manage for this stage, manages all interactive activity on the stage

#### `interactive`
Whether or not the stage is interactive

#### `stage`
The stage is its own stage.

#### `worldTransform` (read-only)
Current transform of the object based on world (parent) factors

### Methods

#### `Stage.initialize()`
TBW

#### `Stage.setInteractionDelegate(domElement)`

> `pixi.js`: PIXI.Stage.prototype.setInteractionDelegate(domElement)

Sets another DOM element which can receive mouse/touch interactions instead of the default Canvas element. This is useful for when you have other DOM elements on top of the Canvas element.

#### `Stage.updateTransform()`

> `pixi.js`: PIXI.Stage.prototype.updateTransform = function()

Updates the object transform for rendering

#### `Stage.setBackgroundColor(backgroundColor)`

> `pixi.js`: PIXI.Stage.prototype.setBackgroundColor(backgroundColor)

Set the background color of the stage.

###### Source
```
PIXI.Stage.prototype.setBackgroundColor = function(backgroundColor)
{
    this.backgroundColor = backgroundColor || 0x000000;
    this.backgroundColorSplit = PIXI.hex2rgb(this.backgroundColor);
    var hex = this.backgroundColor.toString(16);
    hex = '000000'.substr(0, 6 - hex.length) + hex;
    this.backgroundColorString = '#' + hex;
};
```

#### `Stage.getMousePosition()`

> `pixi.js`: PIXI.Stage.prototype.getMousePosition

This will return the point containing global coordinates of the mouse.


```
//-----------------------------------------------------------------------------
/**
 * The root object of the display tree.
 *
 * @class Stage
 * @constructor
 */
function Stage() {
    this.initialize.apply(this, arguments);
}

Stage.prototype = Object.create(PIXI.Stage.prototype);
Stage.prototype.constructor = Stage;

Stage.prototype.initialize = function() {
    PIXI.Stage.call(this);

    // The interactive flag causes a memory leak.
    this.interactive = false;
};

/**
 * [read-only] The array of children of the stage.
 *
 * @property children
 * @type Array
 */

/**
 * Adds a child to the container.
 *
 * @method addChild
 * @param {Object} child The child to add
 * @return {Object} The child that was added
 */

/**
 * Adds a child to the container at a specified index.
 *
 * @method addChildAt
 * @param {Object} child The child to add
 * @param {Number} index The index to place the child in
 * @return {Object} The child that was added
 */

/**
 * Removes a child from the container.
 *
 * @method removeChild
 * @param {Object} child The child to remove
 * @return {Object} The child that was removed
 */

/**
 * Removes a child from the specified index position.
 *
 * @method removeChildAt
 * @param {Number} index The index to get the child from
 * @return {Object} The child that was removed
 */
```
