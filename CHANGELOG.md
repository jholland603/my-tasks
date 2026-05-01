# My Tasks — Changelog

## v1.37
- Fixed: renderMobile was calling deleted dueDotClass() function, silently killing all mobile task rendering
- Mobile tasks now render correctly in portrait mode
- Bumped mobile breakpoint to 1024px to catch more devices
- Added !important to mobile CSS show/hide rules to prevent override
- Overdue tasks now show red text on mobile too

## v1.36
- Section counts now reflect active Work/Personal/All filter
- Removed confusing "2 / 3" format from Today count — now shows plain number like all other sections

## v1.35
- Overdue rows now have a light red background
- All text, checkbox border, and type dot turn red for overdue tasks
- Hover state stays in the red family for visual consistency

## v1.34
- Added rebalanceSections() on load — moves every task to correct section based on current due date
- Tasks due tomorrow now correctly appear in Tomorrow section
- Removed colored dots (red/green/yellow) from due date column
- Overdue rows turn red instead of just the date field

## v1.33
- Added Tomorrow section — due exactly tomorrow
- Renamed This Week → 7 Days (due in 2–7 days)
- Renamed Next Week → 14 Days (due in 8–14 days)
- Backwards compatible — old week/nextweek keys in tasks.json migrate automatically
- Section dot colors: Today=red, Tomorrow=orange, 7 Days=blue, 14 Days=purple, Backlog=green

## v1.32
- Date fields are now read-only — typing disabled
- Click a date to open native date picker only
- Eliminates mid-edit section jumping bug

## v1.31
- Fixed: DOM only rebuilds when task actually moves to a different section
- Deferred render with setTimeout to let blur event complete first

## v1.30
- Auto-place now triggers on blur instead of change
- Prevents task from moving while user is still editing the date

## v1.29
- Fixed timezone bug — todayISO() now uses local date instead of UTC
- Fixes tasks due tomorrow appearing in Today for users behind UTC

## v1.28
- Work type dot changed to burgundy (#8b1a2e)
- Work filter button changed to burgundy to match
- Better visual separation from green Personal color

## v1.27
- Fixed: sortState missing section key caused sections to not render
- loadSortState() now merges saved state with defaults to ensure all sections present

## v1.26
- Fixed: wireDates used stale closure reference to sec after task moved
- Now dynamically finds task's current section before all operations

## v1.25
- Added Next Week section (due in 8–14 days, purple dot)
- autoPlaceTask() moves task to correct section when due date changes
- rebalanceSections() runs on load to place all tasks correctly

## v1.24
- Moved Notes column before Due date
- Moved Created date after Due date
- New column order: Company · Description · URL · Notes · Due · Created

## v1.23
- Fixed: cursor now goes to Description for new personal tasks
- Added missing placeCaretAtEnd helper function

## v1.22
- Fixed: duplicate companyInput declaration broke entire script
- Fixed: setup screen buttons non-functional due to parse error

## v1.21
- Company field disabled and greyed out for personal tasks
- Toggling type dot enables/disables company field live

## v1.20
- New tasks inherit type from active filter
- Personal filter creates personal task; Work or All creates work task

## v1.19
- Fixed: type dot now inline with description text
- Work/Personal filter buttons colored to match their dots

## v1.18
- Added Work / Personal / All filter buttons
- Colored type dot next to each description (burgundy=work, green=personal)
- Click dot to toggle task type
- Mobile detail panel shows task type

## v1.16
- New tasks default due date to 7 days from created date

## v1.15
- Added search/filter bar filtering all sections at once
- Matched text highlights in yellow with result count
- Added Clean up completed — delete tasks older than X days

## v1.14
- Company ID column now bold on desktop and mobile

## v1.13
- Description shows full text as tooltip on hover

## v1.12
- Fixed: mobile CSS ordering bug causing sections to be hidden in portrait
- Bumped mobile breakpoint to 900px

## v1.11
- Added mobile-friendly layout for screens under 900px
- Compact list view with tap-to-expand details
- Added version number to footer

## v1.10
- Sort preferences saved to GitHub as settings.json
- Sort state syncs across all devices

## v1.9
- Sort preferences saved to localStorage per device

## v1.8
- Company, Created, Due columns sortable
- Click header to cycle ascending → descending → manual
- Each section has independent sort state

## v1.7
- Fixed: drag only activates from ⠿ handle
- Within-section row reordering works reliably

## v1.6
- Due date color dots added
- Tasks due today auto-promote to Today section on load

## v1.5
- Wider table layout
- Date picker icon visible
- Browser tab favicon added

## v1.4
- Notes column with modal editor
- Notes button highlights when note exists

## v1.3
- Created and Due date columns
- Drag and drop between sections

## v1.2
- Removed Task column — Description is primary field
- Company field is combobox from existing companies

## v1.1
- Column headers and table layout
- Single-line rows with URL as clickable link

## v1.0
- Initial build: Today, This Week, Backlog sections
- GitHub API sync to tasks.json
- Completed tasks section
- GitHub token setup screen
