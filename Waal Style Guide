# 🎨 Waal.ai Design System Guide

## 📌 Introduction
This design system outlines the core styling guidelines for Waal.ai’s user interface. It ensures consistency in colors, typography, spacing, and component usage across all platforms. **For the app context, Waal.ai prefers a white background and Navy Blue (#001F42) for primary CTA buttons.**

---

## 🎨 Colors

### Brand Colors
| Name               | Hex        | Notes                                            |
|--------------------|-----------|--------------------------------------------------|
| Navy Blue          | `#002B5C` | Primary brand color for backgrounds/headers      |
| Navy Blue (Darker) | `#001F42` | **Used for CTA buttons and key interactive UI**  |
| Light Variant      | `#E6EDF5` | Light variant for subtle backgrounds/borders     |

> **App Usage**:  
> - **White (`#FFFFFF`)** as the main screen background.  
> - **Navy Blue (Darker)** (`#001F42`) for primary CTA buttons.  
> - Use **Light Variant** (`#E6EDF5`) sparingly for subtle sections or containers.

### Accent Colors
| Color   | Hex        | Usage                                                                     |
|---------|-----------|---------------------------------------------------------------------------|
| Orange  | `#FF7F41` | Accent color for secondary buttons, small interactive elements, highlights |
| Gold    | `#FFC107` | Secondary accent for hover states, highlights, or alert badges             |

> **App Usage**:  
> - Use **Orange** or **Gold** only as accent colors.  
> - Keep usage minimal to avoid overpowering the primary brand colors.  


### Gray Scale
A consistent range of grays is essential for **borders**, **text**, **backgrounds**, and **disabled states**.

| Name      | Hex       | Usage                                              |
|-----------|----------|-----------------------------------------------------|
| Gray 50   | `#FAFAFA` | Very light gray for backgrounds or hover overlays  |
| Gray 100  | `#F5F5F5` | Subtle background sections and dividers            |
| Gray 200  | `#EEEEEE` | General borders, light dividers, backgrounds       |
| Gray 300  | `#E0E0E0` | Slightly darker borders, background fill           |
| Gray 400  | `#BDBDBD` | Disabled element states or placeholders            |
| Gray 500  | `#9E9E9E` | Secondary text, icons, or subdued labels           |
| Gray 600  | `#757575` | Body text on very light backgrounds                |
| Gray 700  | `#616161` | Darker text, subtitles, or headings on light BG    |
| Gray 800  | `#424242` | High-contrast text on lighter grays                |
| Gray 900  | `#212121` | Near-black, for very prominent text                |

> **Tip**: Select gray shades based on required contrast. For example, use **Gray 700** or **Gray 800** for text on white backgrounds.

### Status Colors
These colors are used to convey **semantic meaning** such as success, error, warning, or informational states.

| Name     | Hex       | Usage                                          |
|----------|-----------|-----------------------------------------------|
| Success  | `#28A745` | Indicate successful operations or confirmations|
| Error    | `#DC3545` | Critical issues, errors, or destructive actions|
| Warning  | `#FFC107` | Non-critical alerts, warnings, or caution      |
| Info     | `#17A2B8` | Informational messages or neutral alerts       |

> **App Usage**:  
> - Use these colors in **text**, **icons**, or **background fills** for messages, alerts, tooltips, and badges.  
> - Always ensure the text or icon color provides sufficient contrast against its background.


### Theme Colors
While Waal.ai primarily uses a **light theme**, a dark variant or additional themes may be considered in the future. Below are guidelines for the default light theme and a sample dark theme.

#### Light Theme (Default)
| Element                | Color         | Notes                                                |
|------------------------|--------------|------------------------------------------------------|
| **Primary Background** | `#FFFFFF`    | Main screen background                               |
| **Secondary Background** | `#E6EDF5`  | Subtle sections, modals, or highlighted containers   |
| **Text (Default)**     | `#212121` or Gray 900  | High contrast on white                               |
| **CTA Buttons**        | `#001F42`    | Navy Blue (Darker)                                  |
| **Accents**            | `#FF7F41`, `#FFC107` | Orange/Gold for highlights, icons, or secondary buttons|

#### Dark Theme (Future/Optional)
| Element                | Color         | Notes                                                   |
|------------------------|--------------|---------------------------------------------------------|
| **Primary Background** | `#121212`    | Dark background                                        |
| **Secondary Background** | `#1E1E1E` or Gray 900 | Contrasted sections or containers                  |
| **Text (Default)**     | `#FFFFFF`    | White text on dark background                           |
| **CTA Buttons**        | `#001F42` or `#FFC107`  | Navy or Gold can still work for CTAs                  |
| **Accents**            | `#FF7F41` or `#FFC107`  | Use bright accents sparingly for clarity              |

> **Tip**: For a dark theme, ensure **sufficient contrast** by adjusting accent colors or text color to meet WCAG standards.

---

## 🔤 Typography

### Font Family
Using a modern system font stack for optimal performance:
```css
font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
  Oxygen, Ubuntu, Cantarell, 'Fira Sans', 'Droid Sans', 'Helvetica Neue',
  sans-serif;
```

### Font Sizes
| Element    | Class         | REM   | Notes                       |
|------------|--------------|-------|-----------------------------|
| H1         | `text-4xl`   | 2.25  | Main page title             |
| H2         | `text-3xl`   | 1.875 | Section headings            |
| H3         | `text-xl`    | 1.25  | Subsection or card headings |
| Body (Base)| `text-base`  | 1.0   | Default text size           |
| Small      | `text-sm`    | 0.875 | Smaller text                |
| Large      | `text-lg`    | 1.125 | Emphasis text               |

### Font Weights
| Weight    | Class           | Numeric |
|-----------|-----------------|---------|
| Regular   | `font-normal`   | 400     |
| Medium    | `font-medium`   | 500     |
| Semibold  | `font-semibold` | 600     |
| Bold      | `font-bold`     | 700     |

> **Line Heights**: No specific information provided.

---

## 📏 Spacing

### Padding
| Size         | Classes  | REM   |
|--------------|---------|-------|
| Extra Small  | `p-2`   | 0.5   |
| Small        | `p-4`   | 1.0   |
| Medium       | `p-6`   | 1.5   |
| Large        | `p-8`   | 2.0   |

### Margins
| Size         | Classes  | REM   |
|--------------|---------|-------|
| Extra Small  | `m-2`   | 0.5   |
| Small        | `m-4`   | 1.0   |
| Medium       | `m-6`   | 1.5   |
| Large        | `m-8`   | 2.0   |

### Gap
| Size   | Classes   | REM   |
|--------|----------|-------|
| Small  | `gap-4`  | 1.0   |
| Medium | `gap-6`  | 1.5   |
| Large  | `gap-8`  | 2.0   |

---

## 🔲 Border Radius
| Size          | Class          | REM   |
|---------------|---------------|-------|
| Default       | `rounded-xl`  | 0.75  |
| Large         | `rounded-2xl` | 1.0   |
| Extra Large   | `rounded-3xl` | 1.5   |

---

## 🌫️ Shadows
| Element       | Class                                   |
|---------------|-----------------------------------------|
| Card Shadow   | `shadow-lg`                             |
| Button Shadow | `shadow-lg shadow-accent-orange/25`     |

> **App Usage**: For CTA buttons (Navy Blue), consider a subtle drop shadow with `rgba(0, 0, 0, 0.1)` if using a white background to maintain focus without overwhelming.

---

## 🔘 Button Guidelines (App-Specific)

### Primary CTA Button
- **Color**: Navy Blue (Darker) `#001F42`
- **Text Color**: White `#FFFFFF`
- **Hover State**:
  - Slightly lighter shade: e.g., `#002D55` or 90% opacity of `#001F42`
  - Cursor: `pointer`
  - Transition: `transition-all duration-300`
- **Focus State**:
  - Outline or border: 2px solid `#FF7F41` (Orange) or a lighter navy for accessibility.
- **Disabled State**:
  - Lighter background: e.g., `#A3B3CA`
  - Text color: `#F0F0F0` or a neutral gray.
  - Cursor: `not-allowed`

### Secondary Button (Accent)
- **Color**: Orange `#FF7F41` or Gold `#FFC107`
- **Text Color**: White `#FFFFFF` or Navy `#001F42` (depending on contrast needs)
- Use these **only when needed** to draw attention to secondary actions, not to overshadow the primary CTA.

### Tertiary Button (Text Only / Minimal)
- **Color**: Navy Blue `#002B5C` or a dark gray
- **Background**: Transparent or white
- **Border**: 1px `#E6EDF5` or similar if needed
- Used for less prominent actions, links, or “cancel” buttons.

---

## ✅ Usage Guidelines
1. **Layout & Grid**  
   - Use a container with `max-w-6xl` and `px-4 md:px-6` for responsive layouts.  
   - Two-column layouts might use `grid lg:grid-cols-[1.1fr,0.9fr]`.

2. **White Background**  
   - **Default**: White (`#FFFFFF`) for the app’s main screens to maintain clarity and contrast.  
   - Light backgrounds (`#E6EDF5`) may be used for sections or modals.

3. **CTA & Interactive Elements**  
   - **Primary CTA**: Navy Blue (Darker) `#001F42`.  
   - **Accent Colors** (`#FF7F41`, `#FFC107`) for secondary actions or highlights.

4. **Responsive Breakpoints**  
   - Use `md:` for tablets (≥768px) and `lg:` for desktops (≥1024px).  
   - Ensure consistent spacing and sizing across breakpoints.

5. **Animation**  
   - Prefer `transition-all duration-300` for smooth hover/focus states.

6. **Accessibility**  
   - Maintain **high contrast** for text (WCAG 2.1 AA or better).  
   - Provide clear focus states for interactive elements.  
   - Use semantic HTML and appropriate ARIA attributes.  
   - Verify designs on multiple screen sizes and devices.

7. **Best Practices**  
   1. Use semantic HTML elements for improved accessibility.  
   2. Keep spacing consistent.  
   3. Follow the color hierarchy to highlight important UI elements.  
   4. Ensure text readability with sufficient contrast.  
   5. Apply hover, focus, and active states consistently.

---

### Conclusion
With these **extended color guidelines**, including **Gray Scale**, **Status Colors**, and **Theme Colors**, Waal.ai’s design system covers a broader range of scenarios and maintains a cohesive, accessible user experience across both **light** and potential **dark** themes.

