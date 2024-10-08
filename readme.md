# Spin and Sip Website
[Live website](https://iterating.github.io/ps-316-sba/3.book.html)  

[Github source](https://github.com/iterating/ps-316-sba/blob/main/booking.mjs)

I'm inspired by how Nuxt/Vue/React works and started this project with a goal of dynamically rendering most of the content. 

## Objectives
- Populate homepage dynamically from yml file
- Programmatically create cards and sections according to yml data
- Prioritize UX 

## Overview
- The booking calendar is dynamically generated using DocumentFragment and cloneNode. Wicth DOM and DOM methods and event handling logic, the user can click and select dates on the calendar. 
- The selected dates are processed into a `selectedDates` array, which populates the dates section of the form. Users can select and deselect dates due to data handling logic and `array.splice`.
- The form input fields are validated by regex on submission. 
- The booking data is stored as an object in a array on localstorage. Window size is stored for UX purposes. In the future it will be stored to database such as Supabase. 
- Practiced writing arrow functions 
## Tools Used
- jsyaml for processing yaml into json. I decided to use CDN delivered to keep the files light. I would include local libraries if I were to prioritize long term reliability and interoperability. For larger projects, I would consider using a framework for package management. My tech choices here reflect this project as a learning project with a goal of gaining deeper insight of current web standards of HTML, CSS and Javascript.
- Flexbox is used heavily for mobile first design
- [x] Used marked.js to parse markdown into HTML and DOMPurify to sanitize the HTML

# Outcomes
- Learned some details of using **modules**. I thought deeply about adding page components programmatically when possible, and used modules for flexibility and keeping **DRY**. As I write my code from what I want it to do and keep refactoring it, I better conceptualize how start with building with the end in mind. Making modules reusable was a challenging and rewarding process.
    - Learned to create an object that **maps function names (keys) to function references** in order to call them programmatically at runtime
- Running into bugs exposes me to the way code can break, and how to build my code to handle errors. By running my code on an empty HTML document, I found how my implementation of `addEventListener` breaks when `getElementbyID` doesn't find its elements, and became aware of implementing error handling as a write my code. Practiced error handling with try...catch, if...else methods. Practiced console.log-ing and checking expected values while coding. Made a habit of **checking responses** in the process of making functions and error checking early. 

## Further Projects
- [ ] In the future, I would like learn to build **Webcomponents** to build and use HTML by components to promote DRY. For example, the `side menu drawer`,`navbar`, and `login` components ideally should be referenced, not repeated, in each page
    - [ ] Understand how shadow DOM works and how to utilize it effectively and cleanly
    - [ ] Build my own collection of components for practice and future use in projects
- [x] Include a drinks menu page that's rendered from a markdown document. I believe Markdown and YAML make a `grep`-able, time saving CMS system 
- Build a working calendar booking component. Programmatically check the month and add empty `<td class="day">` elements to fill up the first week calendar cells according to the date. 
    - Explore different components, libraries, APIs, and methods of offering a public facing way to interface with calendar booking. This might be a long project. 
        - Explore working with iCalendar format and with gCal API 


### HTML Requirements
- [x] Cache at least one element using selectElementByld.

- [x] Cache at least one element using querySelector or querySelectorAll.

- [x] Use the parent—child—sibling relationship to navigate between elements at least once(firstChild, lastChild, parentNode, nextElementSibling, etc.).

- [x] lterate over a collection of elements to accomplish some task.

- [x] Create at least one element using createElement.

- [x] Use appendChild and/or prepend to add new elements to the DOM.

- [x] Use the DocumentFragment interface or HTM L templating with the cloneNode method to create templated content.

- [x] Modify the HTM L or text content of at least one element in response to user interaction using innerHTM L, innerText, or textContent.

- [x] Modify the style and/or CSS classes of an element in response to user interactions using the style or classList properties.

- [x] Modify at least one attribute of an element in response to user interaction.

- [x] Register at least two different event listeners and create the associated event handler functions.

- [x] Use at least two Browser Object Model (BOM) properties or methods.

- [x] Include at least one form and/or input with HTM L attribute validation.

- [x] Include at least one form and/or input with DOM event-based validation. (This can be the same form or input as the one above, but should include event-based validation in addition to the HTML attribute validation.)

- [x] Ensure that the program runs without errors (comment out things that do not work, and explain your blockers - you can still receive partial credit).

- [x] Commit frequently to the git repository.

- [x] Include a README file that contains a description of your application.