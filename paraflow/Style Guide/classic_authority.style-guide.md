# Editorial Authority Style Guide

## Colors
### Primary Colors
  - **primary-base**: `text-[#3A5A78]` or `bg-[#3A5A78]` - Steel blue for trustworthy authority
  - **primary-lighter**: `bg-[#5A7A98]`
  - **primary-darker**: `text-[#2A4A68]` or `bg-[#2A4A68]`

### Background Colors
- **bg-page**: `bg-white`
- **bg-container-primary**: `bg-white` - All containers match page background for editorial clarity
- **bg-container-secondary**: `bg-white`
- **bg-container-inset**: `bg-[#F8F9FA]` - Subtle gray for input fields
- **bg-container-inset-strong**: `bg-[#E9ECEF]` - For pressed states

### Text Colors
- **color-text-primary**: `text-[#1A1A1A]`
- **color-text-secondary**: `text-[#4A4A4A]`
- **color-text-tertiary**: `text-[#6A6A6A]`
- **color-text-quaternary**: `text-[#9A9A9A]`
- **color-text-on-dark-primary**: `text-white/95` - Text on steel blue backgrounds
- **color-text-on-dark-secondary**: `text-white/75` - Secondary text on steel blue backgrounds
- **color-text-link**: `text-[#3A5A78]` - Links and clickable text

### Functional Colors
Use sparingly to maintain editorial sophistication.
  - **color-success-default**: #2D5F3F
  - **color-success-light**: #E8F3EC - tag\label bg
  - **color-error-default**: #8B3A3A
  - **color-error-light**: #F8E8E8 - tag\label bg
  - **color-warning-default**: #8B7539
  - **color-warning-light**: #F8F3E8 - tag\label bg

### Accent Colors
  - **accent-forest**: `text-[#2D5F3F]` or `bg-[#2D5F3F]` - Deep forest green for secondary emphasis
  - **accent-forest-light**: `text-[#E8F3EC]` or `bg-[#E8F3EC]` - Subtle green backgrounds

## Typography
- **Font Stack**:
  - **font-family-base**: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial` — Clean sans-serif for editorial clarity

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
Minimal radius for timeless, institutional presentation.
  - **None**: 0px — Primary containers, cards, and structural elements
  - **Subtle**: 2px — Buttons and interactive elements
  - **Small**: 4px — Input fields and form elements
  - **Medium**: 6px — Small tags and badges

## Layout & Spacing
  - **Spacing Scale**:
  - **Base Unit**: 4px
  - **Tight**: 8px - For close-related elements
  - **Compact**: 12px - For list items and small gaps
  - **Standard**: 16px - For general padding, margins and section/module spacing
  - **Spacious**: 24px - For major section separation
  - **Generous**: 32px - For page-level spacing

## Create Boundaries (contrast of surface color, borders, shadows)
Fine-line borders create structured editorial outlines with no shadows. Surfaces match background for clean, authoritative presentation.

### Borders
  - **Default**: 1px solid #D1D5DB - Used for cards, sections, and structural divisions. `border border-gray-300`
  - **Stronger**: 1px solid #9CA3AF - Used for emphasized containers and active states. `border border-gray-400`
  - **Accent**: 2px solid #3A5A78 - Used sparingly for primary emphasis. `border-2 border-[#3A5A78]`

### Dividers
  - Use `border-t` or `border-b` with `border-gray-300` for section separation in editorial layouts.

### Shadows & Effects
  - **No shadows** - Maintain flat, editorial clarity with borders defining all boundaries.

## Assets
### Image
- For normal `<img>`: object-cover
- For `<img>` with:
  - Slight overlay: object-cover brightness-90
  - Heavy overlay: object-cover brightness-75

### Logo
- To protect copyright, do **NOT** use real product logos as a logo for a new product, individual user, or other company products.
- **Icon-based**:
  - **Graphic**: Use a simple, relevant FontAwesome Solid icon (e.g., `fa-broom` for cleaning services, `fa-shield-alt` for trust and protection).

### Icon
- Use Material Design Icons (default) from Iconify for sharp, professional clarity.
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
    - Header (Fixed height w-full) <!-- bg: bg-white with border-b border-gray-300-->
    - Content Container(w-full flex):
      - Left Sider - if present (flex-shrink-0 min-w-fit max-w-xs) <!-- bg: bg-white with border-r border-gray-300-->
      - Main Content Area (flex-1 overflow-x-hidden)
      - Right Sider - if present (flex-shrink-0 min-w-fit max-w-xs) <!-- bg: bg-white with border-l border-gray-300-->
    - Footer - if present (Fixed height w-full) <!-- bg: bg-white with border-t border-gray-300-->

- Horizontal Layout (at least one of the left/right siders must be present, or both):
  - body (w-[1440px] flex)
    - Left Sider (Optional)<!-- bg: bg-white with border-r border-gray-300-->
    - content container:
      - Header (Optional)<!-- bg: bg-white with border-b border-gray-300-->
      - main content area
      - Footer (Optional) <!-- bg: bg-white with border-t border-gray-300-->
    - Right Sider (Optional) <!-- bg: bg-white with border-l border-gray-300-->

## Page Layout - Web (*EXTREMELY* important)

```html
<!-- standard implementation for body. A specific body width needs to be defined, which changes based on user requirements -->
<body class="w-[1440px] min-h-[900px] font-[-apple-system,BlinkMacSystemFont,'Segoe_UI',Roboto,'Helvetica_Neue',Arial] leading-[1.4]">

</body>
```

## Tailwind Component Examples
<!-- Important Note: Use utility classes directly. Do NOT create custom CSS classes or add styles in <style> tags -->
### Basic
- **Button**:
  - example 1(Primary button):
    - button: flex items-center gap-2 px-6 py-3 bg-[#3A5A78] text-white/95 rounded-sm border border-[#3A5A78]
      - span: Request Quote (button copy)
  - example 2(Secondary button):
    - button: flex items-center gap-2 px-6 py-3 bg-white text-[#3A5A78] rounded-sm border border-gray-300
      - span: Learn More (button copy)
  - example 3(Text button):
    - button: flex items-center gap-1 text-[#3A5A78]
      - span: View Details (button copy)
      - icon: w-4 h-4
  - example 4(Icon button):
    - button: flex items-center justify-center w-10 h-10 bg-white border border-gray-300 rounded-sm
      - icon: w-5 h-5

- **Label/Tag/Badge**:
    - example 1(Standard tag):
      - div: flex items-center px-3 py-1 bg-[#E8F3EC] text-[#2D5F3F] text-sm rounded
        - span: 30 Years (copy)
    - example 2(Outlined tag):
      - div: flex items-center px-3 py-1 bg-white text-[#3A5A78] text-sm border border-gray-300 rounded
        - span: Certified (copy)

### Data Entry
- **Input Field**:
  - input: px-4 py-3 bg-[#F8F9FA] text-[#1A1A1A] border border-gray-300 rounded-sm

- **Textarea**:
  - textarea: px-4 py-3 bg-[#F8F9FA] text-[#1A1A1A] border border-gray-300 rounded-sm

- **Select Dropdown**:
  - select: px-4 py-3 bg-[#F8F9FA] text-[#1A1A1A] border border-gray-300 rounded-sm

- **Checkbox and radio button**
  - default: bg-[#F8F9FA] border border-gray-300
  - checked: bg-[#3A5A78]; text-white

### Container
- **Navigation Menu - horizontal**
    - example 1(Header navigation):
        - Nav Container: flex items-center gap-12
        - Menu Item: flex items-center gap-2 text-base text-[#1A1A1A]
          - menu-text: Services
          - dropdown-icon (if applicable): w-4 h-4
    - example 2(Navigation with logo and CTA):
        - Nav Container: flex items-center justify-between w-full py-4 px-8 border-b border-gray-300
        - Left Section: flex items-center gap-12
          - Logo: flex items-center gap-3
            - icon: w-8 h-8
            - brand-text: text-xl font-semibold
          - Menu Items: flex items-center gap-8
        - Right Section: flex items-center gap-4
          - Contact: text-sm text-[#4A4A4A]
          - CTA Button: px-6 py-2 bg-[#3A5A78] text-white/95 rounded-sm

- **Card**
    - example 1(Service card with border):
        - Card: bg-white border border-gray-300 flex flex-col p-6 gap-4
        - Icon area: flex items-center justify-center w-12 h-12
          - icon: w-8 h-8 text-[#3A5A78]
        - Text area: flex flex-col gap-3
          - card-title: text-base font-semibold text-[#1A1A1A]
          - card-description: text-sm text-[#4A4A4A]
    - example 2(Testimonial card):
        - Card: bg-white border border-gray-300 flex flex-col p-8 gap-6
        - Quote: text-base text-[#1A1A1A]
        - Author area: flex items-center gap-4 pt-4 border-t border-gray-300
          - avatar: w-12 h-12 rounded-full border border-gray-300
          - info: flex flex-col gap-1
            - name: text-sm font-semibold text-[#1A1A1A]
            - title: text-xs text-[#6A6A6A]
    - example 3(Image feature card):
        - Card: bg-white border border-gray-300 flex gap-6 p-6
        - Image: w-48 h-32 object-cover
        - Text area: flex flex-col gap-3 flex-1
          - card-title: text-base font-semibold text-[#1A1A1A]
          - card-description: text-sm text-[#4A4A4A]
          - card-link: text-sm text-[#3A5A78]

## Additional Notes
This style guide establishes Classic 8 Cleaning's 30-year legacy through editorial design principles. The steel blue primary color conveys institutional trust, while fine-line borders create structured, magazine-like layouts. Deep forest green provides strategic accent without overwhelming the authoritative presentation. The flat, shadow-free approach with minimal border radius ensures timeless sophistication suitable for a professional cleaning service with established credibility.

<colors_extraction>
#3A5A78
#5A7A98
#2A4A68
#FFFFFF
#F8F9FA
#E9ECEF
#1A1A1A
#4A4A4A
#6A6A6A
#9A9A9A
#FFFFFFF2
#FFFFFFBF
#2D5F3F
#E8F3EC
#8B3A3A
#F8E8E8
#8B7539
#F8F3E8
#D1D5DB
#9CA3AF
</colors_extraction>
