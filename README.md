# Campus Life Planner

Campus Life Planner is an application designed to help students organize assignments, study sessions, projects, and other academic activities.

## 1. Key Features

* Add, edit, and delete activities.
* Search, sort, and view activities.
* Dashboard statistics.
* View upcoming activities and their due dates.
* Organize activities using tags, such as assignment, study, project, and personal.
* Customize application appearance using Light, Dark, and System themes.
* Configure notifications, including due date reminders and daily summaries.
* Import and export activities as JSON files for backup and restoration.

## 2. Data Model

Each activity follows this data structure:

interface Activity {
  id: string;
  title: string;
  dueDate: string;    
  duration: number;     
  tag: string;          
  createdAt: string;
  updatedAt: string;
}

## 3. Accessibility Plan

### 3.1 Keyboard Navigation

* All features must be accessible using Tab, Shift+Tab, Enter, and arrow keys where appropriate.
* Maintain a logical focus order throughout the application.
* Ensure that forms, navigation, dialogs, tables, and action menus are keyboard accessible.

### 3.2 Visible Focus

* Provide clear focus indicators, such as a blue outline, for all interactive elements.
* Ensure focus indicators have sufficient contrast against their backgrounds.
* Do not remove browser focus styles without providing an accessible replacement.

### 3.3 Accessible Labels

* Every form control must have a clear, visible label.
* Use appropriate accessible names for icon-only buttons.
* Associate labels and validation messages with their corresponding controls.
* Provide accessible names for search fields, navigation items, and activity actions.

### 3.4 Error Messages

* Display clear, descriptive error messages when user input is invalid or an operation fails.
* Associate error messages with the relevant form fields.
* Make errors programmatically identifiable to assistive technologies.
* Provide useful feedback for failed imports, invalid JSON files, and unsuccessful save operations.

### 3.5 Skip Link

* Add a **"Skip to main content"** link at the top of the page.
* Allow keyboard users to bypass repetitive navigation and move directly to the main content area.

### 3.6 Screen Reader Announcements

* Use appropriate ARIA live regions for dynamic updates.
* Announce important events, including:

  * Successful activity creation or updates.
  * Activity deletion.
  * Successful JSON import or export.
  * Form validation errors.
  * Search results updates when necessary.
* Avoid unnecessary announcements that interrupt the user's workflow.

## 4. Responsive Design

* Support desktop and mobile screen sizes.
* Use a sidebar layout on desktop and a compact bottom navigation layout on mobile.
* Present activity records in a table on desktop and cards on mobile.
* Ensure forms, buttons, filters, and settings remain usable on small screens.
* Provide touch-friendly controls and readable text.
* Prevent horizontal overflow and maintain consistent spacing.

## 5. User Experience

* Provide a personalized greeting on the dashboard.
* Use clear visual indicators for activity categories.
* Highlight upcoming deadlines and completed activities.
* Display helpful empty states when no activities are available.
* Confirm destructive actions, such as deleting an activity.
* Provide clear success and error feedback for user actions.
* Preserve user preferences when appropriate.

## 6. Data Management

* Store activity information using a suitable persistence mechanism.
* Support JSON export for backups.
* Validate imported JSON files before modifying existing data.
* Handle invalid files and import errors gracefully.
* Preserve activity fields, including identifiers, dates, durations, tags, and timestamps, during import and export.

## 7. Project Structure

campus-life-planner/
├── index.html
├── assets/
├── scripts/
├── styles/
├── tests/
├── README.md
└── .gitignore

