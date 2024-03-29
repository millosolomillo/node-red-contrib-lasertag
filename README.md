# Laser tag game with Raspberry Pi + Node-RED + Infrared // WORK IN PROGRESS
Set of flows to create your own Raspberry Pi lasertag game using Node-RED.

**System structure:**

![System Structure](/images/Lasertag_System_Structure.svg)

**Player flow:**

![Player Flow](/images/player_flow.JPG)

**Simulator flow:**

![Simulator Flow](/images/simulator_flow.JPG)

**Display flow:**

![Display Flow](/images/display_flow.JPG)


Features/functionalities draft:
- Player properties:
  - Type (human, “grenade”, referee, etc). (Not yet implemented)
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

~~Biggest problem to overcome (at least for me):~~
~~- LIRC for infrared commands, pain in the ass. I can only send predefined characters.
  I cannot or do not know how to stream data. So the solution I see is build my message and send the characters independently, the consequence is that I will have to build a checksum system to avoid corrupt data (could happen if 2 players shoot at the same time or from the sunlight?).~~
- LIRC not needed anymore: Infrared commands will be sent through a NE555 infrared emitter connected to the serial Tx pin and received through a Vishay TSDP34138 receiver connected to the Rx pin.
 
 
## Donation:
If you find this project of worth, please consider donating:

[![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://www.paypal.com/donate?hosted_button_id=KX3R5RWAAZY7U)

[![Donate](https://img.shields.io/badge/Donate-Tikkie_\(only_Netherlands\)-blueviolet.svg)](https://tikkie.me/pay/6n5tmg73reri1lrorlov) - If Tikkie does not work, please consider Paypal.
