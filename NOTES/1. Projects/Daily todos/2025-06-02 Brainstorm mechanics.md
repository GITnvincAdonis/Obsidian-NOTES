---
creation date: <% tp.file.creation_date() %>
---
 Mechanics for Isometric 2d game:
- [[2025-06-08 pushing objects]] //
- teleporting //
- Moving Plats //
- Picking up //
- Interrupt jump when collide with object
- stomp//
- Stop listening to inputs when paused (on player)//
- Spikes//
- ray guns //
- alternators (gravity switch) 
- stompable platforms (breakable)//
- stompable platforms (alternator like it activates another part of the plaform, think seasaw)
- crash bandicoot obstacle avoidance level **
- 2d alternator perspective **
- Player Damage //
- toggling platforms (as you travel, they activate, and potential disappear) **
  
3d approach
- Define a grid system for 3d (ray casting to predefined grid and using that coord)
- This will be for the 3d objects
- Take a sprite and pro-grammatically attach it to a 3d mesh
  
  
  ### orrrrr
-  Create the 3 object and sprite prefab. Of course of predefined styles
- Will need to iron out specifically how to properly cover 3d objects with sprite
- It will be predictable, as sprites should be make predictably.
- Mesh joining system
  
  
  
ESSENTIALS:
Game play loop:
- menu
- level select
- pause menu
- settings menu

TODOS:
- Path trails for moving platforms
- Camera shake 
- Hurting player adds an upward force and increases speed
- Ideating stompable alternating platform
- Reseach how ill do world space UI

Link to original: [[2025-06-02 Research about isometric game level design]]