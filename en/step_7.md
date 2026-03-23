<h2 class="c-project-heading--task">Remember the last choice</h2>

--- task ---
Use local storage so the page remembers the visitor's last choice and add a reset button to clear it.
--- /task ---

The first code snippet saves the selected option, restores it when the page loads, and clears it again when the visitor resets the page.

Code snippet 1

<div class="c-project-code">

--- code ---
---
language: javascript
filename: scripts.js
line_numbers: true
line_number_start: 40
line_highlights: 75,115,152,187-205
---
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

  localStorage.setItem("choice", "trex");
}

// Option 2
function option2() {
  clear();

  instruction.style.display = "none";
  content.style.display = "grid";

  body.classList.add("triceratops");

  title.innerHTML = "Triceratops";

  slot1.classList.add("triceratops");
  slot1.innerHTML =
    "<h1>Anatomy and Characteristics</h1> \n \
      <p>A herbivorous dinosaur</p> \n \
      <p>Known for its distinctive frill and three facial horns</p> \n \
      <p>It had a bulky body, a beak-like mouth, and a large bony plate projecting from the back of its skull</p> \n \
      <p>Triceratops likely lived in herds and used its horns for defense</p>";

  slot2.classList.add("triceratops");
  slot2.innerHTML =
    "<h1>Trivia</h1> \n \
      <p>Triceratops was a bit of a show off, its frill may have been used for display</p>\n \
      <p>Triceratops roamed North America during the Late Cretaceous period</p>\n \
      <p>Triceratops means three-horned face in Greek</p>";

  slot3.classList.add("triceratops");
  slot3.innerHTML =
    "<h1>Activity</h1> \n \
      <ol>\n \
        <li>Create some Triceratops horns using paper or cardboard</li>\n \
        <li>Attach them to headbands or make them handheld</li>\n \
        <li>Place the horns at varying distances on the ground</li>\n \
        <li>Use hula hoops or create rings from cardboard</li>\n \
        <li>Take turns tossing the rings onto the Triceratops horns, earning 10 points.</li>\n \
        <li>The person with the most points after all turns wins.</li> </ol>";

  localStorage.setItem("choice", "triceratops");
}

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

// Loaded function
document.addEventListener("DOMContentLoaded", function () {
  const choice = localStorage.getItem("choice");

  if (choice == "trex") {
    option1();
  } else if (choice == "triceratops") {
    option2();
  } else if (choice == "stegosaurus") {
    option3();
  }
});

// Reset
function reset() {
  clear();
  content.style.display = "";
  instruction.style.display = "flex";
  localStorage.setItem("choice", "");
}
--- /code ---

</div>

Code snippet 2

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 15
line_highlights: 19
---
<div id="dropdown-options">
  <button onclick="option1()">Tyrannosaurus Rex</button>
  <button onclick="option2()">Triceratops</button>
  <button onclick="option3()">Stegosaurus</button>
  <button onclick="reset()">Reset</button>
</div>
--- /code ---

</div>

<h2 class="c-project-heading--task">Test</h2>

--- task ---
Run the project, choose an option, run it again to check the page remembers that choice, then click Reset and confirm the instructions come back.
--- /task ---

