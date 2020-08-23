# Goal
Add the 20 Hue Color Candle Lights into the Control4 system. Setup the basic on/off as described, where load it always on and bulbs are controlled via programming. The 20 lights should be kept in sync, and a color wheel added to the T3 Touchscreens to allow others to easily set the lighting colors. 

Basic sunrise/sunset timer should be in place. 

Using a 6-button keypad, two buttons (#2, #3) are used to recall Hue Scenes. Those same buttons are "held" to "Save" a current scene (that was set via the Hue App) for future recall. 

Any advanced scenes setup or execution (music sync, party lights, etc) will be controlled directly via one of the native Hue Apps. 

# System Overview
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
Loads are currently on 2 switches:
* Exterior | Front Entry | Porch Lights (Load) SW1202077
* Exterior | Front Entry | Driveway Lights (Load) SW1202077 

In addition, there's a 6-button keypad that has 2 buttons that should be used to save/recall preset scenes.
* Main Floor | Kitchen | Front Hallway Keypad (Buttons #2, #3)

C4 T3 Wall 10  
* Kitchen | T3 10" In-Wall Touch Screen 
* Needs a suitable colorwheel added. 

Hue Lights are added as "Exterior | Front Entry | Driveway Color Lights"
* Driveway Color Lights are bound to Group Address 5 on the Hue Bridge. 

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