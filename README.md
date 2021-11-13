# GMS2 Move in 8 Directions


<!-- OVERVIEW -->
This tutorial is intended for those wanting an introduction to <i>GameMaker Studio 2</i> using their scrpting language <i>GML</i>. This assumes no prior knowledge of the software or scripting. 

Lets look at various ways of moving a human character in 8 dirctions.

* Tested on GameMake Studio2.3.5.589
* An existing [GML Project](https://github.com/maubanel/GMS2-Snippets/blob/main/rename-project/README.md#user-content-rename-gms2-project)


<br>


<!-- TOC -->
## Table of Contents
<kbd></kbd> &nbsp;&nbsp; [Simple Movement](simple-movement/README.md#user-content-simple-movement) <br>
<kbd></kbd> &nbsp;&nbsp; [Simple Movement 8 Directions](simple-8dir/README.md#user-content-simple-movement-8-directions) <br>
<kbd></kbd> &nbsp;&nbsp; [Diagonal Speed Fix](diagonal-speed/README.md#user-content-diagonal-speed-fix) <br>
<kbd></kbd> &nbsp;&nbsp; [Diagonals with 8 Directions](diagonal-8dir/README.md#user-content-diagonals-with-8-directions) <br>
<kbd></kbd> &nbsp;&nbsp; [Player Acceleration](acceleration/README.md#user-content-player-acceleration) <br>
<kbd></kbd> &nbsp;&nbsp; [Player Breaking Friction](breaking-friction/README.md#user-content-player-breaking-friction) <br>
<kbd></kbd> &nbsp;&nbsp; [Animated Turn](animated-turn/README.md#user-content-animated-turn) <br>
<kbd></kbd> &nbsp;&nbsp; [Gamepad](gamepad/README.md#user-content-gamepad) <br>



## Core Algorithm
1. Get Controls
2. Update player phyics 
3. Move and rotate player based on above physics (resolve physics if using speed/hspeed/vspeed automatically happens between step and end step events)
4. Resolve collision -> Decide on final state (walking, running, stopped etc...)
5. Select Animation


<!-- LICENSE -->
## License
Distributed under the MIT License. See `LICENSE` for more information: [link](LICENSE).


</p>
</details>
<details><summary>Dev Tips</summary>
make git m="add commit message"
</details>

