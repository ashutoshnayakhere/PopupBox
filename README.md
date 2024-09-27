# PopupBox

![image](https://github.com/user-attachments/assets/b26f0010-b3c3-4783-8e6d-aeea6c6eb6c1)

### Popup Modal Documentation

This HTML document creates a simple interactive popup modal. When a user clicks the "Submit" button, a popup appears thanking the user for submitting their details. The popup can be closed by clicking the "OK" button.

#### HTML Structure:

- **DOCTYPE Declaration and HTML Tags:**
  - The `<!DOCTYPE html>` declaration defines the document type.
  - The `<html>` element defines the root of the HTML document.
  - The document uses the English language as indicated by the `lang="en"` attribute in the `<html>` tag.

- **Head Section:**
  - Contains `<meta>` tags for character encoding (`<meta charset="UTF-8">`), browser compatibility (`<meta http-equiv="X-UA-Compatible" content="IE=edge">`), and viewport settings for responsive design (`<meta name="viewport" content="width=device-width, initial-scale=1.0">`).
  - A `<style>` block is used for inline CSS to define the appearance of the page.

#### CSS (Style):

The CSS block controls the layout and styling of the modal, button, and overall page.

- **Global Styling (`*` selector):**
  - `margin: 0; padding: 0;` ensures no default margin or padding across elements.
  - `box-sizing: border-box;` ensures that padding and borders are included in the element's total width and height.

- **Container Styling (`.container`):**
  - The container covers the entire viewport (`width: 100%; height: 100vh;`) and has a background color of `#3c5077`.
  - It uses `display: flex; align-items: center; justify-content: center;` to center the button both vertically and horizontally within the page.

- **Button Styling (`.btn`):**
  - A button with padding (`padding: 10px 60px;`) and rounded corners (`border-radius: 30px;`) is centered.
  - The button has a white background (`background: #fff;`), no border (`border: 0;`), and an increased font size for visibility (`font-size: 22px; font-weight: 500;`).
  - The cursor turns into a pointer when hovered over the button (`cursor: pointer;`).

- **Popup Modal Styling (`.popup`):**
  - The popup is initially hidden and positioned outside the view with `visibility: hidden;` and `top: 0; left: 50%; transform: translate(-50%, -50%) scale(0.1);`.
  - When visible, it scales to full size and is positioned at the center of the screen using the class `.open-popup`.
  - The popup has a width of 400px and is styled with a white background, rounded corners (`border-radius: 8px;`), and padding for inner space (`padding: 0 30px 30px;`).
  
- **Popup Elements:**
  - **Image (`.popup img`)**: Displays a checkmark image with a width of 100px, round corners (`border-radius: 50%;`), and a slight shadow for a 3D effect.
  - **Heading (`.popup h2`)**: Displays the thank you message with a large font size (`font-size: 38px`) and margin for spacing.
  - **Popup Button (`.popup button`)**: A green button inside the popup with a white font color. When clicked, it closes the popup.

#### JavaScript (Script):

The JavaScript is embedded in the document and handles the logic for opening and closing the popup.

- **Variable Declaration:**
  ```javascript
  let popup = document.getElementById("popup");
  ```
  - This selects the popup `<div>` by its `id="popup"` and assigns it to the `popup` variable for later manipulation.

- **Open Popup Function (`openPopup`):**
  ```javascript
  function openPopup() {
      popup.classList.add("open-popup");
  }
  ```
  - When the "Submit" button is clicked, this function adds the `open-popup` class to the `popup` element. This changes the popup's visibility and transforms it into a fully visible modal.

- **Close Popup Function (`closePopup`):**
  ```javascript
  function closePopup() {
      popup.classList.remove("open-popup");
  }
  ```
  - When the "OK" button is clicked within the popup, this function removes the `open-popup` class, hiding the popup by resetting its position and scale.

#### Interaction Flow:

1. **Initial State:**
   - The popup is hidden using the `visibility: hidden;` CSS rule, and its size is reduced with `scale(0.1)`.

2. **Opening the Popup:**
   - When the user clicks the "Submit" button, the `openPopup()` function is called, adding the `open-popup` class to the popup, which makes the popup visible and scales it to its full size (`scale(1)`).

3. **Closing the Popup:**
   - The user can close the popup by clicking the "OK" button, which triggers the `closePopup()` function, removing the `open-popup` class and returning the popup to its hidden state.

#### Summary:

This code provides a simple modal popup interaction for a webpage. It features:
- A flexbox layout for centering content.
- A neumorphism-inspired button for triggering the popup.
- JavaScript functions to handle the opening and closing of the modal.
- CSS to ensure smooth scaling transitions and visibility control.
