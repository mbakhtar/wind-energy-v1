# Wind Energy 

```package
cakEnergy=github:climate-action-kits/pxt-climate-action-kit-energy
```
## @showhint
Create a ``||Variables:Variable Revolutions||`` and nest 
``||Variables:set Revolutions to 0||`` 
under ``||basic:on start||`` block
```blocks
let Revolutions = 1
```

## @showhint
Now add ``||logic:If true then||`` block and nest it under
``||basic:forever||`` loop
```blocks
let Revolutions = 1
basic.forever(function () {
    if (true) {
        }
    }
)
```
## @showhint
Now add the true condition ``||cakLandTouch:on tap at P0||`` it replaces the true text loop
```blocks
let Revolutions = 1
basic.forever(function () {
    if (cakLandTouch.getTap(cakLandTouch.TouchPin.P0)) {
        
        }
})
```
## @showhint
Add a ``||Variables:change Revolutions by 1||`` from the ``||Variables:Variables||`` drawer and 
then place it under the true condition of the ``||logic: if then||`` loop
```blocks
basic.forever(function () {
    if (cakLandTouch.getTap(cakLandTouch.TouchPin.P0)) {
        Revolutions += 1
    }
})
let Revolutions = 1
```
## @showhint
Add a delay between the ``||cakLandTouch:Touch sensor||`` detecting a 
``||cakLandTouch:Tap||``. Add a ``||basic:pause||`` block from ``||basic:basic||`` drawer
```blocks
basic.forever(function () {
    if (cakLandTouch.getTap(cakLandTouch.TouchPin.P0)) {
        Revolutions += 1
    }
    basic.pause(20)
})
let Revolutions = 1
```
## @showhint
Add an ``||input:on button A pressed||`` block. This will be used to display a value stored in a 
``||Variables:Variable||``
```blocks
input.onButtonPressed(Button.A, function () {
    })
basic.forever(function () {
    if (cakLandTouch.getTap(cakLandTouch.TouchPin.P0)) {
        Revolutions += 1
    }
    basic.pause(20)
})
let Revolutions = 1
```
## @showhint
Nest the ``||basic:show number||`` block under the ``||input:on button A pressed||``
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber()
})
basic.forever(function () {
    if (cakLandTouch.getTap(cakLandTouch.TouchPin.P0)) {
        Revolutions += 1
    }
    basic.pause(20)
})
let Revolutions = 1
```
## @showhint
Now insert ``||Variables:Revolutions||`` oval block in the 
``||basic:show number||`` block
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(Revolutions)
})
basic.forever(function () {
    if (cakLandTouch.getTap(cakLandTouch.TouchPin.P0)) {
        Revolutions += 1
    }
    basic.pause(20)
})
let Revolutions = 1
```

## @showhint
This is the final code
```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(Revolutions)
})
basic.forever(function () {
    if (cakLandTouch.getTap(cakLandTouch.TouchPin.P0)) {
        Revolutions += 1
    }
    basic.pause(20)
})
let Revolutions = 1
```
