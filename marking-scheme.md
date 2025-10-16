# Project Marking Scheme (Fall 2025)

**Student Name:** Lihini Herath


This project is graded using a version of something called **specifications grading**. Your submitted `submission-checklist.md` is the primary document used for marking. Each grade level is obtained by completing a "bundle" of requirements. To earn a grade, you must successfully complete **all specifications** in that grade's bundle as well as all bundles below it.

Your instructor's role is to **verify the accuracy** of the items you've checked. A bundle is **satisfactory** only if you have checked all its corresponding items **and** the instructor confirms they are functional.

If you obtain the highest level bundle (which works out to be an A-), you have the opportunity to obtain additional marks as well to bring your mark to the A or A+ level.

---

## 🚨 [DEALBREAKER] Items

The checklist contains items marked as a **[DEALBREAKER]**. These represent the non-negotiable, foundational requirements of the project.

- If the instructor finds that **any** [DEALBREAKER] item is non-functional, the Project will receive an F.

---

## 🎟️ Revision Token

To encourage learning from mistakes, and reduce stress (at least a bit), you are granted **one "revision token"** for the Project.

- Your token can be used to resubmit a bundle that was marked "Unsatisfactory" within 48 hours of your instructor you giving you feedback.
- Tokens cannot be used for an initial submission that fails a [DEALBREAKER] check.

---

## ✅ Honesty Clause

Your self-assessment (i.e. submission checklist) must be accurate. A bundle will be marked **Unsatisfactory** if:
1. The instructor finds more than one checked item to be non-functional, and these issues were not disclosed in the 'Known Issues' section. **OR**
2. Any single checked item is non-functional and was not noted by you in the "Known Issues" section of the checklist.

---

## 🏆 Grade Bundles

### 30-Level Bundle: Foundation & Integrity

This bundle covers the non-negotiable technical requirements for the project to be gradable.

- [ ] All checklist items marked **[DEALBREAKER]** under "Part 1: Underlying Code & Submission Checks" are checked and verified.
- [ ] You have submitted a single SQL script in `/config/initdb` that creates and populates all necessary tables with at least 100 records each.
- [ ] Your instructor believes you have made a "reasonable attempt" at completing at least the Admin Portal Site. He'll use his best judgement and your Git history to help him determine this if necessary.
- [ ] The `submission-checklist.md` is submitted and completed with a reasonable degree of accuracy. (See Honesty Clause above.)

### 40-Level Bundle: Core Administrative Functionality

This bundle ensures the admin can log in, navigate, and view data.

- [ ] All requirements in the **30-Level Bundle** are met.
- [ ] All checklist items under "Part 2 -> Administrative Portal -> **Login Page**" are checked and verified.
- [ ] The dashboard, customer, and movie pages are accessible with clear navigation links.
- [ ] The customer data and movie listings are displayed correctly in their initial, unfiltered/unsorted state.

### 50-Level Bundle: Dynamic Admin

This bundle adds data manipulation to the admin portal.

- [ ] All requirements in the **40-Level Bundle** are met.
- [ ] All checklist items under "Part 2 -> Administrative Portal -> **Dashboard Page**" are checked and verified.
- [ ] All checklist items under "Part 2 -> Administrative Portal -> **Customer Data Page**" are checked and verified.
- [ ] All checklist items under "Part 2 -> Administrative Portal -> **Movie Listings Page**" are checked and verified.


### 70-Level Bundle: Public App Core

This bundle establishes the core functionality of the public app.

- [ ] All requirements in the **50-Level Bundle** are met.
- [ ] All checklist items under "Part 2 -> Public-Facing App -> **Login Page**" are checked and verified.
- [ ] All checklist items under "Part 2 -> Public-Facing App -> **Personal Dashboard Page**" are checked and verified.


### 80-Level Bundle: Full-Featured Application & Professional Polish

This bundle represents a complete project that meets all requirements.

- [ ] All requirements in the **70-Level Bundle** are met.
- [ ] All checklist items under "Part 2 -> Public-Facing App -> **Find a Buddy Page**" are checked and verified.
- [ ] All non-dealbreaker items in "Part 1" of the checklist are checked and verified.


---

## 🌟 Additional Marks

If you have completed the 80-Level Bundle, I will add up to 20% in additional marks as follows.

_I realize that a lot of these marks are subjective and/or the requirements or point allocations are vague. This is partly by intent and partly because that's the nature of this work._

### Dev Journal (up to 6%)

- [ ] 6: All entries, or all but one entries, are completed satisfactorily.
- [ ] 3: Two entries are missed, but the remaining entries are completed satisfactorily.
- [ ] 1: Three entries are missed, but the remaining entries are completed satisfactorily.
- [ ] 0: Four or more entries are missed, but the remaining entries are completed satisfactorily.

If in my judgement your journal entries as a whole over the span of the semester show an honest effort, that will be considered satisfactory.


### UI/UX (up to 10%, 5% for Admin Portal and 5% for App)

This is a development course, not a design course...but a certain amount of design care must be taken, especially in consideration of the amount of assistance developers these days can obtain through careful AI use.

I will mark UI/UX with these questions in mind:

- Do pages on a site have a unified visual "feel"? 
- Is it made clear to the user visually that sorting/adding/deletion has occurred?
- Are icons used to make pages less text heavy?
- Do pages contain examples of design that are simply "phoned in" - that is, no effort whatsoever was taken with the visual design. (Some examples of goodish and "phoned in" design can be seen in [these examples from last year](https://drive.google.com/drive/folders/17XerNFyw8n-DIIeq2BMSV606Z0HHH9ZP?usp=sharing). Can you tell which are examples of "phoned in" work?)
    - 'Phoned in' work is characterized by a lack of effort, such as using unstyled, default HTML elements or creating layouts that are misaligned and ignore the specified viewport widths.
- Is it reasonably obvious to figure out how to use the site - even to someone not familiar w/ The Project? 
- Are there any truly broken things going on? (Things like freezing, links that go to incorrect or non-existent pages, buttons that seem to do nothing, and other such shenanigans.) 

#### Admin Portal Site UI/UX @ Laptop L (up to 5%)

- [ ] 5: I'm honestly impressed.
- [ ] 4: Minor issues only present.
- [ ] 3: One or two "phoned it in" examples present.
- [ ] 0: Something egregious causes page(s) to malfunction, or 3+ "phoned it in" examples present throughout the site.

#### Public-Facing App UI/UX @ Mobile M (up to 5%)

- [ ] 5: I'm honestly impressed.
- [ ] 4: Minor issues only present.
- [ ] 3: One or two "phoned it in" examples present.
- [ ] 0: Something egregious causes page(s) to malfunction, or 3+ "phoned it in" examples present throughout the site.

### Code Quality (up to 4%)

The codebase is reasonably easy to understand, and has few - if any - violations of the following signs of coding craftsmanship:

- Variables are named expressively, and not vague - or even worse - telling lies.
- There is a consistent "feel" to the code - it does not feel like it was Frankenstein'd together from a variety of sources.
- Functions are used to perform repeated/complicated tasks.
- Unneeded files aren't present.
- Global variables are kept to a minimum.
- `for each` loops are primarily used in both languages instead of fors/whiles
- Functions are plentiful, expressively named, and short.
- Tricky things are documented with appropriate useful reference links.
- Files are small, well-named, and contain reasonable things.

- [ ] 4 (Excellent): The codebase consistently adheres to the signs of coding craftsmanship. Violations are rare and minor (e.g., one or two slightly vague variable names in a large project). The code is easy to read and understand. 
- [ ] 3 (Good): The codebase demonstrates a strong attempt at craftsmanship. There are some minor, inconsistent violations (e.g., a few functions are a bit long, some files could be better organized), but the overall structure is sound.
- [ ] 1 (Needs Improvement): The codebase has frequent and noticeable violations of craftsmanship principles. It is often difficult to follow, with poorly named variables, very long functions, or a confusing file structure. 
- [ ] 0 (Poor): The codebase shows a widespread disregard for craftsmanship. It feels "Frankenstein'd together," is difficult to read, and lacks a coherent structure.
