<h2 class="c-project-heading--task">Animate the sections</h2>

Use intersection observers to animate each content section when it scrolls into view.

<h2 class="c-project-heading--explainer">Follow these instructions</h2>

The first code snippet hides each content box until the animation starts. The second code snippet watches each slot and adds an animation class at the right moment.

Code snippet 1

<div class="c-project-code">

--- code ---
---
language: css
filename: style.css
line_numbers: true
line_number_start: 100
line_highlights: 106
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

## Now run your code

Make sure your browser window is wide enough to trigger the animations.

Run the project, choose an option, scroll down, and check that each section appears with an animation.
