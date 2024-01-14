```
 <div class="container">
      <div class="progress-container">
        <div class="progress" id="progress"></div>
        <div class="circle active">1</div>
        <div class="circle">2</div>
        <div class="circle">3</div>
        <div class="circle">4</div>
      </div>

      <button class="btn" id="prev" disabled>Prev</button>
      <button class="btn" id="next">Next</button>
    </div>

```html

Contains the visible content of the HTML document:
A <div> with class container acts as the main container for the elements.
Inside the container, there is a <div> with class progress-container, presumably to hold the progress steps.
Within this, there is another <div> with class progress and an ID progress. This likely represents the progress bar.
Following this are four <div> elements with class circle, each containing a number (1 to 4). These probably represent the steps in the progress bar. The first circle has an additional class active, indicating that it is the current step.
There are two buttons:
A "Prev" button with class btn and ID prev, which is disabled (disabled attribute). This button is for navigating to the previous step.
A "Next" button with class btn and ID next, for navigating to the next step.