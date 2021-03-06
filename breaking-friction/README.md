<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Player Breaking Friction

<sub>[previous](../acceleration/README.md#user-content-player-acceleration) • [home](../README.md#user-content-gms2-move-in-8-directions) • [next](../animated-turn/README.md#user-content-animated-turn)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Now that we have the player accelerating, it is a bit jolting to have the player come to an immediate stop.  Lets add some breaking friction so the player slows down before they stop.

<br>

---


##### `Step 1.`\|`MI8D`|:small_blue_diamond:

*Right click* on **Sprites** and select **New | Sprite** and name it `spr_player_4`. Press the <kbd>Edit Image</kbd> button and create another player with a unique color.  Make sure the **Origin** is set to `Middle Center`.

![add spr_player_4 with an origin of middle center](images/sprPlayerFour.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

*Right click* on **obj_player_acceleration** and select **Duplicate**.  Call this new object `obj_player_friction`. Assign the **Sprite** `spr_player_4`.  

![duplicate obj_player_acceleration and create obj_player_friction](images/dupePlayerAcceleeration.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`MI8D`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Open up **obj_player_friction | Create** event and add a variable for friction called `p_friction`.  This is a week force otherwise the acceleration wouldn't overcome the friction.

![alt_text](images/addFrictionToCreate.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`MI8D`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now open up the **Step** event and lets replace setting the speed to `0` when the player is not moving to reducing the velocity by a small frictional force `p_friction`.

![step event subtract p_friction from speed](images/elseStep.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`MI8D`| :small_orange_diamond:

*Right click* on **Rooms** and select **New | Room** and name it `rm_breaking_friction`. Drag a copy of **obj_player_friction** to the room.

![add a new room rm_frictoin and add obj_player_friction](images/newRoomForFriction.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`MI8D`| :small_orange_diamond: :small_blue_diamond:

Open up **obj_game | Draw Gui** event and add a title for the friction room.

![add title to obj_game draw gui](images/breakingFrictionGame.png)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`MI8D`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. Press the <kbd>Spacebar</kbd> to go to the friction room and press to move then let go. The player now comes to a stop over time and again, looks and feels very different.

![play game and breaking friction takes over when the player lets go of the controls](images/BreakingFriction.gif)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 8.`\|`MI8D`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Lets now take this to a sprite with 8 directions of animation.

1.  *Right click* on **obj_player_friction** and select **Duplicate** and call it `obj_player_friction_8Dir`
2.  Assign the **Sprite** `obj_player_idle_0`
3. Open up **obj_player_friction*8Dir | End Step** event.
4. Delete or comment call to **rotate_player()**
5. If the player is moving then call `set_walk_animation();`
6. Else call `set_idle_animation();`
7. *Right click* on **Rooms** and select **Create | Room** and call it `rm_breaking_friction_8Dir`
8.  Drag **obj_player_friction_8Dir** into the room
9. Open up **obj_game | Draw GUI** and add a title for the room
10. Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. 
11. Press the <kbd>Spacebar</kbd> to go to the friction room and press to move then let go.
12. Now the friction works when you let go of the controls

https://user-images.githubusercontent.com/5504953/141603562-ecd3a573-94aa-4b24-8584-ea4da7150eeb.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 9.`\|`MI8D`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Select the **File | Save Project** then press **File | Quit** to make sure everything in the game is saved. If you are using **GitHub** open up **GitHub Desktop** and add a title and longer description (if necessary) and press the <kbd>Commit to main</kbd> button. Finish by pressing **Push origin** to update the server with the latest changes.

![save, quit, commit and push to github](images/GitHub.png)

___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT TMI8DE">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../acceleration/README.md#user-content-player-acceleration)| [home](../README.md#user-content-gms2-move-in-8-directions) | [next](../animated-turn/README.md#user-content-animated-turn)|
|---|---|---|
