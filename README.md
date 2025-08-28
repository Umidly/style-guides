# Umidly Style Guides

This repository contains the official style guides for Umidly, ensuring consistency across all our products, communications, and codebases. Adhering to these guidelines helps us maintain a unified brand identity and deliver a cohesive user experience.

### Logo Usage

[Provide guidelines on how to use the Umidly logo, including minimum size, clear space, and variations (e.g., primary, secondary, icon). Include examples of correct and incorrect usage. The logo image height is typically 40px (desktop) and 30px (mobile).]

### Color Palette

In Umidly, we use a clean and modern color palette, focusing on pleasant, simple colors with gradients to highlight key elements.

| Color Name | HEX | RGB | Usage |
| :--------- | :-- | :-- | :---- |
| White      | #FFFFFF | (255,255,255) | Backgrounds, primary surfaces |
| Dark Grey  | #202124 | (32,33,36) | Primary text, headings |
| Grey       | #5F6368 | (95,99,104) | Secondary text, links, descriptions |
| Blue       | #1A73E8 | (26,115,232) | Primary accent, interactive elements, highlights |
| Light Blue | #4285F4 | (66,133,244) | Gradient component |
| Cyan       | #00BCD4 | (0,188,212) | Gradient component |
| Light Cyan | #26C6DA | (38,198,218) | Gradient component |
| Light Grey | #E8EAED | (232,234,237) | Borders, separators |
| Very Light Grey | #F8F9FA | (248,249,250) | Section backgrounds |
| Transparent White | rgba(255,255,255,0.95) | | Navigation background with blur |
| Transparent Blue | rgba(26,115,232,0.08) | | Hover states |

### Typography

Umidly primarily uses the 'Poppins' font for all text elements, ensuring a clean and modern aesthetic. Line heights are generally set to enhance readability.

*   **Font Family:** 'Poppins', sans-serif
*   **Body Text:**
    *   Paragraph: `font-size: 1rem` (default browser size), `line-height: 1.6`
*   **Headings:**
    *   H1 (`.hero-title`): `clamp(3rem, 7vw, 5.5rem)`, `font-weight: 600`, `line-height: 1.1`, `letter-spacing: -0.02em`
    *   H2 (`.section-title`): `2.5rem` (desktop), `2rem` (mobile), `font-weight: 500`
*   **Subtitles/Descriptions:**
    *   `.hero-subtitle`: `clamp(1.1rem, 2.2vw, 1.3rem)`, `font-weight: 400`, `line-height: 1.7`
    *   `.section-subtitle`: `1.2rem`, `font-weight: 400`
*   **Navigation Links:** `0.9rem`, `font-weight: 500`
*   **Logo Text:** `24px`, `font-weight: 600`
*   **Feature Icon:** `1.5rem`
*   **Stats:**
    *   Number: `2.5rem`, `font-weight: 900`
    *   Label: `0.9rem`, `font-weight: 500`

## Voice & Tone

*   **Overall Tone:** [e.g., Friendly, Professional, Empowering, Innovative]
*   **Key Characteristics:** [e.g., Clear, Concise, Empathetic, Optimistic]
*   **Examples:**
    *   *Do:* "Welcome to Umidly! We're excited to help you..."
    *   *Don't:* "Hey there, user. Get ready for some stuff."

## Design Principles

Umidly's design is guided by principles that prioritize user experience and visual appeal.

*   **User-Centric:** Always design with the user's needs and goals in mind.
*   **Simplicity:** Strive for clarity and ease of use, avoiding unnecessary complexity.
*   **Consistency:** Maintain a consistent look, feel, and behavior across all touchpoints.
*   **Clarity:** Ensure information is easily understandable and actions are intuitive.
*   **Elegance:** Aim for aesthetically pleasing and refined designs.
*   **Responsive Design:** Adapt layouts and elements seamlessly across various screen sizes using media queries.
*   **Modern Aesthetics:** Utilize subtle effects like `backdrop-filter` for navigation, `border-radius` for rounded corners (e.g., `12px` for cards, `24px` for buttons), and `box-shadow` for depth.
*   **Smooth Interactions:** Employ CSS `transition` properties for smooth hover effects and animations.
*   **Flexible Layouts:** Extensive use of `flexbox` for efficient and adaptable content arrangement.

This guide is a living document and will evolve as Umidly grows. For any questions or suggestions, please contact [relevant team/person].

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.