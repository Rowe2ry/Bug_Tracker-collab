# Outline : Rough Draft V1.0.0

## Idea: <span style="color: #00FFFF;">Bug Tracker — web application</span>

An application for users to call or email a company when they have a problem using a good, service, or product. Customer service representatives can create job tickets with a case number, a description of the issue, and a status (case created, needs review, reviewed-contact customer, unresolved-noted, and resolved). We could invent a fake company like the marketing company "Horiseon" from the first homework and skin the project to the fake brand. Using variables in the styling sheet, we can make the application easy to reskin to the brand identities of potential employers by using colors, fonts, and logos from their websites prior to submitting the project portfolio to a specific employer.

These applications exist all over, and we aren't trying to build one robust enough to sell as a working solution (we would not be competitive). More so to show recruiters and employers our collaboration skills, vision, aim, and technical execution of the baseline MVP (minimum viable product) of this type of application.

All features below are being considered critical and *required for the MVP* unless they are marked with "<span style="color: #8888FF;">*Nice to have.*</span>"

## <span style="color: #FFFF00;">Authentication / Permissions/ Security:<span>

### <span style="color: #00FFFF;">Users</span>

* Ability to Create an account for themselves

* Ability to submit a complaint form to open a new case

* Ability to view a "My Account" page  
    1. Change/Update user's contact info
    2. View all cases associated to the user's account (past and present) as a list of links
    3. <span style="color: #8888FF;">*Nice to have:*</span> Ability to upload a user photo
    4. <span style="color: #8888FF;">*Nice to have:*</span> Ability to set a viewing preference for the site (i.e. light mode and dark mode)

* Ability to view a summary page for each case associated to their account  (active and inactive)
    1. Case Status
    2. Truncated version of activity log (date case was created etc.)
    3. Contact rep about case
    4. Add user-notes to the case ticket.

### <span style="color: #00FFFF;">Customer Service Reps (C.S.R)</span>

* Ability to create a case number upon reviewing a complaint form from a user (this would also assign the C.S.R. to that particular case)

* Ability to add internal (to the company) notes to the case ticket (not visible by users)

* Ability to change the status of a Case (created, awaiting customer response, flagged-needs review, closed-unresolved, closed-resolved)

* Ability to assign tags or keywords to help the company find similar cases for statistics and pattern tracking.

* Ability to contact users for technical support

* Ability to flag specialists within the company that a case needs review.

### <span style="color: #00FFFF;">Internal Specialists</span>

* ability to review cases flagged for inspection (view case pages)

* ability to leave internal notes (not visible to users)

* ability to un-flag that a case needs review and notify a C.S.R. that it has been
reviewed and is ready to be handled by the C.S.R. again.
### <span style="color: #00FFFF;">Moderators</span>

* Ability to modify any part of a case ticket, including deletion, reassigning new case numbers, or merging 2 existing cases.

* Ability to create accounts for C.S.R.s and Internal Specialists

* Ability to initialize a reset of a user's password (including C.S.R. and Internal Specialist)

### <span style="color: #00FFFF;">Administrator</span>
* Full application control - all permissions for all other account types above
* Ability to creat new accounts for moderators

## <span style="color: #FFFF00;">Pages:</span>

All pages listed below should have a uniform header and footer and similar styling in the central portion of the screen. They will link to a common stylesheet which can be updated to new band color and assets to easily "reskin" the application.

### <span style="color: #00FFFF;">Home Page</span>

Basic page with site navigation, a hero image, a brief description of the brand adopting the site.  
* Conditional formatting asking users to sign in or create an account (if not signed in already)
* Signed in users have the ability to:  
    1. report an issue (this files a "complaint" to be reviewed by a C.S.R. to create a job ticket)
    2. view "My account"
    3. Check status of open cases
    4. Links to leave a Google review

### <span style="color: #00FFFF;">Create an Account</span>

For users to access any features besides viewing an "About Us" or "Contact Us" page, they will create an account on a "create an account" page that houses a blank form.  
* Username (text input)
* Email address (text input)
* Phone Number (text input)
* First Name (text input)
* Last Name (text input)
* Date of Birth (not required) (text input)
* Password (text input)
* Re-enter password (text input)
* checkbox (I acknowledge that in order to receive technical support, I am agreeing to receiving emails, calls texts, etc.)
* register button

Upon completing the form, the page will display "An email has been sent to you for verification. Please verify your email before proceeding."

### <span style="color: #00FFFF;">Log In Page</span>

Just a simple page

* Email (text input)
* Password (text input)
* <span style="color: #8888FF;">*Nice to have:*</span> Captcha human verification after 3 failed log-in attempts.
* "I forgot my password" button (can just flag a moderator that this user needs assistance in resetting or just display a message for the user to call the company to speak to a moderator to have their password reset. Actually writing code that automatically helps the user generate a new password for themselves is a <span style="color: #8888FF;">*Nice to have*</span>, but is not required)
* "Log In" button

### <span style="color: #00FFFF;">My Account</span>

A page for all accounts to update or change their contact information.

* My details (+ edit buttons for each)  
    1. First Name & Last Name
    2. Email Address
    3. Phone Number
    4. <span style="color: #8888FF;">*Nice to have:*</span> User Photo
    5. <span style="color: #8888FF;">*Nice to have:*</span> Viewing preference (i.e. light mode and dark mode)

* My Cases (list of all cases past & present as clickable links to each case)

### <span style="color: #00FFFF;">Case # xxxxxx</span> (to view just one record and its details)

A page going into detail about one particular case. Displaying the following

* Case # (8 digit YYMM####) last 2 digits of year the case was created, 2 digits for the month, and a 4 digit serial number that resets to 0 on the 1st of every month
* Brief 1-sentence description of error
* keywords/tags about the issue (won't turn on, error messages, fails to meet expectations, etc.)
* Customer Notes Field (updatable by customer and admin)
* Internal notes field (not visible to customers) - accessibly by any internal account.
* Case Status (created, awaiting customer response, flagged-needs review, closed-unresolved, closed-resolved)
* flagged for internal review (boolan-not visible to customer)
* log of activity (shows status change history, creation date, and attempted communications in and out to the customer)
* shortcuts for CSRs to contact the user from the case page (not visible to users)

### <span style="color: #00FFFF;">Internal-Active cases</span>

Visible only to all accounts above users. This page lists all currently active cases, is searchable (by case number, keywords, user, or by C.S.R.).

This list is sorted in order of priority, assumed that the highest priority cases are active cases whose latest status change has the oldest date (as new cases get added to the queue, the longer they go without being addressed, the higher priority they will receive)

### <span style="color: #00FFFF;">Internal-Closed cases</span>

Visible only to all accounts above users. This page lists all closed cases, is searchable (by case number, keywords, user, or by C.S.R.). It is used as reference material to solve issues found in active cases.

## <span style="color: #FFFF00;">Databases:</span>

### <span style="color: #00FFFF;">Accounts</span> – Object datatype
* Username (string)
* Authentication level (number: 0-4; 0-user, 1-CSR, 2-Specialist, 3-Moderator, 4-Admin)
* First Name (string)
* Last Name (string)
* password (<span style="color: #8888FF;">*Nice to have*</span> encrypted)
* email address (string)
* phone number (either string, or number if formatted as 10 digits with no non-number characters)
* Cases associated with the account (an array of case numbers)

### <span style="color: #00FFFF;">Cases</span> – Object datatype
* Case Number (number)
* Description (string)
* Keywords (array of strings)
* customer notes (string — block text)
* Internal notes (string — block text)
* Case Status (number: 0-5; 0-created, 1-awaiting customer response, 2-flagged-needs review, 3-closed-unresolved, 4-closed-resolved)
* flagged for internal review (boolean)
* log of activity (object containing arrays of strings \[ date of event, event type (i.e. status change), account that made the change\])