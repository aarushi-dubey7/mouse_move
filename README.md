# mouse_move

Simple Arduino/PlatformIO project that gently nudges a servo to keep a mouse moving. 
## What it does

The sketch attaches a servo on pin 9, moves it slightly to the right, returns to center, moves it slightly to the left, then returns to center again. After that, it waits before repeating the cycle.

## Hardware

- Arduino Uno
- Servo motor
- External power for the servo if needed
- Common ground between the Arduino and servo power supply

## Wiring

- Signal: pin 9
- Power: servo VCC to 5V or an external 5V supply
- Ground: servo GND to Arduino GND

## Configuration

You can tune the motion in `src/main.cpp`:

- `CENTER_POS` controls the center angle
- `SMALL_MOVE` controls how far the servo nudges left and right
- `MOVE_DELAY` controls how long each movement is held
- `WAIT_TIME` controls the pause between cycles

## Build and upload

From the project folder:

```bash
platformio run
platformio run --target upload
```

If `platformio` is not on your PATH, use the local PlatformIO environment instead.

## Notes

- Start with a small `SMALL_MOVE` value to avoid overdriving the servo.
- If the servo jitters or resets the board, use a separate 5V supply for the servo.
- In the "mouse_move" folder you can see the license and readme for this project, while in the "mouse-move" you can find the code. 
- I used PlatformIO IDE extension in VS code, so there will be files in the "mouse-move" folder to upload code that way. 
