# Lab 6: Stoplight
## Objective

1. Build a circuit using multiple components and a breadboard
2. Write a Python script to light multiple lights and take input from a button or capacitive touch sensor
3. Write a Python script to model a piecewise function by turning the lights off when the sensor detects no light.

## You Will Need

- Raspberry Pi
- Breadboard and T-Cobbler
- 65 $\Omega$ resistor or greater
- 3 LED lights (red, green, and yellow) 
- Male-to-Male Jumper 
- A digital push button or capacitive touch sensor
- Photocell sensor

## Part 1: Python3

1. Create a circuit with 3 LEDs(one green, one red, and one yellow).
2. Create a Python script `led_stoplight.py`  to recreate the following pattern out with your LEDs - Green for 5 seconds, then Yellow for 1 second,  Red for 4 seconds, then it repeats. _Do not use the stoplight sensor, use three individual LEDs._  
	- You will need to import the `GPIO` and `time` libraries for this assignment.
3. Add comments to your Python script to explain how it works.
4. Take a short video of your stoplight working and a clear top-down photo of your wiring

- [ ] Upload `led_stoplight.py`, the video, and the photo to this repository 

## Part 2: Starting with a Button

1. In a new script `button_stoplight.py`, add a button or touch module to your project to start your RGB stoplight. When the button is pressed the light should light up in the green, yellow, red pattern.
2. For your button module, `S` should be connected to a GPIO pin, `V` to 5V, and `G` to ground.
3. In order to use a button, set the `S` pin to an input with `GPIO.setup(pin_number, GPIO.IN)`. It the button is pressed, `GPIO.input(pin_number)` will be equal to 0. If it is unpressed, `GPIO.input(pin_number)` will be equal to 1. See this [resource](https://docs.sunfounder.com/projects/umsk/en/latest/05_raspberry_pi/pi_lesson22_touch_sensor.html) for more information on wiring and the code. 
4. Take a short video of your button starting the stoplight and the pattern appearing correctly.

- [ ] Upload `button_stoplight.py`  and the video to this repository

## Part 3: Starting With a Light Sensor

1. In a new file, `photocell.py`, you will create a program to light all three lights when a photocell sensor detects it is dark. Photocell sensors work the same as buttons when they are set as inputs. The input value will read 1 for light and 0 for dark. 
	1. *Optional Challenge: Use an ADC to get a wider range of input values for your sensor. This will allow you to create a varied response for different amounts of light*
2. When the photocell sensor is covered, light up all three lights. When it is light, turn off all three lights. You can test this but holding your finger over the sensor. 
3. Take a short video of your button starting the stoplight and the pattern appearing correctly.

- [ ] Upload `photocell.py`  and the video to this repository
## Deliverables

- Make sure all the deliverables above are  uploaded to the repository
- Answer the following questions:
	1. What is a Python library and how do you include one in your script?
	2. What does it mean for elements of a circuits to be in series vs. in parallel?
	3. Can you create a circuit of 3 light bulbs in series? Why or why not?
## Rubric 

- 6 points - All required items are present.    
- 5 points - Task was completed, but supplementary materials are weak or missing.    
    - Code is complete, but poorly communicates necessary information
- 4 points - Task was attempted, but is missing major components.    
    - Missing comments, videos/photos, or reflection questions  
- 3 points - Did not attempt or student should reattempt.  
    - Inappropriate use of AI tools.
