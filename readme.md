# Workshop

Remember to save (Ctrl + S) whenever you make a change.


## Geting ready
- [ ] Open PICO 8 in browser tab https://www.pico-8-edu.com/. Hit the play button  
- [ ] Get Ambulanse.p8.png from https://bit.ly/uia_nibble (https://github.com/UiA-SkunkWorks/codeNibble )
- [ ] Drop the Ambulanse.p8.png onto the Pico8 editor
- [ ] Run game (just type run and hit enter).

## Drawing
- [ ] Enter the editor (hit the ESCAPE key).
- [ ] Draw the ambulance front in cell 1
- [ ] Draw the ambulance back in cell 17
- [ ] Draw the alternative front in cell 2
![The full sprite](/sprite.png)

## Drawing code

- [ ] In *init* add the variables *car_front* and *car_back* set the values to 1 and 17 respectivly
```Lua
car_front = 1
car_back = 17
```
- [ ] In update we are goint to use the *spr* function to draw the car, spr is short for sprite and you can think of sprit as drawing. The *spr* function takes a number as input, this is the number of the sprite you want to draw. 
```Lua
spr(car_front,x,y)
spr(car_back,x,y+7)
```
- [ ] Run the code by exiting the editor (hit exit), then type run and hit enter.

## Moving Ambualnce
- [ ] Find the *-- moving left or right* comment. we are going to use the *btn* function to test if a button is pressed. The btn function takes one input, the number of the button to check. 1 is left, 2 is right.
```Lua
if btn(1) then
 x = x - speed
end

if btn(2) then
 x = x + speed
end
```
- [ ] Run the code by exiting the editor (hit exit), then type run and hit enter. Test moving left and right. 
- [ ] Atempt giving the ambulanse a more reasonable speed (test)

## Sound

- [ ] Open the sound efects editor. Lets make a babu sound. (space lets you test the sound while making it)

-[ ] In the code editor in the *init* function use the *sfx* function to run your sound. *sfx* is short for sound effects. Like the *spr* function it takes the number of the sound you want to play. It can also take a secondary parameter and that is the chanel you want to play on. We are going to play sound 1 on channel 1.

```Lua
sfx(1,1)
```

## collisions 
-[ ] We are now going to give a short explenation of how collisions work.


## Points
Our game need points to drive engamgnet. 
- [ ] Add points variable set to 0 in init function (points = 0).  
- [ ] Add update logic in update activ section 
```Lua
if (time()-last) > 2 then
    points = points+1
    last = time()
end
```
- [ ] Add drawing code in draw method
```Lua
elseif active == true then
    print(points,10,10);

```
