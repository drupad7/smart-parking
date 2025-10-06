# Smart Parking SJF Game - Design Guidelines

## Design Approach

**Selected Approach:** Hybrid - Modern Design System with Playful Hand-Drawn Aesthetics

The game combines educational clarity with engaging visual design. Using a clean foundation inspired by Linear and Notion for readability, enhanced with playful, hand-drawn illustrations to make OS concepts approachable and fun.

**Key Design Principles:**
- Visual clarity for algorithm demonstration
- Playful aesthetics to engage learners
- Real-time feedback through animation
- Educational value through visual storytelling

## Core Design Elements

### A. Color Palette

**Dark Mode (Primary):**
- Background: 222 15% 12% (deep charcoal)
- Surface: 222 12% 18% (elevated panels)
- Primary: 142 76% 45% (vibrant green - available slots)
- Accent: 271 76% 65% (purple - active/selected)
- Warning: 48 96% 55% (amber - queue/waiting)
- Error: 0 72% 55% (red - occupied)
- Text Primary: 0 0% 95%
- Text Secondary: 0 0% 65%

**Light Mode:**
- Background: 0 0% 98%
- Surface: 0 0% 100%
- Primary: 142 76% 38%
- Accent: 271 76% 55%
- Same warning/error values with adjusted contrast

### B. Typography

**Font Stack:**
- Primary: 'DM Sans' (Google Fonts) - clean, modern, excellent readability
- Monospace: 'JetBrains Mono' - for metrics, distances, algorithm values
- Accent: 'Caveat' - hand-drawn feel for playful elements

**Type Scale:**
- Hero/Title: text-4xl to text-5xl, font-bold
- Section Headers: text-2xl to text-3xl, font-semibold
- Body: text-base, font-normal
- Metrics/Data: text-sm to text-base, font-mono
- Labels: text-xs to text-sm, font-medium

### C. Layout System

**Spacing Units:** Primarily use 4, 6, 8, 12, 16 (tailwind units)
- Component padding: p-4 to p-8
- Section spacing: space-y-6 to space-y-8
- Grid gaps: gap-4 to gap-6
- Margins: m-4, m-6, m-8

**Grid Structure:**
- Main layout: Two-column on desktop (parking lot + controls/stats sidebar)
- Parking lot: Dynamic grid based on slot count (grid-cols-6 to grid-cols-10)
- Mobile: Stack vertically with parking lot taking priority viewport

### D. Component Library

**Parking Lot Grid:**
- Individual slot: rounded-xl border-2 with subtle shadow
- Size: min 60x80px, max 80x100px per slot
- Available: green border with dashed outline (hand-drawn feel)
- Occupied: red fill with car illustration
- States: subtle scale animation on hover, pulse when assigned

**Car Queue Display:**
- Horizontal scrolling queue at top or side
- Each car: rounded-lg card with car icon and wait time
- Queue position indicator with connecting lines
- Amber/yellow theme for waiting state

**Statistics Dashboard:**
- Card-based layout with rounded-2xl containers
- Metrics: Large numbers (text-3xl) with labels below
- Real-time graphs: Simple line/bar charts for efficiency
- Color-coded: green for good metrics, amber for moderate, red for poor

**Control Panel:**
- Prominent "Add Car" button: Large, rounded-full, primary color
- Speed controls: Slider with visual feedback
- Algorithm info: Collapsible panel explaining SJF logic
- Reset button: Subtle, outlined style

**Distance Visualization:**
- Connecting lines from car to slot with distance value
- Animated path showing SJF calculation
- Highlight closest slot with pulsing ring effect

### E. Visual Style & Illustrations

**Hand-Drawn Elements:**
- Car illustrations: Simple, friendly car icons with slight wobble/organic edges
- Parking slot borders: Slightly irregular, hand-drawn appearance using SVG paths
- Arrows/connectors: Sketchy style for showing movement paths
- Icons: Use Heroicons base with custom hand-drawn overlays for key elements

**Animation Strategy (Minimal but Impactful):**
- Car entrance: Smooth slide-in from queue (0.5s ease)
- Slot assignment: Gentle pulse + scale (0.3s)
- Distance calculation: Animated line drawing (0.4s)
- Stats update: Number count-up animation (0.3s)
- NO: Excessive hover effects, continuous animations, parallax

### F. Game Flow Visual Hierarchy

**Priority Layers:**
1. Parking Lot Grid (center focus, largest viewport area)
2. Queue Display (top or left, secondary focus)
3. Statistics Panel (right sidebar or bottom, tertiary)
4. Controls (fixed bottom or top-right, always accessible)

**Mobile Adaptation:**
- Parking lot: Full width, scrollable if needed
- Queue: Horizontal strip above lot
- Stats: Collapsible panel below
- Controls: Fixed bottom sheet

## Images

**No Hero Images Required** - This is a utility/game interface

**Illustration Needs:**
- Car Icons: 3-4 variations of simple, friendly car illustrations (top-down view)
- Parking Slot Graphics: Hand-drawn parking space markers with subtle texture
- Empty State: Playful illustration when no cars in queue
- Success State: Celebratory car icon when optimal parking achieved

**Placement:**
- Cars: Within queue cards and parking slots
- Background: Subtle grid pattern on parking lot surface (asphalt texture)
- Empty states: Center of respective sections

## Key Interactions

**SJF Algorithm Visualization:**
- On car arrival: Highlight all available slots
- Show distance calculation: Draw lines to each slot with distance values
- Animate selection: Closest slot pulses, others fade
- Car movement: Smooth path animation to selected slot
- Duration: 1-2 second sequence for educational value

**Feedback Patterns:**
- Success: Green checkmark + subtle confetti on optimal assignment
- Queue building: Amber glow on queue when cars waiting
- Full lot: Red overlay with "Lot Full" message
- Efficiency score: Real-time color change based on performance

**Responsive Behavior:**
- Desktop: Side-by-side layout with generous spacing
- Tablet: Modified two-column with adjusted proportions
- Mobile: Vertical stack with parking lot prioritized, controls in bottom sheet

This design creates an engaging, educational experience that makes OS scheduling concepts visually clear while maintaining a playful, approachable aesthetic through hand-drawn elements and thoughtful animations.