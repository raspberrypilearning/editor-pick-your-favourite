<h2 class="c-project-heading--task">Animate the sections</h2>

--- task ---
Use intersection observers to animate each content section when it scrolls into view.
--- /task ---

The first code snippet hides each content box until the animation starts. The second code snippet watches each slot and adds an animation class at the right moment.

Code snippet 1

<div class="c-project-code">

--- code ---
---
language: css
filename: style.css
line_numbers: true
line_number_start: 103
line_highlights: 109
---
.content {
  width: 100%;
  border-radius: 5px;
  box-shadow: 5px 5px black;
  padding: 5px;
  font-size: 32px;
  opacity: 0;
}
--- /code ---

</div>

Code snippet 2

<div class="c-project-code">

--- code ---
---
language: javascript
filename: scripts.js
line_numbers: true
line_number_start: 155
line_highlights: 156-184
---
// Observers
const slot1observer = new IntersectionObserver(
  (entries) => {
    if (entries[0].isIntersecting) {
      slot1.classList.add("fade-in");
    }
  },
  { threshold: 1 }
);
slot1observer.observe(slot1);

const slot2observer = new IntersectionObserver(
  (entries) => {
    if (entries[0].isIntersecting) {
      slot2.classList.add("grow-in");
    }
  },
  { threshold: 1 }
);
slot2observer.observe(slot2);

const slot3observer = new IntersectionObserver(
  (entries) => {
    if (entries[0].isIntersecting) {
      slot3.classList.add("rise-in");
    }
  },
  { threshold: 1 }
);
slot3observer.observe(slot3);
--- /code ---

</div>

You can swap the animation class names if you want a different effect for each section.

<h2 class="c-project-heading--task">Test</h2>

--- task ---
Run the project, choose an option, scroll down, and confirm each section appears with an animation instead of showing straight away.
--- /task ---

