# My Tasks — Changelog

## v1.23
- Fixed: cursor now goes to Description (not Company) for new personal tasks
- Fixed: added missing `placeCaretAtEnd` helper function

## v1.22
- Fixed: duplicate `companyInput` declaration was breaking entire script
- Fixed: setup screen buttons (token, save) were non-functional due to parse error

## v1.21
- Company field disabled and greyed out for personal tasks
- Existing company data preserved but dimmed when task is personal
- Toggling type dot enables/disables company field live

## v1.20
- New tasks now inherit type from active filter (Personal filter → personal task)
- All or Work filter selected → defaults to work type

## v1.19
- Fixed: type dot now inline with description text (flexbox alignment)
- Work/Personal filter buttons colored to match their dot colors (blue/green)

## v1.18
- Added Work / Personal / All filter buttons next to search bar
- Added colored type dot next to each description (blue = work, green = personal)
- Click dot to toggle task between work and personal
- New tasks default to Work type
- Mobile detail panel shows task type

## v1.17 (skipped — intermediate)

## v1.16
- New tasks default due date to 7 days from created date

## v1.15
- Added search/filter bar — filters all sections at once as you type
- Search matches company, description, notes, and URL
- Matched text highlights in yellow
- Added result count display
- Added "Clean up completed" — delete completed tasks older than X days

## v1.14
- Company ID column now bold on desktop and mobile

## v1.13
- Description cell shows full text as native tooltip on hover
- Tooltip updates live as you type

## v1.12
- Fixed: mobile layout CSS ordering bug — sections were hidden in portrait mode
- Bumped mobile breakpoint to 900px to cover more devices

## v1.11
- Added mobile-friendly layout for screens under 900px
- Compact list view: checkbox, Company, Description, due dot per row
- Tap to expand: reveals URL, dates, notes, and action buttons
- Added version number to footer

## v1.10
- Sort preferences now saved to GitHub as settings.json
- Sort state syncs across all devices

## v1.9
- Sort preferences saved to localStorage (per device)

## v1.8
- Company, Created, Due columns now sortable
- Click header to cycle: ascending → descending → manual
- Each section has independent sort state
- Dragging to reorder switches section back to manual sort
- Fixed: sort listeners were duplicating on each render (event delegation)

## v1.7
- Fixed: drag-and-drop now only activates from the ⠿ handle
- Within-section row reordering now works reliably
- Drop indicator (dark line) shows insertion point
- Default sort by Due then Created on load

## v1.6
- Added due date color dots: red (overdue), green (today), yellow (within 2 days)
- Dot updates immediately when due date changes
- Tasks due today auto-promote to Today section on load

## v1.5
- Made table wider (1400px max)
- URL column significantly wider
- Date picker icon now visible and clickable
- Added browser tab favicon (✅ emoji)

## v1.4
- Added Notes column — click ✎ to open free-form text editor
- Notes modal with save, Escape to close, Ctrl+Enter shortcut
- ✎ button highlights blue when a note exists
- Fixed: notes modal HTML moved before script tag to fix null addEventListener error

## v1.3
- Added Created date column (defaults to today)
- Added Due date column (defaults to 7 days from created)
- Overdue dates shown in red
- Added drag-and-drop between sections

## v1.2
- Removed Task column — Description now serves as primary task name
- Company field is now a combobox dropdown populated from existing companies
- Focus on new task goes to Company field

## v1.1
- Added column headers: Company, Description, URL, Created, Due
- Single-line rows with truncation
- URL shows as clickable link, pencil icon to edit
- Rebuilt as table layout

## v1.0
- Initial build: three-section task tracker (Today, This Week, Backlog)
- GitHub API sync — tasks saved to tasks.json in your repo
- Completed tasks section — tasks move there on check, uncheck to restore
- Drag and drop between sections
- Setup screen with GitHub token and repo name
- Token show/hide toggle for mobile paste
- Whitespace stripping on token input
