# node-red-contrib-lasertag
Set of flows to create your own Raspberry Pi lasertag game using Node-RED.

![System Structure](/images/Lasertag_System_Structure.svg)

![Player Flow](/images/player_flow.JPG)


Features/functionalities draft:
- Player properties:
  - Type (human, “grenade”, referee, etc).
  - Is alive?
  - Quantity of life (added).
  - ID (added).
  - Team_ID (added).
- Functions:
  - Kill/respawn.
  - Add/substract life. (added)
  - Set ID (added).
  - Set Team_ID (added).


- Weapons system:



- General for everybody:

-------------------------------
Extra ideas:
- In the future maybe player and guns could be separated in different systems (guns and player would communicate maybe by BLE/Wifi and get locked when player dies).
- Borrow ammo from colleagues by BLE or IR.
- Ammo box (Heavy box with another RPi with a set amount of ammo for players to take).
- Respawn and reload fixed columns.