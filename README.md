# Ministry & Bible Reading Tracker

The offical documenation for the mobile app for tracking ministry service hours and Bible reading progress called "Read & Preach".

## Features

### Report (Bericht)
- Weekly calendar view with day-by-day navigation (swipe left/right between weeks)
- **Monthly Summary** showing total hours and total placements for the current month
- **Ministry Service** entry fields:
  - Actual Hours (Tatsächliche Stunden)
  - Planned Hours (Geplante Stunden)
  - Placements/Deliveries (Abgaben)
  - Bible Studies (Bibelstudien)
- Notes field (Bemerkungen) for daily remarks

### Bible Reading (Bibel)
- Tracks progress across all 1,189 Bible chapters
- Circular progress indicator with percentage completion
- Estimated completion date based on reading pace
- **Today's Reading** section highlighting the chapters scheduled for the day (dynamically sized, scrollable when many chapters)
- Long-press any chapter button to open it directly on JW.org
- Book list with per-book completion percentage
- Chapter grid with visual status indicators:
  - **Blue with checkmark** — completed chapters
  - **Green outline** — today's assigned chapters
  - **Gray** — unread chapters
- Quick-tap chapter marking directly from the grid

#### Bible Reading Plans
- **Sequential** — Genesis to Revelation (default)
- **New Testament → Old Testament** — New Testament first, then Old Testament
- **Custom Order** — Drag-and-drop editor to reorder all 66 books
- **Free Mode** — No daily schedule; chapters are still tracked freely
- Duration: 1 year, 2 years, 3 years, or Custom (chapters per day, max 10)
- "Generate Plan" and "Recalculate" with confirmation dialogs
- Setup prompt shown when no plan has been configured yet

### Memorial Bible Reading Tracker
- Dedicated tracker for the annual Memorial of Christ's death preparation
- Full reading schedule covering ~10 days before and after the Memorial (Nisan 14)
- Passages grouped by day with sunrise / after-sunset time blocks and Nisan day labels
- Includes relevant Bible passages and corresponding chapters from *Jesus — The Way, the Truth, the Life*
- Individual check-off per passage; overall progress counter ("X of Y passages read")
- Automatic yearly reset based on the dynamically calculated Memorial date
- **Memorial reading card** in the daily Bible tab during the memorial season:
  - Shows today's entries plus any unread entries from previous days
  - Check-off and direct JW.org link button per entry
- All Bible passage links open with the correct verse range on JW.org (e.g. `bible=43011055-43012001`)
- *Jesus — The Way* chapter links open the correct chapter on JW.org

### Settings (Einstellungen)
- **General**
  - Language selection
  - Haptic feedback toggle
  - App icon selection (Default, Green, Gold, Purple, Red)
  - Export & Import data (ministry reports, Bible reading progress, memorial reading progress)
  - Developer Mode for permanent deletion of past entries

- **Report Settings**
  - Configurable date format with live preview
  - Recurring role assignment (Publisher, Auxiliary Pioneer, Regular Pioneer) with start/end month
  - One-time monthly pioneer assignments
  - Role history log

- **Bible Reading Settings**
  - Bible language selection (defaults to app language; used for JW.org links)
  - Reading plan: mode, duration, and book order editor
  - Daily Reminder: push notification at a chosen time with today's chapter info

- **Memorial Tracker Settings**
  - Enable / disable the Memorial Tracker
  - Always Show toggle (when off, tracker appears 7 days before the Memorial and hides once all passages are read)
  - Memorial Reminder: individual timed notifications for each schedule day

## Localisation

The app is fully localised in:
- 🇬🇧 English
- 🇩🇪 German (Deutsch)
- 🇫🇷 French (Français)
