have added Web MIDI API hardware controller support to bohlen_pierce_accordion.html:
​Header MIDI Status Pill & Collapsible Routing Drawer: Displays a live MIDI activity LED and connected device count/name, expanding to configure the active MIDI input port, rescan devices, shift the base root (C2, C3, C4), and monitor incoming notes and CCs.
​Three Hardware Note-Mapping Modes:
​1. Direct 1-to-1 BP Steps: Maps sequential MIDI keys linearly across the Bohlen-Pierce scale without octave jumps.
​2. 2-Row Split (Even / Odd): Splits lower keys (< C4) to the outer pearl row and upper keys (>= C4) to the inner obsidian row.
​3. MIDI Accordion Mode: Routes MIDI Channels 1–2 to the right-hand dichromatic treble reeds and MIDI Channel 3 to the left-hand Stradella bass and coupled BP chord buttons.
​Bellows CC, Velocity, Sustain & Register Control: Supports velocity-sensitive reed dynamics, CC #64 sustain pedal, CC #1 (Mod Wheel) / CC #2 (Breath) / CC #11 (Expression) / Channel Aftertouch for real-time 3D bellows pressure pumping, and MIDI Program Change messages to switch reed register stops.
