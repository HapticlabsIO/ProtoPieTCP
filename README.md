# ProtoPie TCP
Hapticlabs Studio can interface with Protopie through a TCP (Transmission Control Protocol) connection. The interface allows you to easily keep changing, adding or tweaking tracks in Hapticlabs Studio while building your ProtoPie demo.

## Demo

To run the demo:
1. Open the `ProtoPie-TCP.hptl` file in Hapticlabs Studio.
2. Connect the Satellite.
3. Open ProtoPie Connect.
4. Import `ProtoPie-TCP.pie` in ProtoPie Connect
5. Click "New" > "Local Pie" in the top left corner
6. Run it!




## Connection

Simply open Hapticlabs Studio and then ProtoPie Connect. Hapticlabs will send a confirmation message in ProtoPie Connect when everything is working.

![Screenshot 2023-10-23 at 17 40 43](https://github.com/HapticlabsIO/ProtoPieTCP/assets/34678030/7806bea3-0836-4399-b2ea-aa476c592630)

### Troubleshooting
Sometimes restarting ProtoPie Connect is needed if it was running before Hapticlabs Studio. Also make sure to use either the first or the second server address in ProtoPie Connect.

![image](https://github.com/HapticlabsIO/ProtoPieTCP/assets/34678030/b9cb9a8e-2cc9-40f1-94d2-695ce196be0e)

## Syntax

Anywhere in your ProtoPie, send a message to Hapticlabs Studio to control track playback on the Satellite. 

The message syntax is as follows:
- `StartTrack` with the value `"example track"` to start the track named "example track".
- `SetAmplitudeScale` with value `0.1`. This scales the amplitude of whatever is currently playing to 0.1 (10%), the range is 0.0 to 1.0.
> Make sure to send SetAmplitudeScale after sending StartTrack, as StartTrack will reset the amplitude scale to 1.0 by default.
- `StartTrack` with value `"example track, 0.5"` to start "example track" with amplitude scale 0.5.
- `Stop` will stop whatever is playing.

<img width="1582" alt="Screenshot 2023-10-23 at 17 27 08" src="https://github.com/HapticlabsIO/ProtoPieTCP/assets/34678030/2fe82ac5-6321-4463-9fc2-86e61779491f">
