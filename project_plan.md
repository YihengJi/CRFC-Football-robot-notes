# Project Status and Next Steps

Updated September 2026. This replaces the early-build checklist; dated observations remain in the [build log](build_log.md).

## Completed work documented here

- Built and flashed Pico W starter firmware.
- Made a wooden test base and assembled the drive hardware.
- Performed motion tests and investigated reverse drift.
- Added and compiled report-timing/timeout logic; full validation against the original incident was not completed.
- Tested suspected wiring faults and investigated a low-battery connection problem.
- Transferred components to a plastic chassis and addressed fit and wiring issues.
- Recorded development observations and photographs.

## Subsequent course extension

The Spring 2026 EE-454 project migrated the platform to ESP32 and added three VL53L0X sensors, boost mode and fixed-distance stopping during boost. See the [ESP32 implementation](https://github.com/YihengJi/EE454-ESP32-Robot-Final-Project).

## Unresolved questions

- Root cause of the original continued-turning incident.
- Full evaluation of the Pico W timeout under controlled stale-report conditions.
- Quantitative stopping distance and sensing/control delay.
- Reproducibility of the Pico W build from files available here.

## Possible follow-up work

Recover and preserve the original firmware revision and dependency versions; develop repeatable fault cases; measure stopping behavior; compare fixed-distance and speed-aware rules; improve wiring access and strain relief.

## Separate senior design

The planned vision-guided quarterback is separate from this build record. Yiheng Ji's assigned area is vision and AI; implementation has not begun as of September 2026. Target detection/localization remain planned capabilities.
