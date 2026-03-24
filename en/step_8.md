<h2 class="c-project-heading--task">Upgrade your project</h2>

--- task ---

Extend your fan website by adding another option or giving each section more styling.

--- /task ---

One way to upgrade your project is to add a fourth choice. Copy one of your existing functions, rename it, then change the class names and content so it matches your new idea.

<div class="c-project-code">

--- code ---
---
language: javascript
filename: scripts.js
line_numbers: true
line_number_start: 118
line_highlights: 119-153
---
// Option 3
function option3() {
  clear();

  instruction.style.display = "none";
  content.style.display = "grid";

  body.classList.add("stegosaurus");

  title.innerHTML = "Stegosaurus";

  slot1.classList.add("stegosaurus");
  slot1.innerHTML =
    "<h1>Anatomy and Characteristics</h1> \n \
      <p>Stegosaurus was a plant eater.</p> \n \
      <p>It had a double row of large bony plates along its back</p> \n \
      <p>It had spikes on its tail</p> \n \
      <p>It had a small head, with a small brain compared to its body size</p>";

  slot2.classList.add("stegosaurus");
  slot2.innerHTML =
    "<h1>Trivia</h1> \n \
      <p>Stegosaurus had a second brain in its hips, assisting in coordinating movement and balance</p>\n \
      <p>Stegosaurus lived during the Late Jurassic period</p> \n \
      <p>Stegosaurus means armoured roof lizard in Greek</p> \n \
      <p>The stop-motion puppet used in the 1933 film King Kong was based on a 1897 illustration of Stegosaurus</p>";

  slot3.classList.add("stegosaurus");
  slot3.innerHTML =
    "<h1>Activity</h1> \n \
      <ol><li>Decorate some paper plates to make Stegosaurus's bony plates</li>\n \
      <li>Once the plates are dry, have a Stegosaurus parade to showcase your plates</li>\n \
      <li>Share the designs and celebrate the creativity.</li></ol>";

  localStorage.setItem("choice", "stegosaurus");
}
--- /code ---

</div>

If you want a styling challenge instead, keep the same three options and improve the layout, colours, or text styling inside each content box.

<h2 class="c-project-heading--task">Test</h2>

--- task ---

Run your project and confirm your upgrade works, whether that means a brand new option appears or your existing sections have a stronger design.

--- /task ---

