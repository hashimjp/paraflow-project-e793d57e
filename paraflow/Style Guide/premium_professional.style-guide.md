# Premium Professional Style Guide

## Colors
### Primary Colors
  - **primary-base**: `text-[#2C3539]` or `bg-[#2C3539]` - Charcoal grey for headings, primary buttons
  - **primary-lighter**: `bg-[#4A5458]`
  - **primary-darker**: `text-[#1A2024]` or `bg-[#1A2024]`

### Background Colors
- **bg-page**: `bg-[#FAF8F6]` - Off-white with subtle warm tint
- **bg-container-primary**: `bg-white` - Main cards, elevated content containers
- **bg-container-secondary**: `bg-[#F5F3F0]` - Secondary sections, subtle differentiation
- **bg-container-elevated**: `bg-white` - Premium cards with shadow elevation

### Text Colors
- **color-text-primary**: `text-[#2C3539]` - Primary headings and important content
- **color-text-secondary**: `text-[#5A6367]` - Body text, descriptions
- **color-text-tertiary**: `text-[#8B9397]` - Supporting text, captions
- **color-text-on-dark-primary**: `text-white/95` - Text on dark backgrounds and primary color surfaces
- **color-text-on-dark-secondary**: `text-white/75` - Secondary text on dark backgrounds
- **color-text-link**: `text-[#2C3539]` - Links with underline for clarity

### Accent Colors
  - **accent-gold**: `text-[#C9A961]` or `bg-[#C9A961]` - Warm gold for key CTAs, highlights, and premium touches
  - **accent-gold-light**: `bg-[#E8DCC0]` - Subtle backgrounds for featured sections
  - **accent-gold-dark**: `text-[#A68B4D]` or `bg-[#A68B4D]` - Hover states for gold elements

### Functional Colors
  - **color-success-default**: #5C9A6F
  - **color-success-light**: #E8F5EC - Tag/label backgrounds
  - **color-error-default**: #C94D3F
  - **color-error-light**: #FCE8E6 - Tag/label backgrounds
  - **color-warning-default**: #E8B456
  - **color-warning-light**: #FDF4E3 - Tag/label backgrounds

## Typography
- **Font Stack**:
  - **font-family-base**: `-apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Helvetica Neue", Arial, sans-serif` — For all UI content with elegant proportions

- **Font Size & Weight**:
  - **Caption**: `text-xs font-normal`
  - **Body small**: `text-sm font-normal`
  - **Body default**: `text-base font-normal`
  - **Card Title / Emphasized Text**: `text-lg font-semibold`
  - **Page Title**: `text-2xl font-semibold`
  - **Headline**: `text-4xl font-semibold`
  - **Display**: `text-5xl font-semibold`

- **Line Height**: 1.4

## Border Radius
  - **Minimal**: 4px — Small interactive elements, tags
  - **Small**: 8px — Buttons, inputs
  - **Medium**: 12px — Cards, content containers
  - **Large**: 16px — Hero sections, prominent features

## Layout & Spacing
  - **Spacing Scale**:
  - **Base Unit**: 4px
  - **Tight**: 8px - For closely related elements
  - **Compact**: 16px - For list items and component internal spacing
  - **Standard**: 24px - For section spacing and card padding
  - **Spacious**: 32px - For major section breaks
  - **Generous**: 48px - For page-level spacing and hero sections

## Create Boundaries
Primarily relies on clean layered surfaces with subtle elevation. Minimal borders used only for inputs and functional clarity.

### Borders
  - **Default**: Rarely used. When needed for inputs or functional boundaries: 1px solid #E5E3DF `border border-[#E5E3DF]`
  - **Focused**: 1px solid #C9A961 (accent-gold) for active input states `border border-[#C9A961]`

### Dividers
  - **Subtle**: `border-t border-[#EFEEE9]` - Gentle separation within sections when surface color contrast isn't sufficient

### Shadows & Effects
  - **Elevated Card (Primary)**: `shadow-[0_2px_12px_rgba(44,53,57,0.08)]` - For main content cards and containers
  - **Elevated Card (Hover)**: `shadow-[0_4px_20px_rgba(44,53,57,0.12)]` - Interactive card hover state
  - **Subtle Depth**: `shadow-[0_1px_4px_rgba(44,53,57,0.06)]` - For buttons and small interactive elements

## Assets
### Image
- For normal `<img>`: object-cover
- For `<img>` with:
  - Slight overlay: object-cover brightness-90
  - Heavy overlay: object-cover brightness-75

### Logo
- To protect copyright, do **NOT** use real product logos as a logo for a new product, individual user, or other company products.
- **Icon-based**:
  - **Graphic**: Use a simple, relevant FontAwesome Solid icon (e.g., `fa-broom` for cleaning services, `fa-shield-check` for reliability).

### Icon
- Use Lucide icons from Iconify for their refined, professional appearance.
- To ensure aesthetic layout, each icon should be centered in a square container matching the icon's size. This container is only for layout optimization and does not imply the icon has a background; other properties should be determined based on actual needs.
- Use Tailwind font size to control icon size
- Example:
  ```html
  <div class="flex items-center justify-center bg-transparent w-5 h-5">
  <iconify-icon icon="lucide:sparkles" class="text-xl"></iconify-icon>
  </div>
  ```

## Basic Layout - Web

<!-- Critical Note: **MUST** follow the layout rules. -->
- Vertical Layout:
  - body (w-[1440px])
    - Header (Fixed height w-full) <!-- bg: bg-white with subtle shadow -->
    - Content Container(w-full flex):
      - Main Content Area (flex-1 overflow-x-hidden)
    - Footer - if present (Fixed height w-full) <!-- bg: bg-[#2C3539] -->

## Page Layout - Web

```html
<!-- standard implementation for body. A specific body width needs to be defined, which changes based on user requirements -->
<body class="w-[1440px] min-h-[900px] font-[-apple-system,BlinkMacSystemFont,'Segoe_UI','Roboto','Helvetica_Neue',Arial,sans-serif] leading-[1.4]">

</body>
```

## Tailwind Component Examples
<!-- Important Note: Use utility classes directly. Do NOT create custom CSS classes or add styles in <style> tags -->
### Basic
- **Button**:
  - example 1 (Primary CTA - Gold):
    - button: flex items-center justify-center gap-2 bg-[#C9A961] text-white/95 px-6 py-3 rounded-lg font-semibold shadow-[0_1px_4px_rgba(44,53,57,0.06)] hover:bg-[#A68B4D]
      - span: Get Started (button copy)
  - example 2 (Secondary - Charcoal):
    - button: flex items-center justify-center gap-2 bg-[#2C3539] text-white/95 px-6 py-3 rounded-lg font-semibold shadow-[0_1px_4px_rgba(44,53,57,0.06)] hover:bg-[#1A2024]
      - span: Learn More (button copy)
  - example 3 (Text button):
    - button: flex items-center gap-2 text-[#2C3539] font-semibold underline
      - span: View Details (button copy)
  - example 4 (Icon button):
    - button: flex items-center justify-center w-10 h-10 bg-white rounded-lg shadow-[0_1px_4px_rgba(44,53,57,0.06)]
      - icon: w-5 h-5

- **Label/Tag/Badge**:
    - div: flex items-center px-3 py-1.5 bg-[#E8DCC0] text-[#2C3539] rounded text-sm font-medium
      - span: Featured (copy)

### Data Entry
- **Input Field**:
  - container: flex flex-col gap-2
    - label: text-sm font-medium text-[#2C3539]
    - input: px-4 py-3 bg-white border border-[#E5E3DF] rounded-lg text-[#2C3539] placeholder:text-[#8B9397] focus:border-[#C9A961] focus:outline-none

- **Checkbox and Radio Button**:
  - default: bg-white border-2 border-[#E5E3DF]
  - checked: bg-[#C9A961] border-[#C9A961] text-white

### Container
- **Navigation Menu - horizontal**
    - Nav Container: flex items-center justify-between w-full px-12 py-6 bg-white shadow-[0_1px_4px_rgba(44,53,57,0.06)]
    - Left Section (Logo): flex items-center gap-3
      - logo-icon: w-10 h-10
      - brand-name: text-xl font-semibold text-[#2C3539]
    - Center Section (Menu): flex items-center gap-8
      - Menu Item: flex items-center gap-2 text-[#5A6367] font-medium hover:text-[#2C3539]
    - Right Section: flex items-center gap-4
      - CTA Button

- **Card**
    - example 1 (Elevated service card):
        - Card: bg-white rounded-xl flex flex-col p-6 gap-4 shadow-[0_2px_12px_rgba(44,53,57,0.08)] hover:shadow-[0_4px_20px_rgba(44,53,57,0.12)]
        - Icon Container: flex items-center justify-center w-12 h-12 bg-[#E8DCC0] rounded-lg
          - icon: w-6 h-6 text-[#C9A961]
        - Text area: flex flex-col gap-2
          - card-title: text-lg font-semibold text-[#2C3539]
          - card-description: text-sm text-[#5A6367]
    - example 2 (Testimonial card):
        - Card: bg-[#F5F3F0] rounded-xl flex flex-col p-6 gap-4
        - Quote: text-base text-[#5A6367] italic
        - Author area: flex items-center gap-3
          - avatar: w-10 h-10 rounded-full
          - author-info: flex flex-col
            - name: text-sm font-semibold text-[#2C3539]
            - role: text-xs text-[#8B9397]
    - example 3 (Image-focused project card):
        - Card: flex flex-col gap-4
        - Image: rounded-xl w-full object-cover
        - Text area: flex flex-col gap-2
          - card-title: text-lg font-semibold text-[#2C3539]
          - card-subtitle: text-sm text-[#5A6367]

## Additional Notes
This style guide establishes a refined professional aesthetic that communicates corporate sophistication and premium service quality. The charcoal grey and warm gold palette creates an approachable yet authoritative presence, while the subtle shadows and clean surfaces maintain visual clarity. The design balances modern minimalism with classic elegance, ensuring the brand feels established and trustworthy while remaining contemporary and accessible.

<colors_extraction>
#2C3539
#4A5458
#1A2024
#FAF8F6
#FFFFFF
#F5F3F0
#5A6367
#8B9397
#FFFFFF99
#C9A961
#E8DCC0
#A68B4D
#5C9A6F
#E8F5EC
#C94D3F
#FCE8E6
#E8B456
#FDF4E3
#E5E3DF
#EFEEE9
</colors_extraction>
