# Lighting controls

Panda Control Vent treats the vent LEDs and relocated chamber LEDs as separate
zones. Open **Lighting** in the controller interface to configure either zone.
Link the zones when both should use the vent-light settings, or unlink them to
give each zone its own brightness, colours, effects, and print-progress display.

## Printer states

Set **Color follows** to **Printer status** to use separate colours for Idle,
Preparing, Printing, Paused, Completed, and Error. Each normal state can be
steady or flashing. Error retains its dedicated colour and flash control.

The chamber zone can also:

- dim while the printer is idle;
- follow the X1C factory chamber-light setting;
- use its own settings independently of the vent-light zone.

## Print progress

Enable **Show print progress** to turn the active LEDs into a progress bar while
the printer reports that a job is printing. The bar fills from the opposite end
of the strip. Whole LEDs represent the reported print percentage.

With **Alternate displays** disabled, the progress bar remains visible for the
whole Printing state. With it enabled, the zone alternates between:

1. the print-progress bar; and
2. the effect selected in the **Effect** list.

Use the **Switch every** slider to choose how long each display remains visible.
The range is 1–30 seconds and the default is 3 seconds. Vent and chamber zones
can use different intervals when they are unlinked.

Progress starts a new cycle whenever printing begins or resumes. Paused,
Completed, and Error states take priority over the progress display. If the
printer has not supplied a valid percentage, the normal selected effect remains
visible.

## Saving and upgrades

Select **Save lighting** after making changes. Lighting settings are stored on
the controller and survive normal OTA updates. Firmware from before the progress
controls keeps its existing lighting configuration; the new progress controls
start disabled and the interval defaults to 3 seconds.
