# Medical Shift Planner

A comprehensive web-based shift planning application designed for medical facilities to manage staff schedules, leave periods, and transport crew assignments. Features bilingual support (English/Polish) for international medical teams.

## 🚀 Quick Start

1. Open `calendar_assignment_new.html` in your browser
2. Click **"Manage Staff"** to add your team members
3. Click **"Manage Leave"** to add any leave periods
4. Click **"Assign Shifts"** to configure transports and auto-assign monthly shifts
5. Click any day to manually edit or review assignments
6. Use **📊 Availability**, **🔄 Shift Swap**, and **📈 Stats** for advanced features
7. Click **🖨️ Print** to print the calendar with color-coded shifts

## Features Overview

**13+ Major Features** including shift management, staff tracking, leave management, swap system, availability calendar, work statistics, and more!

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
- **Local Storage**: All data persisted in browser localStorage (staff, assignments, leave, transport config, language preference, swap requests)
- **Export Data**: Export all staff, assignments, leave records, transport configuration, and swap requests to JSON
- **Import Data**: Import previously exported JSON files
- **Data Persistence**: No data loss on browser refresh

### 🖨️ Print-Friendly Calendar
- **Print Button**: Dedicated print button with printer icon (🖨️)
- **Optimized Layout**: Landscape orientation for better calendar viewing
- **Color-Coded Printing**: 
  - Day shifts (blue), Night shifts (yellow), Control room (purple)
  - Ambulances (red), Medical transports (green)
  - Weekends (gray), Headers (dark gray)
- **Print Legend**: Automatic legend showing shift type colors
- **Background Graphics**: Instructions for enabling colors in browser print dialog
- **Compact Design**: Optimized fonts and spacing for paper
- **No Clutter**: Hides buttons and controls when printing

### 🔄 Shift Swap Management
- **Swap Requests**: Create formal shift swap requests between staff members
- **Date Range Filter**: Filter shifts by date range (default: next 30 days)
- **Swap Approval System**:
  - Submit swap requests with optional reason
  - Approve/Reject requests
  - Automatic shift exchange upon approval
- **Request Status Tracking**:
  - Pending (orange border)
  - Approved (green background)
  - Rejected (red background)
- **Complete Swap Details**: Shows who wants which shift in exchange for what
- **History Management**: View all requests, filter by status, delete old requests
- **Smart Shift Selection**: Dropdowns automatically load all shifts for selected staff within date range

### 📊 Staff Availability Calendar
- **Grid View**: Matrix showing all staff and all days of the month
- **Color-Coded Status**:
  - 🟢 Green: Available (not scheduled, not on leave)
  - 🟡 Yellow with ✓: Scheduled for a shift
  - 🔴 Red with ✗: On leave
  - Gray: Weekend days
- **Sticky Headers**: Staff names and dates stay visible when scrolling
- **Month Navigation**: Browse any month to see availability
- **Smart Filtering**:
  - All Staff
  - Available Only (staff with free days)
  - Unavailable Only (staff fully booked/on leave)
- **Hover Details**: Tooltips show shift details when hovering over cells
- **Quick Planning**: See at a glance who's free for assignments

### 📈 Work Statistics & Reports
- **Statistics Dashboard**: Comprehensive work hour and shift tracking
- **Summary Cards**:
  - Total shifts across all staff
  - Total hours worked
  - Average shifts per staff member
  - Average hours per staff member
- **Detailed Breakdown**:
  - Day shifts count per person
  - Night shifts count per person
  - Control room shifts count per person
  - Transport assignments count per person
  - Total days worked (unique days)
  - Total hours worked (12h for day/night/control, 8h for transport)
- **Smart Sorting**:
  - By name (A-Z)
  - By days worked (high to low or low to high)
  - By hours worked (high to low or low to high)
- **Search & Filter**: Real-time search by staff name
- **CSV Export**: Download complete statistics report for Excel
- **Month Navigation**: View statistics for any month
- **Workload Analysis**: Identify over/under-worked staff members

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

### Printing Calendar
1. Navigate to the month you want to print
2. Apply any filters if needed (specific staff or shift type)
3. Click **"🖨️ Print"** button
4. Read the alert about enabling background graphics
5. In print dialog:
   - Enable "Background graphics" or "Print backgrounds"
   - Orientation is automatically set to landscape
6. Print or save as PDF

### Shift Swapping
1. Click **"🔄 Shift Swap"** button
2. Set date range filter (defaults to next 30 days)
3. Select requesting staff member
4. Choose their shift to swap from dropdown
5. Select swap partner staff member
6. Choose which shift they'll take in exchange
7. Add optional reason
8. Click **"Submit Swap Request"**
9. View all requests in the list below
10. Approve/Reject pending requests
11. Filter by status: All/Pending/Approved/Rejected

### Viewing Staff Availability
1. Click **"📊 Availability"** button
2. See grid with all staff and their availability
3. Navigate months with Previous/Next buttons
4. Use filter dropdown to show:
   - All Staff
   - Available Only (staff with free days)
   - Unavailable Only (completely booked)
5. Hover over cells for shift details
6. Green = available, Yellow = scheduled, Red = on leave

### Viewing Work Statistics
1. Click **"📈 Stats"** button
2. View summary cards showing totals and averages
3. Navigate months to see different periods
4. Use search box to find specific staff
5. Sort by name, days, or hours using dropdown
6. Click **"📥 Export to CSV"** to download report
7. Table shows:
   - Day/Night/Control/Transport shift counts
   - Total days worked per person
   - Total hours worked per person

### Export/Import
- **Export**: Click "Export Data" to download a JSON file with all data (includes swap requests)
- **Import**: Click "Import Data" and select a previously exported JSON file
- Use for backup, sharing, or transferring data between browsers

## Technical Details

### Data Storage
All data is stored in browser localStorage:
- `people`: Staff members and their details
- `assignments`: Daily shift assignments
- `leaveRecords`: Leave periods
- `transportsConfig`: Ambulance and medical transport counts (separate limits per type)
- `swapRequests`: Shift swap requests with status tracking
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
  "transportsConfig": {...},
  "swapRequests": [...]
}
```

### Hours Calculation
Work statistics calculate hours based on:
- **Day Shift**: 12 hours
- **Night Shift**: 12 hours
- **Control Room**: 12 hours
- **Transport**: 8 hours (average)

## Tips & Best Practices

1. **Regular Backups**: Export your data regularly to avoid data loss
2. **Transport Configuration**: Set separate limits for ambulances and medical transports before auto-assigning shifts
3. **Leave First**: Add leave periods before auto-assigning shifts
4. **Review Auto-Assignments**: Always review and adjust auto-assigned shifts as needed
5. **Language Preference**: Select your preferred language (EN/PL) - it will be remembered for future sessions
6. **Browser Storage**: Remember that data is browser-specific - export to move between browsers
7. **Scrolling**: Use scroll within calendar day cells to view all assignments when multiple shifts are assigned
8. **Print Colors**: Enable "Background graphics" in your browser's print settings to see color-coded shifts
9. **Date Range Filtering**: Use the date range filter in shift swap to focus on upcoming shifts only
10. **Availability Check**: Use the Availability Calendar before assigning shifts to see who's free
11. **Statistics Review**: Check work statistics monthly to ensure fair workload distribution
12. **CSV Reports**: Export statistics to CSV for payroll or management reporting
13. **Swap Requests**: Encourage staff to use the swap system for better tracking and approval workflow

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

### Print Colors Not Showing
- Ensure "Background graphics" is enabled in print settings
- Chrome/Edge: Click "More settings" → Enable "Background graphics"
- Firefox: Under "Appearance" → Check "Print backgrounds"
- Safari: In print dialog → Check "Print backgrounds"

### Statistics Not Accurate
- Verify all shifts are properly saved
- Check that month/year is correct
- Transport shifts count as 8 hours each
- Day/Night/Control shifts count as 12 hours each

### Shift Swap Date Range Empty
- Ensure staff members have shifts assigned in the selected date range
- Try clearing date range filter to see all shifts
- Check that assignments exist for the current/future months

## Recent Updates

### Version 3.0 Features (Latest)
- ✅ **Print-Friendly Calendar**: Optimized printing with color-coded shifts and legend
- ✅ **Shift Swap System**: Complete swap request and approval workflow with date filtering
- ✅ **Staff Availability Calendar**: Visual grid showing availability status for all staff
- ✅ **Work Statistics Dashboard**: Comprehensive tracking of days and hours worked per employee
- ✅ **CSV Export**: Download statistics reports for external analysis
- ✅ **Enhanced Data Persistence**: Swap requests included in export/import

### Version 2.0 Features
- ✅ **Bilingual Support**: Complete English/Polish translation system
- ✅ **Separate Transport Types**: Distinct ambulance and medical transport management
- ✅ **Type-specific Limits**: Independent limits for each transport vehicle type
- ✅ **Improved UI**: Better spacing, sticky date numbers, optimized modal layering
- ✅ **Enhanced Calendar**: Scrollable cells with better text layout
- ✅ **Localized Dates**: Month and day names in selected language

## Feature Highlights

### 🆕 New in Version 3.0
1. **Print Calendar** (🖨️): Professional print layout with color legend
2. **Shift Swap** (🔄): Formal request/approval system with date range filtering
3. **Availability Grid** (📊): Visual matrix of staff availability across entire month
4. **Work Statistics** (📈): Automatic calculation of days and hours per staff member
5. **CSV Export**: Download statistical reports for payroll and management

## Future Enhancements

Potential improvements for future versions:
- Additional language support (German, Spanish, etc.)
- Role-based assignment rules (e.g., senior staff required for certain shifts)
- Conflict detection and warnings
- Multi-month view
- Mobile responsive design improvements
- Cloud storage integration
- Email notifications for shift swaps
- Custom shift hour configuration
- PDF export for schedules

## License

This project is provided as-is for medical facility shift planning purposes.

## Support

For issues or questions, refer to the built-in test functionality or check browser console for error messages.
