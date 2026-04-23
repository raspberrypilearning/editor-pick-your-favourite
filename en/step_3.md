<h2 class="c-project-heading--task">Add your colours</h2>

Create colour variables and CSS classes so each choice can give the page its own look.

<h2 class="c-project-heading--explainer">Follow these instructions</h2>

Replace the example class names and colours with ones that match your own topic.


The first code snippet stores the colours in `default.css`. The second code snippet uses those colours in `style.css`.

Code snippet 1

<div class="c-project-code">

--- code ---
---
language: css
filename: default.css
line_numbers: true
line_number_start: 1
line_highlights: 8-28
---
:root {
  /* Font variable */
  --main-font: "sans-serif";

  /* Base Colours */
  --body-background: #ffffff;
  --body-text-colour: #000000;
  --nav-bar: #ffffff;

  /* Option Body classes */
  --body-t-rex: #ffffff;
  --body-triceratops: #ffffff;
  --body-stegosaurus: #ffffff;

  /* Slot 1 colours */
  --slot-1-t-rex: #00b2a9;
  --slot-1-triceratops: #1c2c5b;
  --slot-1-stegosaurus: #132257;

  /* Slot 2 colours */
  --slot-2-t-rex: #00b2a9;
  --slot-2-triceratops: #ffc659;
  --slot-2-stegosaurus: #131f53;

  /* Slot 3 colours */
  --slot-3-t-rex: #00b2a9;
  --slot-3-triceratops: #ec3325;
  --slot-3-stegosaurus: #131f53;
}
--- /code ---

</div>

Code snippet 2

<div class="c-project-code">

--- code ---
---
language: css
filename: style.css
line_numbers: true
line_number_start: 40
line_highlights: 44,91,111-229
---
nav {
  height: 60px;
  display: flex;
  justify-content: center;
  background-color: #9385bf;
  position: fixed;
  top: 0;
  width: 100%;
}

.dropdown {
  width: 300px;
  font-size: large;
  padding: 5px;
  display: flex;
  min-height: 100%;
  flex-direction: column;
}

button {
  width: 100%;
  border: none;
  background-color: white;
  font-size: 32px;
  font-family: inherit;
}

#dropdown-options {
  position: relative;
  display: none;
  color: white;
  min-width: 140px;
  text-align: center;
  z-index: 1;
}

#dropdown-options.open {
  display: flex;
  flex-direction: column;
  z-index: 1;
}

#instruction {
  height: 100vh;

  h1 {
      font-size: 62px;
  }
}

#content-holder {
  display: none;
  grid-template-rows: repeat(3, 100vh auto);
}

#content-holder > h1 {
  font-size: 3em;
  margin: auto;
}

.content {
  width: 100%;
  border-radius: 5px;
  box-shadow: 5px 5px black;
  padding: 5px;
  font-size: 32px;
}

/* Slot 1 classes */


#slot-1 {
  grid-row-start: 2;
  grid-row-end: 3;
}

#slot-1.trex {
  background-color: var(--slot-1-t-rex);

  h1 {
    color: #f6eb61;
  }
}

#slot-1.triceratops {
  background-color: var(--slot-1-triceratops);

  h1 {
    color: rgb(255, 198, 89);
  }
}

#slot-1.stegosaurus {
  background-color: var(--slot-1-stegosaurus);
  color: white;

  h1 {
    color: white;
  }
}

/* Slot 2 classes */


#slot-2 {
  grid-row-start: 4;
  grid-row-end: 5;
}

#slot-2.trex {
  background-color: var(--slot-2-t-rex);
  color: white;

  h1 {
    color: #f6eb61;
  }
}

#slot-2.triceratops {
  background-color: var(--slot-2-triceratops);
  color: black;

  h1 {
    color: rgb(28, 44, 91);
  }
}

#slot-2.stegosaurus {
  background-color: var(--slot-2-stegosaurus);
  color: white;

  h1 {
    color: white;
  }
}

/* Slot 3 classes */


#slot-3 {
  grid-row-start: 6;
  grid-row-end: 7;
}

#slot-3.trex {
  background-color: var(--slot-3-t-rex);
  text-align: left;

  h1 {
    color: #f6eb61;
    text-align: center;
  }
}

#slot-3.triceratops {
  background-color: var(--slot-3-triceratops);
  text-align: left;
  color: white;

  h1 {
    color: rgb(255, 198, 89);
    text-align: center;
  }
}

#slot-3.stegosaurus {
  background-color: var(--slot-3-stegosaurus);
  color: white;
  text-align: left;

  h1 {
    color: white;
    text-align: center;
  }
}

.trex {
  background-color: #41220f;
  color: white;
}

.triceratops {
  background-color: #6a7029;
  color: white;
}

.stegosaurus {
  background-color: rgb(32, 78, 55);
  color: black;
}

/* Animations */


--- /code ---

</div>

## Now run your code

Run the project, click your first option, and confirm the page background and content boxes change to match that choice.

Confirm the observable result.
