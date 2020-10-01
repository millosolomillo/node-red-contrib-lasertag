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
  - Kill/respawn?
  - Add/substract life. (added)
  - Set ID (added).
  - Set Team_ID (added).


- Weapons system:
  - Damage of each weapon.
  - Active weapon.
  - Type of weapon available for use or not.
  - Silencer? ("Picked up" in a clumn maybe and maybe only temporary or for a fixed amount of bullets).
  - Magazine size before reload for each weapon.
  - Max capacity of bullets for each weapon.
  - Weapons blocked? Can be programmed in this flow or also in player.
  - Automatic, semiautomatic.
  - Rate of firing (rate in automatic and cooldown in semiautomatic).
- 2 Approaches for life points change: Either the amount of life (+ or -) is sent over IR, either only the code for the weapon or medkit.
  

- General for everybody:
  - Configuration of all the clients at the beginning of game at the same time.
  - Log in each player shots received for satistics.
  - Friendly fire switch.

-------------------------------

Extra ideas:
- In the future maybe player and guns could be separated in different systems (guns and player would communicate maybe by BLE/Wifi and get locked when player dies).
- Borrow ammo from colleagues by BLE or IR.
- Ammo box (Heavy box with another RPi with a set amount of ammo for players to take).
- Respawn and reload fixed columns.
- Medkit.
