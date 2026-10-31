# StudyLoop – Responsive Product Landing Page (UI/UX using Figma, IPS)

**Enrollment No:** 202403103510025
**Name:** Batt Saral Manojbhai

## 1. Product and target users
**StudyLoop** is a fictional study-group platform for college students. It matches students with classmates who share the same subject and exam date, then gives the group a shared plan, notes, and daily check-ins.

**Target users:** college students (18–23) who find self-study hard to stay consistent with, mostly on phones, often studying at night before exams.
**Main job of the page:** get a student to click "Find my study group" within the first screen.

## 2. Design choices
- **Hero shows the product, not a stock photo.** The dark "study board" illustration shows a real group schedule, so users understand the product in seconds.
- **Colors:** deep ink blue for trust and focus, marigold for the single action colour (every primary button), teal for "live / active" status. Light cool-grey background keeps text easy to read.
- **Typography:** Bricolage Grotesque for headings (friendly, confident), DM Sans for body (clean on small screens). Only 6 text styles.
- **Spacing:** 8-point system (4, 8, 16, 24, 32, 48, 80) so every gap is predictable.
- **Responsive:** 3 cards become 1 column and the hero stacks on tablet/mobile.
- **Accessibility:** contrast above 4.5:1 for body text, visible keyboard focus, reduced-motion respected.

## 3. Colour styles (create in Figma → Local styles)
| Style name | Hex | Use |
|---|---|---|
| Ink/900 | #14213D | Text, dark panels, footer |
| Ink/700 | #2B3A5C | Secondary text, inner panels |
| Marigold/500 | #FCA311 | Primary buttons, highlights |
| Teal/500 | #2A9D8F | Status, logo accent |
| Mist/100 | #E8ECF4 | Borders |
| Paper/50 | #F6F8FC | Page background |
| White | #FFFFFF | Header, cards on light |

## 4. Text styles
| Style | Font | Weight | Size / Line |
|---|---|---|---|
| Display/H1 | Bricolage Grotesque | Bold | 56 / 60 |
| Display/H2 | Bricolage Grotesque | Bold | 36 / 42 |
| Heading/H3 | Bricolage Grotesque | SemiBold | 22 / 28 |
| Body/Large | DM Sans | Regular | 18 / 28 |
| Body/Regular | DM Sans | Regular | 16 / 24 |
| Button | DM Sans | Bold | 16 / 20 |

(Also in `design-tokens.json`.)

## 5. Reusable components (4)
1. **Button** – variants: `Primary` (marigold), `Secondary` (outline), size `Default/Small`. Auto Layout horizontal, padding 14/24, radius 10, gap 8.
2. **Header** – logo + 4 nav links + Button/Small. Auto Layout horizontal, space-between, height 72, fill width.
3. **Feature Card** – icon tile + H3 + body. Auto Layout vertical, padding 32, gap 16, radius 20, fixed width 384 on desktop.
4. **Schedule Slot** (hero board row) – time chip + title + avatars. Auto Layout horizontal, padding 16, gap 16, radius 14.

## 6. Figma build steps (follow in order)
1. Create frame **Desktop – 1440 × 1024**. Layout grid: 12 columns, margin 120, gutter 24 (content width 1200).
2. Create colour and text styles from sections 3 and 4.
3. Build the **Button** component, then add Primary/Secondary variants (Component set).
4. Build the **Header**: Auto Layout horizontal, place logo, links, and Button/Small. Make it a component.
5. **Hero**: Auto Layout horizontal, left column (H1, Body/Large, two buttons, small note), right column the study board (Ink/900 panel, radius 20, three Schedule Slot instances + progress bar).
6. **Features**: Auto Layout section with H2 and a horizontal row of 3 Feature Card instances (gap 24).
7. **CTA** section (H2, text, Primary button) and **Footer** (logo, two link columns, copyright), all Auto Layout.
8. Create a **Mobile – 390 × 844** frame: switch hero and cards to vertical direction, hide nav links (add a menu icon if you want).
9. Check spacing uses only 4/8/16/24/32/48/80, then publish styles/components.

> Figma link: 
https://www.figma.com/design/sQjtRQFmXIzkMnxZTgyd7G/StudyLoop-%E2%80%93-Landing-Page?node-id=0-1&t=PYsvrgeYcWKYYGRi-1
