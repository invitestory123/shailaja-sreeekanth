# Customer Editing Guide — wax-seal-royale

This wedding invitation is designed with an interactive wax-seal envelope overlay, opening animation video, swan ambient background video, classical soundtrack (*Sita Kalyanam*), live countdown timer, schedule of events, venue details, and gift/attire etiquette.

Configured for: **Shailaja Chakravarthi & Sreekanth Reddy**  
Wedding Date: **November 20, 2026** (Muhurtham: **9:48 AM**)  
Venue: **Ogha Convention, Hyderabad, Telangana**

---

## Normal Customer Changes

All routine customer edits are configured in:
→ [editable/wedding-data.js](editable/wedding-data.js)

### Couple Information
Edit `couple` in `editable/wedding-data.js`:
- `bride` & `groom`: Display names (`"Shailaja"`, `"Sreekanth"`)
- `brideFull` & `groomFull`: Full names (`"Shailaja Chakravarthi"`, `"Sreekanth Reddy"`)
- `order`: Name order (`"bride-first"` or `"groom-first"`)
- `subtitle`: Tagline / subtitle

### Wedding Date & Invitation Note
Edit `wedding` in `editable/wedding-data.js`:
- `dateLabel`: Short date string for hero banner (`"20.11.26"`)
- `dateISO`: Event start ISO timestamp with timezone offset (`"2026-11-20T09:48:00+05:30"`). Directly drives live countdown timer and Google Calendar link.
- `invitationNote`: Main invitation message text (HTML tags like `<br />` and `<strong>` supported)

### Schedule of Events
Edit `schedule` array in `editable/wedding-data.js`:
- Five timed event rows with `title` and `time`:
  - `Guest Arrival` (8:30 AM)
  - `Lagna Muhurtham` (9:48 AM)
  - `Mangalya Dharana` (10:30 AM)
  - `Wedding Feast` (12:30 PM)
  - `Reception` (7:00 PM)

### Venue & Location
Edit `venue` in `editable/wedding-data.js`:
- `name`: Convention / hall name (`"Ogha Convention"`)
- `address`: Full street address
- `mapsUrl`: Google Maps direction URL (`https://maps.app.goo.gl/HPCLiubkX76d3ZFX9?g_st=ic`)

### Etiquette & Notes
Edit `details` in `editable/wedding-data.js`:
- `giftPreference`: Gift preference statement (`"Your presence and heartfelt blessings are our greatest gift."`)
- `dressCode`: Dress code guideline (`"Traditional Indian / Festive Formal"`)

### Media & Assets
Replace files directly in `editable/assets/` or update `media` in `wedding-data.js`:
- `overlayImage`: Wax-seal envelope graphic (`editable/assets/ChatGPT Image Jun 23, 2026, 04_40_29 PM.png`)
- `sealVideo`: Wax-seal breaking/opening MP4 (`editable/assets/1782224012851.mp4`)
- `heroVideo`: Ambient background video (`editable/assets/Swans2.mov`)
- `audio`: Background soundtrack (`editable/assets/sita-kalyanam.mp3`)

---

## Validation
Validate data changes with:
```bash
node --check editable/wedding-data.js
```
