# Blacksmithing Game
Intention here is to create the mini-game I want to implement in my RPG roguelite for blacksmithing. I want something skill-based to create a crafting system that rewards skill over grinding.

## Gameplay Loop
- Purify Ore into Ingots with the furnace
- Shape the ingots
- Finish the piece (Sharpen, Oil)

## Implementation
- Cell = 96 x 96 block
- The cell is broken into a 3 x 3 grid (32 x 32)
- Striking the cell will reduce it's thickness and duplicate it in the surrounding location based on where on the grid is struck
    - Example: Striking on 1,2 will create a half thickness duplicate directly to the right of the cell
- Cell attributes
    - Thickness
    - Temperature
- An Ingot is a 3 x 6 block of cells
    - Ingots can be manibulated by striking the cells to move material around
    