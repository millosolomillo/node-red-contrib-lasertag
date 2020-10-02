# Laser tag game with Raspberry Pi + Node-RED + LIRC // WORK IN PROGRESS
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
  - Silencer? ("Picked up" in a column maybe and maybe only temporary or for a fixed amount of bullets).
  - Magazine size before reload for each weapon.
  - Max capacity of bullets for each weapon.
  - Weapons blocked? Can be programmed in this flow or also in player.
  - Automatic, semiautomatic.
  - Rate of firing (rate in automatic and cooldown in semiautomatic).
- 2 Approaches for life points change: Either the amount of life (+ or -) is sent over IR, either only the code for the weapon or medkit.
  

- General for everybody:
  - Configuration of all the clients at the beginning of game at the same time.
  - Log in each player shots received for satistics. Also log corrupted IR packages (due to collisions?)
  - Friendly fire switch.
  
- Flows should be standard for any type of "player" (human, grenade, referee, medkit, etc.) so the programming is always the same.
  In this way, type of "player" could be changed in configuration.

-------------------------------

Extra ideas:
- In the future maybe player and guns could be separated in different systems (guns and player would communicate maybe by BLE/Wifi and get locked when player dies).
- Borrow ammo from colleagues by BLE or IR.
- Ammo box (Heavy box with another RPi with a set amount of ammo for players to take).
- Respawn and reload fixed columns.
- Medkit.

Biggest problem to overcome (at least for me):
- LIRC for infrared commands, pain in the ass. I can only send predefined characters.
  I cannot or do not know how to stream data. So the solution I see is build my message and send the characters independently, the consequence is that I will have to build a checksum system to avoid corrupt data (could happen if 2 players shoot at the same time or from the sunlight?).
