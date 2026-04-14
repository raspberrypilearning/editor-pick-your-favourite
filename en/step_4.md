<h2 class="c-project-heading--task">Add the other choices</h2>

### Step 1

Create the other two functions so each menu option shows different content on the page.


You already know the pattern from your first function, so now you can copy it and swap in the class names, titles, and facts for your second and third choices.

If your project is not about dinosaurs, change the text so each option shows the visitor something about your own topic.

<div class="c-project-code">

--- code ---
---
language: javascript
filename: scripts.js
line_numbers: true
line_number_start: 76
line_highlights: 77-150
---
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
}
--- /code ---

</div>

<h2 class="c-project-heading--task">Test</h2>

### Step 2

Run the project and confirm each menu choice shows a different title, different colours, and different content.
