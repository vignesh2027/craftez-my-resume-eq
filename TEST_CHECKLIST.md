# CMR Resume Builder - QA Testing Checklist

## Test Environment
- [ ] Browser: Chrome, Firefox, Safari, Edge
- [ ] Devices: Desktop, Tablet, Mobile
- [ ] Network: Online and Offline modes
- [ ] Cache: Cleared before testing
- [ ] Console: Open to catch errors

---

## Core Features Testing

### 1. Landing Page (`/`)
- [ ] Header loads with navigation
- [ ] Hero section displays correctly
- [ ] Feature highlights visible
- [ ] Statistics section shows
- [ ] Resume examples section loads
- [ ] Templates gallery renders
- [ ] CTA buttons redirect correctly
- [ ] Mobile responsive layout

### 2. Resume Builder (`/form`)
- [ ] Page loads without errors
- [ ] All tabs accessible (Personal, Experience, Education, Skills, Additional, Cover Letter)
- [ ] Sidebar displays correctly
- [ ] Form inputs accept data
- [ ] Preview pane updates in real-time

### 3. Cover Letter Builder (`/cover`)
- [ ] Form fields load
- [ ] Preview updates on input
- [ ] Can switch back to resume
- [ ] Data persists when switching tabs

---

## Template Testing

### Template Loading
- [ ] Modern template loads
- [ ] Classic template loads
- [ ] Elegant template loads
- [ ] Creative templates load (all 18)
- [ ] ATS templates load (all 12)
- [ ] Professional templates load (all 8)
- [ ] Tech templates load (all 8)
- [ ] Corporate templates load (all 3)
- [ ] International templates load (all 8)
- [ ] Fallback works if template missing
- [ ] Template switching is smooth
- [ ] No 404 errors in console

### Template Customization
- [ ] Color picker works (8 colors)
- [ ] Font selector works (4 options)
- [ ] Changes apply in real-time
- [ ] Customization persists on refresh

---

## Advanced Analysis Testing

### Analyze Resume Button
- [ ] Button is clickable
- [ ] Modal opens without errors
- [ ] Analysis card displays:
  - [ ] Overall Score
  - [ ] Power Keywords count
  - [ ] AI Detection percentage
  - [ ] Metrics found count
- [ ] Recommendations display correctly
- [ ] Keyword badges show detected words
- [ ] Modal can be closed

### Analysis Accuracy
- [ ] Power keywords counted correctly (led, managed, increased, etc.)
- [ ] Weak keywords detected (responsible for, worked on, etc.)
- [ ] Quantifiable metrics found ($, %, numbers)
- [ ] AI detection score calculates
- [ ] Recommendations are relevant
- [ ] Score matches content quality

---

## ATS Optimizer Testing

### Score Calculation
- [ ] Score initializes at 0
- [ ] Score updates when data added
- [ ] Full name adds points
- [ ] Email/phone add points
- [ ] Professional summary adds points
- [ ] Experience adds points (more = higher)
- [ ] Education adds points
- [ ] Skills add points
- [ ] Max score is 100

### Score Display
- [ ] Score shows in circle
- [ ] Color changes: poor → fair → good → excellent
- [ ] Tips update dynamically
- [ ] At least 3 tips show when incomplete
- [ ] "Excellent" message shows when complete

### ATS Mode
- [ ] Toggle button works
- [ ] ATS-friendly template loads
- [ ] Regular templates can't be selected in ATS mode
- [ ] Can turn off ATS mode
- [ ] Resume looks clean and readable

---

## Data Management Testing

### Auto-Save
- [ ] Data saves every 5 seconds
- [ ] Save indicator appears briefly
- [ ] Data persists on page refresh
- [ ] Saved data loads on return visit
- [ ] 7-day expiration works

### Export/Import
- [ ] Export button generates JSON file
- [ ] Exported file contains all resume data
- [ ] Import button opens file picker
- [ ] Imported data loads correctly
- [ ] All fields populated from import
- [ ] Can edit imported data

### Sample Data
- [ ] TCS sample loads completely
- [ ] Infosys sample loads completely
- [ ] Zoho sample loads completely
- [ ] Samples have realistic content
- [ ] Can edit sample data

### Clear Draft
- [ ] Clear button shows confirmation
- [ ] Canceling keeps data
- [ ] Confirming clears all data
- [ ] Page reloads after clear
- [ ] All fields empty after clear

---

## Form Functionality Testing

### Personal Information
- [ ] Full Name field required
- [ ] Email field validates email format
- [ ] Phone field accepts formats
- [ ] Location field optional
- [ ] LinkedIn URL optional
- [ ] Summary field accepts long text
- [ ] Photo upload works
- [ ] Photo preview displays

### Experience
- [ ] Add Experience button works
- [ ] Multiple experiences addable
- [ ] Job title, company, dates required
- [ ] Description accepts multiline text
- [ ] Remove button deletes entry
- [ ] Entries persist on save
- [ ] Dates format correctly

### Education
- [ ] Add Education button works
- [ ] Degree field required
- [ ] School field required
- [ ] Year field works
- [ ] Multiple education entries work
- [ ] Remove button works
- [ ] Entries persist

### Skills
- [ ] Technical skills comma-separated
- [ ] Soft skills comma-separated
- [ ] Languages with proficiency accepted
- [ ] Multiple skills parse correctly
- [ ] Skills display as badges in preview

### Additional Sections
- [ ] Certifications accept multiline
- [ ] Projects accept multiline
- [ ] Awards accept multiline
- [ ] Volunteer work accepts multiline

---

## Preview Functionality Testing

### Preview Display
- [ ] Preview updates on every input change
- [ ] Preview shows all resume sections
- [ ] Formatting looks professional
- [ ] Mobile preview responsive
- [ ] Preview scrollable if long
- [ ] Print preview works (Ctrl+P)

### Preview Performance
- [ ] Updates don't lag (debounce working)
- [ ] Large resumes still preview smoothly
- [ ] Template switching fast (< 1 second)
- [ ] No memory leaks on long sessions

---

## Offline Testing

### Offline Mode
- [ ] Offline indicator appears when offline
- [ ] Form still works offline
- [ ] Data saves offline
- [ ] Can't download PDF offline
- [ ] Data syncs back online
- [ ] No error messages

### Network Recovery
- [ ] Works when connection restored
- [ ] Saved data intact after disconnect
- [ ] No duplicate saves on reconnect

---

## Download/Export Testing

### PDF Download
- [ ] Download button works
- [ ] PDF generates from current template
- [ ] Filename includes name/date
- [ ] Formatting matches preview
- [ ] All content included
- [ ] File size reasonable (< 2MB)
- [ ] Opens in PDF reader

---

## UI/UX Testing

### Navigation
- [ ] All navigation links work
- [ ] Active tab highlights correctly
- [ ] Tab switching smooth
- [ ] Can navigate via URL
- [ ] Breadcrumbs clear (if present)

### Responsive Design
- [ ] Desktop layout (1920px): Sidebar + Preview side-by-side
- [ ] Tablet layout (768px): Stacked or grid layout
- [ ] Mobile layout (375px): Single column, scrollable
- [ ] Touch targets adequate (44x44px minimum)
- [ ] No horizontal scrolling on mobile

### Accessibility
- [ ] Keyboard navigation works (Tab, Enter)
- [ ] Form labels properly associated
- [ ] Color contrast adequate (WCAG AA)
- [ ] Alt text on all images
- [ ] ARIA labels where needed
- [ ] Works with screen readers (basic test)

### Theme Switching
- [ ] Light mode displays correctly
- [ ] Dark mode displays correctly
- [ ] Toggle button works
- [ ] Theme persists on refresh
- [ ] All text readable in both themes
- [ ] Contrast adequate in both modes

### Language Support
- [ ] English translations complete
- [ ] Tamil translations complete
- [ ] Hindi translations complete
- [ ] Language switch works
- [ ] RTL languages display correctly (if added)

---

## Error Handling Testing

### Error Scenarios
- [ ] Invalid email format shows error
- [ ] Missing required fields blocked
- [ ] Large file upload rejected
- [ ] Network error handled gracefully
- [ ] Template missing shows fallback
- [ ] Corrupted data shows warning
- [ ] Invalid import file rejected
- [ ] Storage quota exceeded handled

### Console Errors
- [ ] No JavaScript errors
- [ ] No 404 errors (except intentional)
- [ ] No console warnings
- [ ] Network requests successful
- [ ] API calls (if any) successful

---

## Browser Specific Testing

### Chrome
- [ ] All features work
- [ ] DevTools shows no errors
- [ ] Performance good (< 3s load)

### Firefox
- [ ] All features work
- [ ] No compatibility issues
- [ ] Storage working

### Safari
- [ ] All features work
- [ ] iOS version works
- [ ] Storage working

### Edge
- [ ] All features work
- [ ] No compatibility issues

---

## Performance Testing

### Load Time
- [ ] Initial load: < 2 seconds
- [ ] Time to Interactive: < 3 seconds
- [ ] Page Speed Insights: > 80

### Runtime Performance
- [ ] No jank (60fps scrolling)
- [ ] Form input responsive
- [ ] Template switching smooth
- [ ] No memory leaks (DevTools check)

### Storage
- [ ] Cache working (F12 > Application > Cache)
- [ ] LocalStorage using reasonable space
- [ ] Old data cleanup working

---

## Security Testing

### Data Privacy
- [ ] No sensitive data in URLs
- [ ] No credentials in console
- [ ] HTTPS enforced (on Vercel)
- [ ] No XSS vulnerabilities
- [ ] Input sanitization working
- [ ] CORS headers correct

### File Upload
- [ ] Only images accepted for photo
- [ ] File size limited
- [ ] No executable files allowed
- [ ] File type validation

---

## Deployment Verification

### Vercel Deployment
- [ ] Site deploys without errors
- [ ] Environment variables set correctly
- [ ] Build logs clean
- [ ] No failed deployments
- [ ] Deployment preview works
- [ ] Production domain accessible

### DNS & Routing
- [ ] Domain resolves correctly
- [ ] All routes accessible (`/`, `/form`, `/cover`, `/tech`)
- [ ] Redirects work properly
- [ ] 404 page shows for invalid routes
- [ ] Sitemap accessible (`/sitemap.xml`)

---

## Post-Deployment Testing

### User Acceptance Testing
- [ ] User can complete full resume
- [ ] User can download PDF
- [ ] User can share/export
- [ ] User experience smooth
- [ ] No blockers or crashes
- [ ] Features as advertised

### Analytics (if enabled)
- [ ] Page views tracked
- [ ] User interactions tracked
- [ ] Conversion events logged
- [ ] No tracking errors

---

## Sign-Off

| Tester | Date | Status | Notes |
|--------|------|--------|-------|
| | | | |
| | | | |
| | | | |

**Overall Status:** [ ] PASS [ ] FAIL

**Known Issues:** (List any bugs found)
1. 
2. 
3. 

**Sign-Off Date:** ________________
