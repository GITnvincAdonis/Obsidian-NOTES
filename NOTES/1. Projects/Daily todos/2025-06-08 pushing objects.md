---
creation date: <% tp.file.creation_date() %>
---

> [!Danger] Statement of Problem
> 

The character should be able to move an object (push along ground surface) in the cardinal directions:
- North
- South
- East
- West


> [!NOTE] Solution
> 

Move-able objects are assigned rigid-bodies. The character is assigned separate kinematic rigid-body that would affect move-able obstacles.

To limit the obstacle movement to the cardinal directions, the rotation was frozen on all axes. This apparently works.

Link to original: [[2025-06-02 Brainstorm mechanics]]