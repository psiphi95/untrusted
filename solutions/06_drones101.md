# Drone Cage
## esolitos

```javascript
map.placeObject(map.getWidth()-11, 13, 'block');
map.placeObject(map.getWidth()-11, 12, 'block');
map.placeObject(map.getWidth()-11, 11, 'block');
map.placeObject(map.getWidth()-11, 10, 'block');

map.placeObject(map.getWidth()-10, 13, 'block');
map.placeObject(map.getWidth()-10, 10, 'block');

map.placeObject(map.getWidth()-9, 13, 'block');
map.placeObject(map.getWidth()-9, 10, 'block');
map.placeObject(map.getWidth()-9, 11, 'block');
```

And than just go for the exit from the top.

## amahdy: Block-em, they are idiots

```javascript
map.placeObject(map.getWidth()-5, 11, 'block');
map.placeObject(map.getWidth()-6, 11, 'block');
map.placeObject(map.getWidth()-6, 12, 'block');
map.placeObject(map.getWidth()-5, 13, 'block');
map.placeObject(map.getWidth()-6, 13, 'block');
```

## mathdude314: The drone can't get out if he wanted to
```javascript
map.createFromGrid([
    	' #####',
        ' #   #',
        ' # # #',
        ' # # #',
        '#  #  ',
        ' ##   '
    ], {
    	'#': 'block',
    }, 38, 8);
```

# Drone Creation
##psiphi95: Create own drone army to swarm the enemy

```javascript
   map.defineObject('crusher', {
        'type': 'dynamic',
        'symbol': '*',
        'color': 'green',
        'onCollision': function (attackDrone) {
            'attackDrone'.killedBy('a crusher');
        },
        'behavior': function (attackDrone) {
            moveToward(attackDrone, 'attackDrone');
        }
   });
   for (var i=16; i<map.getWidth()-31; i++) {
   map.placeObject(map.getWidth()-21+i, map.getHeight()-11, 'crusher');
   map.placeObject(map.getWidth()-21+i, map.getHeight()-15, 'crusher');
   }
```

# Function Override
## esolitos

```javascript
function moveToward(obj, type) {
    obj.move('left');
}
```
