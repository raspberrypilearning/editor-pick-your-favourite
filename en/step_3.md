<h2 class="c-project-heading--task">Show the first choice</h2>

--- task ---

Open `scripts.js`

--- /task ---

--- task ---

Write the JavaScript that fills the page with content when the first option is clicked.

Start by making one choice work from end to end. Once you can click one button and see your page update, the other choices will be much quicker to add.

--- /task ---

<div class="c-project-code">

--- code ---
---
language: javascript
filename: scripts.js
line_numbers: true
line_number_start: 13
line_highlights: 26, 29, 32, 35, 41-74
---
// Constants
const body = document.querySelector("body");
const instruction = document.querySelector("#instruction");
const content = document.querySelector("#content-holder");
const title = document.querySelector("#title");
const slot1 = document.querySelector("#slot-1");
const slot2 = document.querySelector("#slot-2");
const slot3 = document.querySelector("#slot-3");

// Clear function
function clear() {
  body.classList = "";

  title.innerHTML = "";

  slot1.classList = "content";
  slot1.innerHTML = "";

  slot2.classList = "content";
  slot2.innerHTML = "";

  slot3.classList = "content";
  slot3.innerHTML = "";

  dropdown.classList.remove("open");
}

// Option 1
function option1() {
  clear();

  instruction.style.display = "none";
  content.style.display = "grid";

  body.classList.add("trex");

  title.innerHTML = "T-Rex <br> &#129430";

  slot1.classList.add("trex");
  slot1.innerHTML =
    "<h1>Anatomy and Characteristics</h1> \n \
      <p>One of the largest meat-eating dinosaurs</p> \n \
      <p>Powerful hind limbs</p> \n \
      <p>Massive skull with sharp teeth</p> \n \
      <p>Tiny, two-fingered forelimbs</p>";

  slot2.classList.add("trex");
  slot2.innerHTML =
    "<h1>Trivia</h1> \n \
      <p>T-Rex had an huge bite force, capable of crushing bone</p> \n \
      <p>T-Rex was a fast runner</p> \n \
      <p>The name Tyrannosaurus Rex means tyrant lizard king in Greek</p>";

  slot3.classList.add("trex");
  slot3.innerHTML =
    "<h1>Activity</h1> \n \
      <ol>\n \
      <li>Get into teams and line up at a start line</li> \n \
      <li>Put one toy for each team member at the other end of the room</li> \n \
      <li>One person from each team races to 'bite' a toy and bring it back to the team</li> \n \
      <li>The first team to return all their toys wins!</li> </ol>";
}
--- /code ---

</div>

Use your own heading and facts if you picked a different topic, but keep the same pattern: clear the page, show the content grid, then fill the three slots.

<h2 class="c-project-heading--task">Test</h2>

--- task ---

Run the project, open the menu, click your first option, and confirm the title and all three content sections appear.

--- /task ---

