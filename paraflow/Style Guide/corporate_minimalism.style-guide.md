# Corporate Minimalism Style Guide

## Colors
### Primary Colors
  - **primary-base**: `text-[#1A2B4A]` or `bg-[#1A2B4A]` - Deep navy blue for headers, key text, and primary brand surfaces
  - **primary-lighter**: `bg-[#2A3B5A]`
  - **primary-darker**: `text-[#0F1A2E]` or `bg-[#0F1A2E]`

### Background Colors
- **bg-page**: `bg-[#F5F5F3]` - Light grey with subtle warmth
- **bg-container-primary**: `bg-white` - Main cards, content containers
- **bg-container-secondary**: `bg-[#FAFAF8]`
- **bg-section-alternate**: `bg-[#F0F0ED]` - Alternating sections for visual separation

### Text Colors
- **color-text-primary**: `text-[#1A1A1A]`
- **color-text-secondary**: `text-[#4A4A4A]`
- **color-text-tertiary**: `text-[#6A6A6A]`
- **color-text-quaternary**: `text-[#9A9A9A]`
- **color-text-on-dark-primary**: `text-white` - Text on dark backgrounds and primary-base surfaces
- **color-text-on-dark-secondary**: `text-white/80` - Text on dark backgrounds and primary-base surfaces
- **color-text-link**: `text-[#1A2B4A]` - Links, text-only buttons without backgrounds, and clickable text

### Functional Colors
Use sparingly to maintain minimalist aesthetic. Used for status indicators and critical alerts only.
  - **color-success-default**: #2C7A4F
  - **color-success-light**: #E8F5E9
  - **color-error-default**: #C62828
  - **color-error-light**: #FFEBEE
  - **color-warning-default**: #F57C00
  - **color-warning-light**: #FFF3E0
  - **color-function-default**: #1565C0
  - **color-function-light**: #E3F2FD

### Accent Colors
  - **accent-gold**: `text-[#B8935C]` or `bg-[#B8935C]` - Metallic gold used sparingly for premium highlights and CTAs
  - **accent-gold-light**: `bg-[#D4BA8F]`

### Data Visualization Charts
  - Standard data colors: #1A2B4A, #2A3B5A, #4A5B7A, #6A7B9A, #8A9BBA, #AABBDA
  - Accent data: #B8935C, #D4BA8F, #2C7A4F, #4A9A6F

## Typography
- **Font Stack**:
  - **font-family-base**: `-apple-system, BlinkMacSystemFont, "Segoe UI", "Helvetica Neue", Arial, sans-serif` — For all UI text

- **Font Size & Weight**:
  - **Caption**: `text-xs font-normal`
  - **Body small**: `text-sm font-normal`
  - **Body default**: `text-base font-normal`
  - **Card Title / Emphasized Text**: `text-base font-semibold`
  - **Page Title**: `text-2xl font-semibold`
  - **Headline**: `text-4xl font-semibold`
  - **Display**: `text-5xl font-semibold`

- **Line Height**: 1.4

## Border Radius
  - **None**: 0px — All elements maintain sharp, clean edges for systematic precision
  - **Minimal**: 2px — Only for input fields and buttons when subtle softening is needed

## Layout & Spacing
  - **Spacing Scale**:
  - **Base Unit**: 4px
  - **Tight**: 8px - For closely related elements within components
  - **Compact**: 16px - For component internal spacing
  - **Standard**: 24px - For section spacing and card padding
  - **Spacious**: 40px - For major section separation
  - **Extra Spacious**: 64px - For primary page sections

## Create Boundaries (contrast of surface color, borders, shadows)
Boundaries created primarily through surface color contrast and structured grid-based separation. Minimal use of borders for utmost clarity.

### Borders
  - **case 1**: No borders - Primary approach using surface color contrast only
  - **case 2**: If needed for critical separation
    - **Default**: 1px solid #E0E0DC - Used sparingly for inputs and tables. `border border-[#E0E0DC]`
    - **Stronger**: 1px solid #1A2B4A - Used for emphasis or active states. `border border-[#1A2B4A]`

### Dividers
  - **case 1**: No dividers - Prefer surface color separation
  - **case 2**: If needed for structured data tables or lists, `border-t` or `border-b` `border-[#E0E0DC]`

### Shadows & Effects
  - **case 1**: No shadows - Primary approach for flat, systematic design
  - **case 2 (subtle elevation)**: shadow-[0_1px_3px_rgba(26,43,74,0.08)] - Used only for elevated cards or modals when hierarchy requires it

## Assets
### Image
- For normal `<img>`: object-cover
- For `<img>` with:
  - Slight overlay: object-cover brightness-90
  - Heavy overlay: object-cover brightness-75

### Logo
- To protect copyright, do **NOT** use real product logos as a logo for a new product, individual user, or other company products.
- **Icon-based**:
  - **Graphic**: Use a simple, professional FontAwesome Solid icon (e.g., `fa-broom` for cleaning services, `fa-shield-alt` for trust/reliability).

### Icon
- Use Material Design Icons - default (no suffix) from Iconify for sharp, professional appearance.
- To ensure aesthetic layout, each icon should be centered in a square container matching the icon's size. This container is only for layout optimization and does not imply the icon has a background; other properties should be determined based on actual needs.
- Use Tailwind font size to control icon size
- Example:
  ```html
  <div class="flex items-center justify-center bg-transparent w-4 h-4">
  <iconify-icon icon="mdi:broom" class="text-base"></iconify-icon>
  </div>
  ```

## Basic Layout - Web

<!-- Critical Note: **MUST** follow the layout rules. -->
- Vertical Layout:
  - body (w-[1440px])
    - Header (Fixed height w-full) <!-- bg: bg-white-->
    - Content Container(w-full flex):
      - Left Sider - if present (flex-shrink-0 min-w-fit max-w-xs) <!-- bg: bg-[#FAFAF8]-->
      - Main Content Area (flex-1 overflow-x-hidden)
      - Right Sider - if present (flex-shrink-0 min-w-fit max-w-xs) <!-- bg: bg-[#FAFAF8]-->
    - Footer - if present (Fixed height w-full)

- Horizontal Layout (at least one of the left/right siders must be present, or both):
  - body (w-[1440px] flex)
    - Left Sider (Optional)<!-- bg: bg-white-->
    - content container:
      - Header (Optional)<!-- bg: bg-[#FAFAF8]-->
      - main content area
      - Footer (Optional)
    - Right Sider (Optional)

## Page Layout - Web (*EXTREMELY* important)

```html
<!-- standard implementation for body. A specific body width needs to be defined, which changes based on user requirements -->
<body class="w-[1440px] min-h-[900px] font-[-apple-system,BlinkMacSystemFont,'Segoe_UI','Helvetica_Neue',Arial,sans-serif] leading-[1.4]">

</body>
```

## Tailwind Component Examples
<!-- Important Note: Use utility classes directly. Do NOT create custom CSS classes or add styles in <style> tags -->
### Basic
- **Button**:
  - example 1(primary button):
    - button: flex items-center bg-[#1A2B4A] text-white px-6 py-3 hover:bg-[#2A3B5A]
      - span: Request Quote
  - example 2(secondary button):
    - button: flex items-center bg-white text-[#1A2B4A] border border-[#1A2B4A] px-6 py-3 hover:bg-[#F5F5F3]
      - span: Learn More
  - example 3(accent button - use sparingly):
    - button: flex items-center bg-[#B8935C] text-white px-6 py-3 hover:bg-[#D4BA8F]
      - span: Get Started
  - example 4(text button):
    - button: flex items-center text-[#1A2B4A] hover:text-[#2A3B5A]
      - span: View All Services
  - example 5(icon button):
    - button: flex items-center justify-center w-10 h-10 bg-white text-[#1A2B4A] hover:bg-[#F5F5F3]
      - icon

- **Label/Tag/Badge**:
    - div: flex items-center bg-[#F0F0ED] text-[#4A4A4A] px-3 py-1 text-xs font-medium
      - span: Professional

### Data Entry
- **Input Field**:
  - input: border border-[#E0E0DC] bg-white px-4 py-3 text-base focus:border-[#1A2B4A] focus:outline-none

- **Progress bars**: h-2 bg-[#E0E0DC]
  - progress fill: bg-[#1A2B4A]

- **Checkbox and radio button**
  - default: bg-white border border-[#E0E0DC]
  - checked: bg-[#1A2B4A] border-[#1A2B4A]; text-white

### Container
- **Navigation Menu - horizontal**
    - example 1(Basic horizontal navigation):
        - Nav Container: flex items-center gap-10
        - Menu Item: flex items-center text-base font-medium text-[#1A1A1A] hover:text-[#1A2B4A]
          - menu-text
    - example 2(Navigation with sections/grouping):
        - Nav Container: flex items-center justify-between w-full
        - Left Section: flex items-center gap-10
          - Menu Item: flex items-center text-base font-medium text-[#1A1A1A] hover:text-[#1A2B4A]
        - Right Section: flex items-center gap-6
          - Contact Button: flex items-center bg-[#B8935C] text-white px-6 py-2 hover:bg-[#D4BA8F]

- **Card**
    - example 1(Service card - vertical with icon):
        - Card: bg-white flex flex-col p-8 gap-6
        - Icon Container: flex items-center justify-center w-12 h-12 bg-[#F5F5F3]
          - icon: text-2xl text-[#1A2B4A]
        - Text area: flex flex-col gap-3
          - card-title: text-base font-semibold text-[#1A1A1A]
          - card-description: text-sm text-[#4A4A4A]
    - example 2(Testimonial card - horizontal):
        - Card: bg-white flex p-8 gap-6 border-l-2 border-[#B8935C]
        - Text area: flex flex-col gap-4
          - quote: text-base text-[#1A1A1A]
          - author: text-sm font-medium text-[#4A4A4A]
    - example 3(Stats card - minimal):
        - Card: flex flex-col gap-2 p-6
        - Number: text-4xl font-semibold text-[#1A2B4A]
        - Label: text-sm text-[#6A6A6A]

## Additional Notes

This style guide emphasizes systematic precision and disciplined clarity through:
- Sharp edges (0-2px radius) for professional, structured appearance
- Generous whitespace using the defined spacing scale for breathing room
- Surface color contrast as primary boundary creation method
- Minimal decorative elements - every element serves a functional purpose
- Grid-based layouts with clear alignment and hierarchy
- Restrained use of metallic gold accent to maintain sophistication
- Deep navy blue as the authoritative brand anchor
- Clean typography hierarchy for scannable, professional content

<colors_extraction>
#1A2B4A
#2A3B5A
#0F1A2E
#F5F5F3
#FFFFFF
#FAFAF8
#F0F0ED
#1A1A1A
#4A4A4A
#6A6A6A
#9A9A9A
#E0E0DC
#2C7A4F
#E8F5E9
#C62828
#FFEBEE
#F57C00
#FFF3E0
#1565C0
#E3F2FD
#B8935C
#D4BA8F
#4A5B7A
#6A7B9A
#8A9BBA
#AABBDA
#4A9A6F
</colors_extraction>
