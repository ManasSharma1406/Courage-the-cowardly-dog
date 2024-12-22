# Courage-the-cowardly-dog



Here's the updated explanation for your repository, incorporating the **CSS** file and providing a detailed description of the styles used in your project:

---

# **Courage the Cowardly Dog Tribute Website**

## **Overview**  
This project is a tribute to the iconic cartoon series *Courage the Cowardly Dog*. The website uses HTML, CSS, and JavaScript, along with libraries like **GSAP** and **Locomotive Scroll**, to create an interactive, nostalgic, and eerie design. This project showcases advanced CSS techniques and JavaScript functionalities to deliver a seamless and visually engaging user experience.

---

## **Features**

### 1. **Dynamic Layout with Styling**
   - **Custom Font Integration:**  
     - The `Parkinsans` font is imported using the `@font-face` rule for a unique visual identity that aligns with the spooky theme.  
     - Ensures consistent typography throughout the website.

   - **Custom Styling for Each Section:**  
     - `#page`, `#page1`, `#page2`, and `#page3` are styled distinctly to provide variety while maintaining a cohesive design.  
     - Uses `background-image`, `text-shadow`, and advanced CSS effects for visual appeal.

### 2. **Smooth Scrolling with Locomotive Scroll**  
   - **Locomotive Scroll Library:** Enables smooth, buttery scrolling across the website.  
   - Integrated with **GSAP ScrollTrigger** to handle animations dynamically during scroll events.

### 3. **Interactive Parallax Effect**
   - JavaScript-powered parallax effect for the image in the `#page` section.  
   - The image moves slightly in response to mouse movements, creating a 3D-like interaction.

### 4. **Eerie Aesthetic with CSS**
   - Use of color themes like `#ec1994e1` (pink), `#0F34B4` (dark blue), and `#2f92c9` (teal) to maintain the eerie vibe of the Courage series.  
   - **Blurred Background Videos:** Adds an immersive layer to the visuals.  
   - **Drop Shadow and Filters:** Enhance images and text for a dramatic look.

---

## **Code Explanation**

### **HTML Structure**
- **Sections (`#page`, `#page1`, `#page2`, `#page3`):**  
  Each section is a vertical block with unique content such as images, text, and facts about the series.

- **Navigation Bar (`#nav`):**  
  Includes links for easy navigation and features a centered menu for a clean, symmetrical design.

- **Image Placement:**  
  Strategic use of absolute positioning ensures that images like Courage and the founders align perfectly with the theme.

---

### **CSS Breakdown**
- **Global Styles:**  
  - **Custom Font:** `@font-face` defines a spooky font for the entire website.  
  - **Universal Reset:** Margins and paddings are reset using `* { margin: 0; padding: 0; }` to avoid cross-browser inconsistencies.  
  - **Full-Screen Sections:** Each section is styled to occupy the full viewport (`height: 100vh; width: 100vw;`).

- **Video Background (`video`):**  
  - A blurred video serves as the background to create a mysterious and immersive atmosphere.  
  - **CSS Properties:**  
    ```css
    video {
        filter: blur(4px);
        object-fit: cover;
        width: 100vw;
        height: 100vh;
    }
    ```

- **Parallax Image Styling (`#page>img`):**  
  - Positioned with margins to create a visually appealing offset.  
  - Parallax effect is implemented with smooth transitions using:
    ```css
    transition: all cubic-bezier(0.19, 1, 0.22, 1) 1s;
    ```

- **Creepy Fact Section (`#page1`):**  
  - A background image fills the entire viewport with `background-size: cover`.  
  - Green-highlighted `h6` with a custom underline effect adds a unique design element:
    ```css
    #page1>h6::after {
        content: '';
        position: absolute;
        background-color: #00ff11;
        transform: skewY(-16deg);
    }
    ```

- **Founders Section (`#page2`):**  
  - Images of the founders are placed using `absolute` positioning for a creative layout.  
  - Center-aligned text with color accents complements the section design.

- **Final Section (`#page3`):**  
  - Minimalistic design with a centered image and large heading (`h3`).  
  - Styled for impact using large fonts and vibrant colors.

---

### **JavaScript Functionality**
- **Locomotive Scroll Integration:**  
   Enables smooth scrolling and synchronization with **GSAP ScrollTrigger**.

- **Mouse Movement Parallax Effect:**  
   - Reacts to cursor movements to adjust the position of the image dynamically:
     ```javascript
     main.addEventListener("mousemove", function(dets) {
         image.style.top = 1 - dets.y * 0.09 + "px";
         image.style.left = 1 - dets.x * 0.09 + "px";
     });
     ```

---

## **How to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/YourUsername/Courage-The-Cowardly-Dog.git
   cd Courage-The-Cowardly-Dog
   ```

2. Open the `index.html` file in a browser to view the site.

3. Ensure an active internet connection for external libraries like GSAP and Locomotive Scroll. Alternatively, download and link them locally.

---

## **Future Enhancements**
- Add additional sections with trivia or Easter eggs about the show.  
- Implement a gallery for fan art submissions.  
- Add sound effects to enhance the immersive experience.  

---

Let me know if you need further refinements or additional suggestions for enhancing your project!
