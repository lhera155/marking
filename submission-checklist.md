# The Project: Submission Checklist

**Instructions:** Before submitting your project, go through this entire checklist in order. Test each feature and place a check (`x`) in the box only if you can confirm it works exactly as described. Submitting an accurately completed checklist is a part of the project's professionalism requirements.

**Student Name:** Lihini Herath

---

## Part 1: Underlying Code & Submission Checks

Any entry marked as **[DEALBREAKER]** must be checked for your Project submission to be marked.

- [ ] I have included a single SQL script in the `/config/initdb` directory that creates all tables necessary for both sites to work properly, populated with at least 100 records each.

### Administrative Portal (PHP)

- [ ] The digests in my `administrators` table begin with `$2y$15`, proving I've used the bcrypt algorithm with a cost of 15.
- [ ] My code does not use `mysqli` functions; it exclusively uses PDO. **[DEALBREAKER]** 
- [ ] My forms do not use any client-side (HTML or JS) validation.
- [ ] My login code uses the `password_verify()` function. **[DEALBREAKER]** 
- [ ] My `/admin/customers` and `/admin/listings` pages pass W3C validation with no errors. (Warnings are acceptable.)
- [ ] My site uses the provided Router class for all page requests. **[DEALBREAKER]** 
- [ ] My site uses the provided `DatabaseQueries` class for all database queries, including the ones used for the custom API endpoints. **[DEALBREAKER]** 
- [ ] My code does not use any external PHP libraries. **[DEALBREAKER]** 
- [ ] All my custom API endpoints follow the `/api/...` format.
- [ ] All my API endpoints return a content type of `application/json`.
- [ ] All database queries that use `$_GET` or `$_POST` data use prepared statements.
- [ ] My administrative portal does not use any JavaScript. **[DEALBREAKER]** 

### Public-Facing App (JS)

- [ ] My app is a single page (one PHP view) that uses external JS to modify the DOM. **[DEALBREAKER]** 
- [ ] All my JavaScript is in external files loaded via `<script type="module">`. **[DEALBREAKER]**
- [ ] My code does not use `onclick` or other `on...` event attributes in the HTML. **[DEALBREAKER]**
- [ ] My code does not use the `innerHTML` property. **[DEALBREAKER]**
- [ ] My code does not use `alert()`.
- [ ] My code does not use third-party JS libraries (unless I received permission). **[DEALBREAKER]** 
- [ ] My code uses an HTML `<dialog>` element and vanilla JS to implement the login modal. **[DEALBREAKER]**
- [ ] My Personal Dashboard page passes W3C validation after adding *and* after removing a movie.
- [ ] I have used event delegation for handling clicks on dynamic elements (e.g., removing a film).
- [ ] I have used Promise chaining to consume at least one API endpoint.
- [ ] I have used `async/await` to consume at least one API endpoint.
- [ ] I have implemented caching of watchlist data using Web API's localStorage.

---

## Part 2: Page Functionality Checks

The bracketed numbers refer to functionalities listed in the Requirements docs. For example, for an entry under the Administrative Portal section, `[2]` refers to functionality #2 in the Administrative Portal Requirements document: "I want to log in to the administrative portal with an email and a password."

### Administrative Portal (PHP)

*Before starting, I have opened my browser in **Laptop L mode** (1440px wide).*

#### Login Page
- [ ] When logged out, trying to access `/admin/dashboard` redirects me to `/admin`. [10]
- [ ] When logged out, trying to access `/admin/customers` redirects me to `/admin`. [17]
- [ ] When logged out, trying to access `/admin/listings` redirects me to `/admin`. [26]
- [ ] When logged out, if I go to `/admin`, I see an empty login form.[1,3]
- [ ] The login form obfuscates the password. [4]
- [ ] When I log in with `foo@foo.com` and `comp3512`, I wind up back at the login form with `foo@foo.com` filled in, the password field empty, and a suitably vague notification telling me the login was unsuccessful. [5,6,8]
- [ ] When I log in with `jpratt@mtroyal.ca` and `foo`, I wind up back at the login form with `jpratt@mtroyal.ca` filled in, the password field empty, and a suitably vague notification telling me the login was unsuccessful. [5,6,8]
- [ ] When I log in with `jpratt@mtroyal.ca` and `comp3512`, I land on the `/admin/dashboard` page, with the date and time in MST/MDT of my last login clearly visible. [7,8,14]

#### Dashboard Page
- [ ] There is a clear way to log out; doing so takes me back to the Login Page with an empty login form. [11]
- [ ] There is a clear way to get to the Customer Data Page and it has resource path `/admin/customers`. [12,16]
- [ ] There is a clear way to get to the Movie Listings Page and it has resource path `/admin/listings`. [13,25]
- [ ] The dashboard correctly displays all required analytics. [15]
- [ ] If I leave this page and come back, the date/time of my last login is no longer visible, and I've used cookies to accomplish this. [14]

#### Customer Data Page
- [ ] There is a clear way to log out; doing so takes me back to the Login Page with an empty login form. [18]
- [ ] There is a clear way to get to the Dashboard Page and it has resource path `/admin/dashboard`. [19,9]
- [ ] There is a clear way to get to the Movie Listings Page and it has resource path `/admin/listings`. [20,25]
- [ ] I clearly see all required information about every customer. [21]
- [ ] I can successfully filter customers by their plan type. [22]
- [ ] I can sort the results by name (ascending and descending) using hyperlinks, and clearly see whether the names are sorted ascending or descending. [23]
- [ ] I can filter by plan type and then sort the results by name and only see sorted results of that type. [24]

#### Movie Listings Page
- [ ] There is a clear way to log out; doing so takes me back to the Login Page with an empty login form. [27]
- [ ] There is a clear way to get to the Dashboard Page and it has resource path `/admin/dashboard`. [28,9]
- [ ] There is a clear way to get to the Customer Data Page and it has resource path `/admin/customers`. [29,16]
- [ ] I can see a list of theatres grouped by province. [30]
- [ ] I can click on a theatre and see the names of the 3 (or fewer) movies playing there. [31]
- [ ] I can successfully add a movie to a theatre. [32]
- [ ] I can successfully remove a movie from a theatre. [32]


### Public-Facing App (JS)

*Before starting, I have opened my browser in **Mobile M mode** (375px wide).*

#### Login Page
- [ ] When logged out, if I go to `/`, I see an empty login form that lets me request an OTP using either a cell number or email address.[1,2]
- [ ] When I enter an unknown user's email/phone, a clear error message appears and the modal does not. [4]
- [ ] When I enter a known user's email/phone, the OTP modal appears. [3]
- [ ] I can close the OTP modal without logging in, and it has no negative effect. [3]
- [ ] If I enter an incorrect OTP in the modal, a clear error message is shown within the modal, and I can try again. [6]
- [ ] When I enter the correct OTP (the string `OTP`, case-insensitive), I am taken to the Personal Dashboard page. [5] 

#### Personal Dashboard Page
- [ ] There is an obvious way to logout here; when I do, I'm returned to a reset login page. [8]
- [ ] My user information (name, email, phone, preferred theatres, and customer type) is correctly displayed here. [9]
- [ ] My watchlist correctly displays each film's title, runtime in minutes, and the specific preferred theatres playing it. [10]
- [ ] For films on my watchlist that are not playing at any of my preferred theatres, this is clearly indicated. [10]
- [ ] I can remove a film from the watchlist, and it disappears without a page reload. [11]
- [ ] The "add a film" feature only shows the type-ahead dropdown after I have typed at least 3 characters (case-insensitive), and it adds the selected film to my watchlist without a page reload. [12]
- [ ] There's an obvious way to find a buddy for any film on my watchlist; when I use it, I am taken to the Find a Buddy Page. [13]


#### Find a Buddy Page
- [ ] The title of the film I selected on the Personal Dashboard Page is clearly displayed. [15]
- [ ] The view correctly displays a clear message if I have no buddies at all. [16]
- [ ] The view correctly displays a clear message if I have buddies, but none want to see the selected film. [17]
- [ ] If I have buddies who want to watch the film, their full details (name, email, phone, preferred contact method, preferred theatres) are all displayed. [18]
- [ ] This page can be closed, returning me to the Personal Dashboard. [14]


---

### Known Issues / Incomplete Features

*(Use this space to list any features you know are not working correctly. Honesty here is a key part of the professionalism grade.)*

________________________________________________________________________________
________________________________________________________________________________

**By submitting this checklist, I affirm that I have personally tested each of the checked features and that this document accurately reflects the state of my project at the time of submission.**
