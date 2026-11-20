# KK256A & Digital Fixture DMX Tables (supplement)

!!! note "Note"

    This page is not in the main handout PDF; it comes from the newer digital fixtures & digital consoles handout (數位燈具與數位前級講義.docx) in the folder.


## King Kong-256A (KK256A) digital lighting console

The King Kong series is designed for moving lights and also works with other digital fixtures. It controls up to **256 channels** of DMX512. The panel has a basic operating area, fixture / scene area, function area and programming area, with **no master fader**; its features are an LCD screen and two data wheels handy for moving lights.

### Panel

| Area | Key | Function |
| --- | --- | --- |
| ① Fixture | Fixture | When lit, the basic area addresses fixture channels. 12 fixture pages, up to 32 channels each |
|  | Channel | Channel page; when lit the faders control channels 17–32 |
| ② Scene | Playback page | When lit, the basic area addresses stores. 5 pages of 16 scenes = 80 |
| ③ Basic operation | Unit keys (16) | Shared by fixtures and scenes: select fixtures or stores |
|  | Faders (16) | Shared: change fixture channel values or run stores |
| ④ Function | Record | Store and edit scenes or chases |
|  | Copy / Include | Copy scenes and chases / load data into the programmer |
|  | Delete / Off | Delete fixtures, chase steps, stores and other data |
|  | Time | Edit scene and chase times |
|  | Shape | Call built-in shapes |
|  | Setup | Patch fixtures, edit attributes, language, backup and load, clear console data |
|  | Black out | Flashing = output is zero; press again to restore |
| ⑤ Programming | Exit | Up one level or leave the function |
|  | ↑ / ↓ | Scroll the menu |
|  | Enter | Go down a level, execute or toggle |
|  | Clear | Deselect fixtures, zero dimmer attributes and clear the programmer |
|  | A / B | Choose the upper / lower menu option |
|  | Data wheels A / B | Change the left / right value, or control a moving head's X / Y axis |

### Basic operation

**Controlling fixtures**: with Fixture lit, press the unit keys you want (several allowed) and change channel values with the faders; the values go into the programmer. **There is no flash function for fixtures.**

**Store a scene (single step)**

1. (Press Clear first to avoid storing unwanted data.) Set the look. Only edited values enter the programmer.
2. Press Record → choose &lt;A&gt; single-step scene (the light flashes).
3. Press the playback page (unused stores flash).
4. Press the unit key of the store (the light goes out).

Two storage units: "by fixture" stores all attributes of the fixture; "by channel" stores only changed channels (recommended).

**Store a chase (multi-step scene)** (up to 100 steps)

1. Press Record → choose &lt;B&gt; multi-step scene.
2. Press the playback page → press the store's unit key (the screen shows the store number and current step).
3. Set this step's look (or bring in stored data with Copy / Include).
4. Press Enter to store and move to the next step; repeat (Clear between steps if you wish).
5. When all steps are stored, press Record to save and exit.

**Run a scene or chase**: choose the playback page; a store's unit key is its flash; raise the matching fader to run it, the value being its master level. Up to one page of 16 stores at once.

**Set chase speed**: run the chase → wheel A sets speed (default 1.0 s; more seconds is slower) → wheel B sets crossfade (default FF,FF is maximum) → press &lt;A&gt; to enter settings → press &lt;A&gt; again to save.

**Edit / delete chase steps**: Record → &lt;B&gt; → playback page → store → choose the step with up/down → set the look and press Enter, choosing insert / overwrite / merge; or press Delete to remove the step → press Record to exit.

**Delete a scene / chase**: choose the playback page and press the store's unit key twice. **Delete all**: Setup → next page &lt;B&gt; erase data → &lt;B&gt; clear all playback data → Enter.

## DMX512 tables for digital fixtures

The tri-colour LED's 7-channel (Ch07) mode is in DMX Console & LED PAR.

### Tri-colour LED (3W×36 RGB) — Ch05 mode

| Ch | Function | Value |
| --- | --- | --- |
| 1 | Red | 0–255 |
| 2 | Green | 0–255 |
| 3 | Blue | 0–255 |
| 4 | Strobe | Same as channel 6 of Ch07 mode |
| 5 | Master dimmer | 0–255 |

### Four-colour LED (3W×54 RGBW) — simple modes

| Mode | Ch1 | Ch2 | Ch3 | Ch4 | Ch5 | Ch6 |
| --- | --- | --- | --- | --- | --- | --- |
| ARC.1 | Red | Green | Blue |  |  |  |
| ARC.2 | Red | Green | Blue | White |  |  |
| AR1.d | Dimmer | Red | Green | Blue |  |  |
| AR2.d | Dimmer | Red | Green | Blue | White |  |
| AR2.S | Dimmer | Red | Green | Blue | White | Strobe (0–10 full on; 11–255 slow to fast) |
| HSV | Hue | Saturation | Value |  |  |  |

### Four-colour LED — STAG mode (11 channels)

| Ch | Function | Value | Description |
| --- | --- | --- | --- |
| 1 | Master dimmer | 0–255 | 0–100% |
| 2 | Red | 0–255 | Controls Time when Ch8 selects PR01–10 |
| 3 | Green | 0–255 | Controls Fade when Ch8 selects PR01–10 |
| 4 | Blue | 0–255 |  |
| 5 | White | 0–255 |  |
| 6 | Colour change | 0–5 | No function |
|  |  | 6–20 | High Power (in Normal Power mode) |
|  |  | 21–30 | No function |
|  |  | 31–255 | Colour change (see the colour table) |
| 7 | Strobe | 0–10 | Full on, no strobe |
|  |  | 128–255 | Strobe slow to fast |
| 8 | Colour program | 0–20 | No function |
|  |  | 21–120 | Built-in programs 1–10 (10 values each) |
|  |  | 121–220 | User programs 1–10 (10 values each) |
|  |  | 221–255 | No function |
| 9 | Colour speed | 0–255 | Speed of built-in programs (user programs use Ch2, Ch3) |
| 10 | Dimmer speed | 0–9 | Use the dimmer speed in the SET menu |
|  |  | 10–29 | Off |
|  |  | 30–69 | Speed 1 (fastest) |
|  |  | 70–129 | Speed 2 |
|  |  | 130–189 | Speed 3 |
|  |  | 190–255 | Speed 4 (slowest) |
| 11 | ID address | 0–9 | ID disabled |
|  |  | 10–209 | ID1–ID20 (10 values each) |
|  |  | 210–255 | ID21–ID66 |

### Amber LED (2 channels)

| Ch | Function | Value |
| --- | --- | --- |
| 1 | Strobe | Same as channel 6 of the tri-colour Ch07 mode |
| 2 | Master dimmer | 0–255 |

### Laser (7 channels)

| Ch | Function | Value | Description |
| --- | --- | --- | --- |
| 1 | Mode | 0–49 | Laser off |
|  |  | 50–99 | Sound mode |
|  |  | 100–149 | Auto mode |
|  |  | 150–199 | Static mode |
|  |  | 200–255 | Dynamic mode |
| 2 | Pattern | 0–255 | 52 static / dynamic patterns |
| 3 | X position | 0–255 |  |
| 4 | Y position | 0–255 |  |
| 5 | Scan speed | 0–255 | Fast to slow |
| 6 | Movement speed in dynamic mode | 0–255 | Fast to slow, 10 levels |
| 7 | Pattern size in static mode | 0–255 | Small to large |
