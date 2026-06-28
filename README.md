# swsh Event Intelligence

A demo tool that connects to a swsh album and uses AI vision to automatically detect sponsor logos, crowd energy, and merch in every fan photo — then writes structured labels back to each photo via the swsh API.

Built on the [swsh Public API](https://dev-docs.joinswsh.com) as part of a job application to swsh.

## What it does

- Fetches photos from a swsh album via `/album/getPhotos`
- Sends each photo to Claude vision for analysis (sponsor logos, crowd energy, merch, viral potential)
- Writes AI-generated labels back to each photo via `/photo/addPhotoLabel`
- Tracks stats: photos analyzed, labels written, sponsor detections

## How to run

**Demo mode** (no API key needed)
1. Open `swsh-event-intelligence.html` in any browser
2. Click "Demo mode"
3. Optionally add brand context (e.g. "Sponsors: Nike, Red Bull")
4. Click "Run demo analysis"

**Live API mode**
1. Create a swsh account and generate an API key from [developer settings](https://www.joinswsh.com/settings?modal=DeveloperSettings)
2. Open the tool, enter your API key and album ID
3. Click "Fetch album and analyze photos"

> Live API mode requires a swsh API key and a Claude API key (set in the fetch call). Demo mode works out of the box.

## Stack

- Vanilla HTML/CSS/JS — no framework, no build step
- [swsh Public API](https://dev-docs.joinswsh.com) for album and photo label management
- Claude vision API (`claude-sonnet-4-6`) for image analysis

## Built by

[Ayesha Dawodi](https://ayeshadawodi.me)
