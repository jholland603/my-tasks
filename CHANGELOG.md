# My Day — Changelog

## v1.47
- Live weather from Open-Meteo (free, no API key, CORS-friendly)
- Current conditions update icon, temperature, and description
- 5-day forecast renders dynamically from real data
- Detail popup now includes rainfall amount (inches) and High/Low temp
- Weather refreshes every 30 minutes automatically
- Weather timestamp shows source and last updated time

## v1.46
- Page title and header changed from "My Tasks" to "My Day"
- "My Day" header is now larger and more prominent
- "My Tasks" label moved to just above the task sections in smaller italic text
- Fixed: deleting a ticker no longer wipes prices from remaining symbols
- Removed duplicate SPY entry from default tickers
- Browser tab title updated to "My Day"

## v1.45
- Fixed: DEFAULT_tickers reference error (case typo from sed replace)

## v1.44
- Ticker symbols are now fully manageable — add and remove at will
- Add row below market grid: type symbol + optional label, press Enter or click + Add
- Hover a ticker to reveal × remove button
- Ticker list persists in settings.json and syncs across devices
- Enter key support for ticker inputs

## v1.43
- Added Favorite Links collapsible panel below dashboard
- Add links with URL + optional label (domain used as fallback)
- Remove links by hovering chip and clicking ×
- Links sync across all devices via settings.json
- Enter key support for link inputs

## v1.42
- Added 5-day weather forecast to weather widget (hardcoded, replaced in v1.47)
- Click any forecast day to open detail modal (condition, high, precip, wind, humidity)
- Added SPY and TSLA to default market tickers
- Fixed initDashboard function wrapper that was accidentally dropped

## v1.41
- Switched from Yahoo Finance to Finnhub for live market data (CORS-compliant)
- Finnhub API key stored in localStorage, entered via ⚙ settings screen
- Prompts user to enter key if not set
- Added Finnhub key field to existing settings overlay

## v1.40
- Live market data via Yahoo Finance (later replaced by Finnhub in v1.41)
- Clock now shows full date: weekday, month, day, year
- Markets refresh every 5 minutes with last-updated timestamp

## v1.39
- Added dashboard bar: clock widget, weather widget, markets widget
- Clock updates every second with AM/PM
- Weather widget shows current conditions (hardcoded Rochester NH, replaced in v1.47)
- Markets show S&P 500, Dow, Nasdaq, Bitcoin, Gold (static data, replaced in v1.40)

## v1.38
- Fixed: new tasks always added to the clicked section regardless of default due date
- Auto-placement only triggers when due date is changed after creation
- Fixed due date calculation to use local time instead of UTC

## v1.37
- Fixed: renderMobile was calling deleted dueDotClass() causing silent failure
- Mobile tasks now render correctly in portrait mode
- Bumped mobile breakpoint to 1024px
- Added !important to mobile CSS show/hide rules
- Overdue tasks show red text on mobile

## v1.36
- Section counts now reflect active Work/Personal/All filter
- Removed confusing "x / 3" format from Today count

## v1.35
- Overdue rows have light red background
- All text, checkbox, and type dot turn red for overdue tasks

## v1.34
- Added rebalanceSections() — moves tasks to correct section on load
- Removed colored dots from due date column
- Overdue row text turns red

## v1.33
- Added Tomorrow section
- Renamed This Week → 7 Days, Next Week → 14 Days
- Old week/nextweek keys migrate automatically

## v1.32
- Date fields read-only — click to open native date picker only

## v1.31
- DOM only rebuilds when task actually moves section
- Deferred render with setTimeout

## v1.30
- Auto-place triggers on blur, not change
- Prevents mid-edit section jumping

## v1.29
- Fixed timezone bug in todayISO() — now uses local date

## v1.28
- Work type dot and button changed to burgundy

## v1.27
- Fixed sortState missing section key on load
- Merges saved state with defaults to ensure all sections present

## v1.26
- Fixed wireDates stale closure reference after task moved

## v1.25
- Added Next Week section (due 8–14 days)
- autoPlaceTask() moves task on due date change

## v1.24
- Reordered columns: Company · Description · URL · Notes · Due · Created

## v1.23
- Fixed focus going to Description for personal tasks
- Added placeCaretAtEnd helper

## v1.22
- Fixed duplicate companyInput declaration breaking entire script

## v1.21
- Company field disabled for personal tasks

## v1.20
- New tasks inherit type from active filter

## v1.19
- Fixed type dot alignment inline with description
- Filter button colors match dot colors

## v1.18
- Added Work / Personal / All filter buttons
- Type dot next to description (burgundy=work, green=personal)
- Click dot to toggle type

## v1.16
- New tasks default due date to 7 days out

## v1.15
- Search bar filters all sections at once
- Matched text highlights yellow
- Clean up completed — delete tasks older than X days

## v1.14
- Company column now bold

## v1.13
- Description tooltip on hover

## v1.12
- Fixed mobile CSS ordering bug
- Bumped breakpoint to 900px

## v1.11
- Mobile layout for screens under 900px
- Compact list with tap-to-expand

## v1.10
- Sort preferences synced to GitHub via settings.json

## v1.9
- Sort preferences saved to localStorage

## v1.8
- Sortable columns: Company, Due, Created
- Independent sort state per section

## v1.7
- Drag only from ⠿ handle
- Within-section reordering works

## v1.6
- Due date color dots
- Tasks due today auto-promote to Today on load

## v1.5
- Wider table, date picker visible, favicon added

## v1.4
- Notes column with modal editor

## v1.3
- Created and Due date columns, drag between sections

## v1.2
- Description as primary field, company combobox

## v1.1
- Column headers, table layout, clickable URLs

## v1.0
- Initial build: Today, This Week, Backlog
- GitHub sync, completed section, token setup
