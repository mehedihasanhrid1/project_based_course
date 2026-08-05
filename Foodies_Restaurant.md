# Assignment: Build **Foodie's Restaurant** Website (HTML & CSS Only)

**Total Marks: 100**

## Objective

Build a responsive restaurant landing page named **Foodie's Restaurant**
using **HTML5** and **CSS3** only. JavaScript is **not allowed**.

## Requirements

### 1. Navigation Bar (10 Marks)

-   Logo
-   Links: Home, About, Menu, Gallery, Reviews, Contact
-   Sticky navigation using CSS

### 2. Hero Section (15 Marks)

-   Heading
-   Short description
-   Call-to-action button
-   One restaurant image

### 3. About Section (10 Marks)

-   Restaurant description
-   One image
-   Button

### 4. Menu Section (20 Marks)

Create at least **6 food cards**. Each card must contain: - Food image -
Food name - Description - Price

### 5. Gallery (10 Marks)

Display at least **6 food images** using CSS Grid.

### 6. Customer Reviews (10 Marks)

Display at least **3 customer review cards** with: - Customer image -
Name - Review

### 7. Contact Section (10 Marks)

Include: - Restaurant address - Phone - Email - Contact form (Name,
Email, Message, Submit button)

### 8. Footer (5 Marks)

Include copyright information.

### 9. Responsive Design (10 Marks)

-   Mobile friendly
-   Tablet friendly
-   Desktop friendly
-   Use Flexbox and/or CSS Grid

## Technical Requirements

-   HTML5 semantic tags
-   External CSS (`style.css`)
-   No JavaScript
-   Use `object-fit: cover` for images
-   Organize code with proper indentation
-   Add comments for each major section

## Suggested Folder Structure

``` text
Restaurant-Website/
│
├── index.html
├── style.css
└── images/
```

## Demo HTML Code

``` html
<section class="menu-card">
    <img src="" alt="Food Image">

    <h3>Grilled Steak</h3>

    <p>Fresh grilled steak served with vegetables.</p>

    <span>$24</span>
</section>
```

## Demo CSS Code

``` css
.menu-card{
    background:#fff;
    border-radius:15px;
    overflow:hidden;
}

.menu-card img{
    width:100%;
    height:220px;
    object-fit:cover;
}
```

## Marking Rubric

  Criteria                      Marks
  ------------------------- ---------
  HTML Structure                   20
  CSS Styling                      25
  Responsive Design                15
  Menu & Gallery                   15
  Contact & Footer                 10
  Code Quality & Comments          10
  Creativity                        5
  **Total**                   **100**

## Submission

Submit: 1. `index.html` 2. `style.css` 3. `images` folder (or image
links)

Good luck and focus on writing clean, well-structured HTML and CSS.
