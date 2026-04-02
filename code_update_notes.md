# Code Update Notes

## 2026-03-29

### Safety logic update

#### Files changed
- `bt_hid.h`
- `bt_hid.c`
- `main_app.c`

#### Main changes
- Added a new function declaration in `bt_hid.h` for checking the time since the most recent controller report
- Added tracking of the most recent HID report time in `bt_hid.c`
- Updated the Bluetooth input handling code so the report timestamp is refreshed whenever a new controller report is received
- Added a function in `bt_hid.c` to measure how long it has been since the last controller report
- Updated `main_app.c` to add a timeout-based safety check during motion
- Limited the timeout-based stop condition so it only applies when the robot is currently being commanded to move
- Kept the original disconnect-based stop behavior from the older code

#### New logic added
- A timestamp is now stored whenever a new HID controller report is received
- The code can now measure the elapsed time since the last valid controller update
- If controller reports stop updating for longer than the timeout period while the robot is still moving, the motors are forced to stop
- Normal idle state is not treated as a fault condition
