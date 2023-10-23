# ProtoPie TCP
ProtoPie Demo highlighting the TCP connection with Hapticlabs Studio. It triggers playback in the Hapticlabs Studio through TCP so the Satellite can remain connected to the Studio, this means you can keep easily changing, adding or tweaking tracks while building your ProtoPie demo.

## Demo

To run the demo:
1. Open the `ProtoPie-TCP.hptl` file in Hapticlabs Studi0.
2. Connect your Satellite.
3. Open ProtoPie Connect.
4. Import `ProtoPie-TCP.pie` in ProtoPie Connect; "New" > "Local Pie" in the top left corner.
5. Run it!

## Connection

Simply open Hapticlabs Studio and ProtoPie Connect. Hapticlabs should send a confirmation message in ProtoPie Connect when it is connected.
![Screenshot 2023-10-23 at 17 40 43](https://github.com/HapticlabsIO/ProtoPieTCP/assets/34678030/7806bea3-0836-4399-b2ea-aa476c592630)

## Syntax

Anywhere in your ProtoPie, send a message to ProtoPie Studio to control track playback on the Satellite. 

The message syntax is as follows:
- `StartTrack` with value `"example track"` to start the track named "example track".
- `SetAmplitudeScale` with value `0.1`. This scales the amplitude of whatever is currently playing to 0.1 (10%), the range is 0.0 to 1.0.
> Make sure to send SetAmplitudeScale after sending StartTrack, as StartTrack will reset the amplitude scale to 1.0 by default.
- `StartTrack` with value `"example track, 0.5"` to start "example track" with amplitude scale 0.5.
- `Stop`, this will stop whatever is playing.

<img width="1582" alt="Screenshot 2023-10-23 at 17 27 08" src="https://github.com/HapticlabsIO/ProtoPieTCP/assets/34678030/2fe82ac5-6321-4463-9fc2-86e61779491f">
