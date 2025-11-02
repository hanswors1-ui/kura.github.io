# Medical Shift Planner

A comprehensive web-based shift planning application designed for medical facilities to manage staff schedules, leave periods, and transport crew assignments. Features bilingual support (English/Polish) for international medical teams.

## Features

### 🌍 Multilingual Support
- **English/Polish Interface**: Toggle between English and Polish with one click
- **Complete Translation**: All UI elements, labels, buttons, and role names translated
- **Persistent Preference**: Language choice saved in browser
- **Localized Dates**: Month and day names displayed in selected language
- **Dynamic Updates**: Calendar and all content refresh instantly on language change

### 📅 Calendar Management
- **Interactive Monthly Calendar**: Visual month-by-month calendar view with easy navigation
- **Color-coded Shifts**: Different colors for day shifts, night shifts, control room, ambulances, and medical transports
- **Today Indicator**: Current date highlighted for easy reference
- **Weekend Highlighting**: Weekends visually distinguished from weekdays
- **Scrollable Day Cells**: Each calendar day cell supports scrolling when content exceeds available space
- **Sticky Date Numbers**: Date numbers remain visible at top when scrolling through assignments
- **Optimized Layout**: Improved spacing prevents text overlap and ensures readability

### 👥 Staff Management
- **Multi-role Support**: Staff can have multiple roles including:
  - Doctor
  - Driver
  - Medic Senior
  - Medic Trainee
  - Transport
  - Nightshift
  - Dayshift
  - Control Room
- **Employment Types**: Track permanent and contractor staff
- **Staff Preferences**:
  - Maximum shifts per week (1-7)
  - Minimum rest days between shifts (0-3)
  - Weekdays-only option (exclude from weekend shifts)
- **Staff Search**: Quick search functionality by name or role
- **Edit/Remove**: Modify or remove staff members as needed

### 🗓️ Leave Management
- **Leave Types**: Support for vacation, sick leave, training, and other leave types
- **Date Ranges**: Define leave periods with start and end dates
- **Notes**: Add optional notes to leave records
- **Current & Upcoming View**: Automatically filters to show only current and future leave
- **Delete Functionality**: Remove outdated or incorrect leave entries

### 📋 Shift Assignment
- **Auto-Assignment**: Intelligent algorithm for monthly shift distribution
- **Fair Distribution**: Balances workload across all staff members
- **Constraint Handling**:
  - Respects maximum shifts per week
  - Ensures minimum rest days between shifts
  - Honors weekdays-only preferences
  - Checks for leave periods
- **Transport Configuration**: Set the number of ambulances and medical transports available per day
- **Separate Transport Types**: Distinct buttons for adding ambulance vs. medical transport crews

### ✏️ Daily Shift Editing
- **Click-to-Edit**: Click any calendar day to edit assignments
- **Manual Adjustments**: Override auto-assignments as needed
- **Shift Types**:
  - Day Shift
  - Night Shift
  - Control Room
  - Transport Crews (Ambulance and Medical Transport)
- **Transport Crew Management**:
  - Add separate ambulance or medical transport crews via dedicated buttons
  - Assign Doctor, Medic, and Driver for each crew
  - Remove crews as needed
  - Respects daily transport limits (enforced per vehicle type)
  - Scrollable transport list for longer assignments
- **Modal Interface**: Clean, organized modal dialogs with proper layering (no overlapping elements)

### 🔍 Filtering & View Options
- **Staff Filter**: View shifts for a specific staff member
- **Shift Type Filter**: Filter by day shifts, night shifts, control room, or transports
- **Visual Indication**: Filtered results highlighted in the calendar
- **Clear Filters**: Easy one-click filter reset

### 💾 Data Management
- **Local Storage**: All data persisted in browser localStorage (staff, assignments, leave, transport config, language preference)
- **Export Data**: Export all staff, assignments, leave records, and transport configuration to JSON
- **Import Data**: Import previously exported JSON files
- **Data Persistence**: No data loss on browser refresh

## How to Use

### Getting Started
1. Open `calendar_assignment_new.html` in a modern web browser (Chrome, Firefox, Edge, Safari)
2. No server or installation required - runs entirely in the browser
3. Click **EN/PL** button in top right to switch between English and Polish interface

### Adding Staff
1. Click **"Manage Staff"** button
2. Fill in staff details:
   - Name
   - Employment type (Permanent/Contractor)
   - Select applicable roles
   - Set availability preferences
   - Optional: Check "Weekdays only" for staff who don't work weekends
3. Click **"Add Staff Member"**
4. Use the search box to quickly find staff members

### Managing Leave
1. Click **"Manage Leave"** button
2. Select staff member from dropdown
3. Choose leave type
4. Set start and end dates
5. Add optional notes
6. Click **"Add Leave"**
7. Delete leave records by clicking the "Delete" button on each entry

### Configuring Transports
1. Click **"Assign Shifts"** button
2. Set the number of ambulances available per day
3. Set the number of medical transports available per day
4. Click **"Save transports"**
5. These limits will be enforced when adding transport crews manually or via auto-assignment

### Auto-Assigning Shifts
1. Navigate to the desired month using Previous/Next Month buttons
2. Click **"Assign Shifts"**
3. Configure transport numbers if not already set
4. Click **"Auto-Assign Shifts for Current Month"**
5. The algorithm will:
   - Assign day and night shifts to clinical staff
   - Distribute shifts fairly
   - Respect all constraints (leave, rest days, preferences)
   - Assign control room staff
   - Create transport crew assignments based on configured limits

### Manual Editing
1. Click any day in the calendar
2. Select or change staff for each shift type
3. Add transport crews:
   - Click **"Add Ambulance Crew"** to add an ambulance (shows as red badge in calendar)
   - Click **"Add Medical Transport"** to add a medical transport (shows as green badge in calendar)
   - Select Doctor, Medic, and Driver from dropdowns for each crew
   - The system will prevent adding more crews than the configured daily limits
   - Each transport type has its own limit (e.g., 2 ambulances + 3 medical transports per day)
4. Click **"Remove"** to delete a transport crew
5. Click **"Save Changes"**
6. Transport crew roles (Doctor/Medic/Driver) display in selected language

### Filtering View
1. Click **"Filter View"** button
2. Select a staff member to see only their shifts
3. Or select a shift type to see only those shifts
4. Click **"Apply Filter"**
5. Filtered calendar cells are highlighted in blue
6. Click **"Clear Filter"** to reset

### Export/Import
- **Export**: Click "Export Data" to download a JSON file with all data
- **Import**: Click "Import Data" and select a previously exported JSON file
- Use for backup, sharing, or transferring data between browsers

## Technical Details

### Data Storage
All data is stored in browser localStorage:
- `people`: Staff members and their details
- `assignments`: Daily shift assignments
- `leaveRecords`: Leave periods
- `transportsConfig`: Ambulance and medical transport counts (separate limits per type)
- `language`: User's preferred interface language (en/pl)

### Browser Compatibility
- Modern browsers with localStorage support
- JavaScript must be enabled
- No external dependencies or libraries required

### Data Format
Export files are JSON format containing:
```json
{
  "people": [...],
  "assignments": {...},
  "leaveRecords": [...],
  "transportsConfig": {...}
}
```

## Tips & Best Practices

1. **Regular Backups**: Export your data regularly to avoid data loss
2. **Transport Configuration**: Set separate limits for ambulances and medical transports before auto-assigning shifts
3. **Leave First**: Add leave periods before auto-assigning shifts
4. **Review Auto-Assignments**: Always review and adjust auto-assigned shifts as needed
5. **Language Preference**: Select your preferred language (EN/PL) - it will be remembered for future sessions
6. **Browser Storage**: Remember that data is browser-specific - export to move between browsers
7. **Scrolling**: Use scroll within calendar day cells to view all assignments when multiple shifts are assigned

## Troubleshooting

### Shifts Not Assigning
- Ensure you have at least 2 clinical staff members (Doctor, Medic Senior, or Medic Trainee)
- Check that staff are not all on leave
- Verify staff preferences allow assignments (e.g., not all weekdays-only on weekends)

### Transport Crews Limited
- Check configured transport limits in "Assign Shifts" modal
- Ensure limits are saved by clicking "Save transports"
- Maximum crews per day is enforced based on configuration
- Ambulance and medical transport limits are tracked separately
- Error messages will indicate which vehicle type limit has been reached

### Data Lost After Closing Browser
- Check if browser is in private/incognito mode (localStorage doesn't persist)
- Verify browser allows localStorage
- Export data regularly as backup

### Calendar Not Updating
- Click on calendar days to refresh view
- Use Previous/Next Month buttons to re-render calendar
- Refresh browser page if issues persist

## Recent Updates

### Version 2.0 Features
- ✅ **Bilingual Support**: Complete English/Polish translation system
- ✅ **Separate Transport Types**: Distinct ambulance and medical transport management
- ✅ **Type-specific Limits**: Independent limits for each transport vehicle type
- ✅ **Improved UI**: Better spacing, sticky date numbers, optimized modal layering
- ✅ **Enhanced Calendar**: Scrollable cells with better text layout
- ✅ **Localized Dates**: Month and day names in selected language

## Future Enhancements

Potential improvements for future versions:
- Additional language support (German, Spanish, etc.)
- Role-based assignment rules (e.g., senior staff required for certain shifts)
- Conflict detection and warnings
- Multi-month view
- Print-friendly calendar format
- Shift swap functionality
- Staff availability calendar
- Mobile responsive design improvements
- Cloud storage integration

## License

This project is provided as-is for medical facility shift planning purposes.

## Support

For issues or questions, refer to the built-in test functionality or check browser console for error messages.
