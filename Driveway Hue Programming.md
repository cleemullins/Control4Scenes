# Overview

System Overview
* Current O/S 3.1.3.*
* Current Controller C4 EA5
* Hue Bulbs updated to latest firmware
* Hue v3 Controller (latest)

Relevant Hue Info:
* 6 large physical outdoor lights. Each has multiple Hue Color Candle Color bulbs. 
  * 4 lights on the house (each with 3 color candles)
  * 2 lights at the end of the driveway (each with 4 color candles)
* Keep all lights in sync. Not trying to get fancy via C4. I can do that via Hue if we're having a party. :) 
 
# Front Outdoor Lights 

## C4 View
C4 ViewLoads currently on 2 switches:
* Exterior | Front Entry | Porch Lights (Load) SW1202077
* Exterior | Front Entry | Driveway Lights (Load) SW1202077 
* Main Floor | Kitchen | Front Hallway Keypad is a 6-button keypad dimmer. 

C4 T3 Wall 10  ("Kitchen | T3 10" In-Wall Touch Screen"). 

Hue Lights are added as "Exterior | Front Entry | Driveway Color Lights"
* Driveway Color Lights are bound to Group Address 5. 

Hue Bridge (OS 2.9+) is added as "Other | Control4 Drivers | Hue Bridge"
* Group 5 has Light IDs 14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34

## Hue View
In the Hue app, all bulbs are added to the the room "Garage Doors"

## Desired Behavior
1. Remove Load from switch buttons. 
   * Enable "Double Tap Top" to enable load on each switch
   * Enable "Double Tap Bottom" to disable load on each switch. 

1. Press Up on "Porch Lights" or "Driveway Lights" should:
   * Turn on all Hue Lights in Group 5.
   * Set them to "Bright"
   * LED's on swtichs should follow (top blue, bottom off)

2. Press Down on "Porch Lights" or "Driveway Lights" should: 
   * Turn off all Hue Lights in Group 5 (using Hue. Don't turn off the actual load).
   * LED's on swtich should follow (top off, bottom blue)

3. Timers should 
   * Turn on lights at sunset, turn off at Sunrise. 
   * If lights are on due to the timer, manually turning them off disables the timer for that day. Aka, don't turn them back on. 
   * LEDs on the two switches should update. 

4. Front Hallway Keypad 
   * Button 2 should 
    * If the electrical loads are off, turn them on. 
    * Press should Restore Preset Scene #1 on "Driveway Color Lights". LED should be lit both on the keypad on on the switches. 
    * Hold for 3 seconds should save current Hue Scene as Scene 1. 
       * Should flash the LED for 3 seconds to reflect it did something. 
     
   * Button 3 should 
     * If the electrical loads are off, turn them on. 
     * Press should Restore Preset Scene #2 "Driveway Color Lights". LED should be lit. LED should be lit both on the keypad on on the switches. 
     * Hold for 3 seconds should save current Hue Scene as Scene 2. 
       * Should flash the LED for 3 seconds to reflect it did something. 
   
5. T3 10" Touch Screen 
    * Add a Color Wheel, controlling the exterior light colors. Not sure which one. Let's discuss.