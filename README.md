# Nyborg-Aktivitetspark


## Update 0.1.1:
> Added 18. June 2024 - 15.02

### Devlog.
It has been a while since I have added anything to the updates, which has been an error on my part. There will (if possible) daily updates from now on. Now let us get into the changes that have been made.
<br>
The goal for the website currently, is to get it compatible with WordPress, so it can be used by users. At the time of writing this log, the time required to reach an end product is unknown. 
<br>

### XAMPP
- I've used XAMPP. XAMPP is a popular PHP development environment that allows you to run PHP, Apache, and MySQL servers locally on my machine.

### PHP
- The HTML structure is currently being split up using the PHP. It is a challenge at the moment since PHP, I will have to learn PHP to make this work. 

<br>

### CSS
- There has been a lot of changes to the websites CSS code, since it was previously not responsive. Therefore, the code has got very long and cluttered, it will need to be segmented, to make it easier to adjust the websites design.


## Update 0.1.0.0:
Added 21. March - 14:51

### Rework
- The entire design has been changed, to make more stylish and minimalistic.  The goal for this is to make the page more readable for users.
- Menu has been moved to the left (will probably be using a hamburger-menu in the future)

<br>
<br>
<br>

## Update 0.0.5.2:
> Added 20. March 2024 - 15.28

### "Nothing to see here"
- Rework is in effect

<br>
<br>
<br>


## Update 0.0.5.1b:
> Added 20. March 2024 - 14:07 

### Text
- Text has been adjusted. However only by using breaking element in html. 
- Webpage will be remade using grid- and flexboxes to enhance the webpage. 


<br>
<br>
<br>


## Update 0.0.5.1a:
> Added 20. March 2024 - 11:14

### Text
- Text is being added and layout for it is being adjusted (.section-one .headline and .section-one .paragraph)
- The goal is to have the the text load once the corelating section has been selected (using the navigation buttons or arrowkeys)


<br>
<br>
<br>


## Update 0.0.5:
> Added 20. March 2024 - 09:11

### Frame
- The initial version of the frame has been added. (Has to be reworked so it will work with smartphone-view.)

### Backgrounds
- I have added backgrounds, so it will be easier to see the direction of the webpage's layout

### Bug fixes
- A bug occured that made the button and the arrowkeys not work as intended. This has now been fixed.
> Reason: duplication in the code made it unreadable for JavaScript.



<br>
<br>
<br>



## Update 0.0.4.1:
> Added 19. March 2024 - 14:37

### Testing
- There has been done testing on adding a better user-interface for
  smartphone-view
- The code for the webpage's frame has been added to WORK-IN-PROGRESS.md
>Read more there


<br>
<br>
<br>


## Update 0.0.4:
> Added 19. March 2024 - 10:51

### Base Structure:
- Added frame images to enhance visual appeal (commented out for later addition).

### Styling:
- Adjusted button styles for better consistency and user experience.
- Tweaked the positioning of navigation buttons for improved layout.

### Functionality:
- Implemented keyboard navigation using arrow keys for seamless user interaction.
- Improved button visibility based on the current section to enhance usability.

### "Going forward":
- Further customization of frame images to complement the design.
- Exploration of additional features to enrich user engagement.


<br>
<br>
<br>



## Update 0.0.3:
> Added 18. March 2024 - 12:41

### Base Structure:
- Implemented the basic structure of the webpage, including navigation links and content sections.
- The "dropdown" class has been added, to help make a dropdown of the contents of the webpages.
  
```html
           <li class="dropdown">
            <a href="/assets/pages/kontakt.html">Kontakt</a>
            <div class="dropdown-content">
              <a href="/assets/pages/partnerinfo.html">Partnere i projektet</a>
            </div>
  ```
        
### Styling
- Applied more refined (however, still somewhat crude) CSS styling to define the layout and appearance of the webpage.
- Adjusted button sizes and positions for better compatibility across different screen sizes and resolutions.

### Functionality
- Integrated a fixed navigation bar for improved accessibility and user experience.
- Fine-tuned layout and styles for optimal presentation with horizontal scroll.
- Introduced buttons for navigating between sections horizontally.
  > For this a JavaScript has been written:
```js
document.addEventListener("DOMContentLoaded", function() {
  // Få fat i alle sektioner
  const sections = document.querySelectorAll(".section");

  // Få fat i knapperne
  const goRightBtn = document.getElementById("goRight");
  const goLeftBtn = document.getElementById("goLeft");

  // Aktuelt sektionsindeks
  let currentIndex = 0;

  // Funktion til at rulle til næste sektion
  function gåTilNæsteSektion() {
    if (currentIndex < sections.length - 1) {
      currentIndex++;
      sections[currentIndex].scrollIntoView({ behavior: 'smooth' });
    }
  }

  // Funktion til at rulle til forrige sektion
  function gåTilForrigeSektion() {
    if (currentIndex > 0) {
      currentIndex--;
      sections[currentIndex].scrollIntoView({ behavior: 'smooth' });
    }
  }

  // Eventlytter for højre knap
  goRightBtn.addEventListener("click", gåTilNæsteSektion);

  // Eventlytter for venstre knap
  goLeftBtn.addEventListener("click", gåTilForrigeSektion);
});

  ```

### "Going forward"
- A colour theme should be decided upon.
- Create grids for the different segments of the page, so there will be space for text and image/video
 

<br>
<br>
<br>

## Update 0.0.2
> Added 12. March 2024 - 13:11

### Inspiration from "Omerko" Tutorial:
#### Base Code Implementation:
- Leveraging the horizontal scroll functionality demonstrated in the tutorial by "Omerko" on YouTube, the codebase has been adapted to incorporate similar scrolling behavior.
- Acknowledgment: The guide by "Omerko" serves as an inspiration, providing valuable insights into implementing horizontal scrolling and parallax effects.

#### Resource Reference:
- Tutorial: [Omerko - Horizontal Scroll Tutorial](https://www.youtube.com/watch?v=JgrZOom6jMg)
- CodePen Example: [Omerko's Horizontal Scroll CodePen](https://codepen.io/omerko96/pen/abNPMbb)

#### Other:
- The Javascript has been removed, and will probably be added at a later date. 

- The plan is to use the base he has created and start from there. The goal will to have a webpage that will move horizontally and have parallax. Hopefully, to make the page more 
  digestible and presentable for potential users.
