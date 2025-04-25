# Interactive Dragon Project

An interactive web-based animation featuring a responsive dragon that follows cursor movements with fluid, organic animations.

## Project Overview

The Interactive Dragon is a web application that creates an engaging user experience through a dynamically animated dragon that responds to user cursor movements. The dragon is constructed using SVG elements that form a chain-like structure, resulting in smooth and natural movement patterns.

## Technical Specifications

### Technologies Used
- HTML5
- CSS3
- JavaScript (ES6+)
- SVG (Scalable Vector Graphics)

### File Structure
```
interactive_dragon/
├── cursor-dragon.html
├── cursor-dragon.css
├── cursor-dragon.js
└── README.md
```

## Components Description

### 1. HTML Structure (`cursor-dragon.html`)
- Contains the basic HTML5 structure
- Includes SVG definitions for dragon components:
  - `Cabeza` (Head): Defines the dragon's head using SVG paths
  - `Aletas` (Fins): Complex gradient-filled fins
  - `Espina` (Spine): Gradient-filled spine segments
- Uses SVG `defs` for reusable components
- Implements a screen container for the animation

### 2. Styling (`cursor-dragon.css`)
- Sets up a fullscreen canvas
- Key styling features:
  - Removes default margins and padding
  - Forces fullscreen display
  - Prevents scrolling
  - Sets background colors:
    - Body: RGB(60, 97, 153)
    - SVG canvas: #c9c9c9
  - Applies a sepia filter (20%) for visual effect
  - Implements touch-action prevention for better mobile experience

### 3. Animation Logic (`cursor-dragon.js`)
- Core Features:
  1. Pointer Tracking
     - Tracks user's cursor position
     - Updates dragon movement accordingly
  
  2. Dragon Assembly
     - Creates 40 segments (N = 40)
     - Combines different elements:
       - Head (Cabeza)
       - Fins (Aletas) at segments 8 and 14
       - Spine (Espina) for remaining segments
  
  3. Animation System
     - Uses RequestAnimationFrame for smooth animation
     - Implements physics-based movement:
       - Segment following behavior
       - Smooth transitions
       - Distance-based scaling
     - Automatic centering when inactive

## Key Functions

### 1. `resize()`
- Handles window resizing
- Updates width and height variables

### 2. `prepend(use, i)`
- Creates new SVG elements
- Manages element references
- Adds elements to the screen

### 3. `run()`
- Main animation loop
- Calculates positions and rotations
- Updates element transformations
- Handles automatic centering behavior

## Interactive Features

### 1. Cursor Following
- Dragon follows cursor movement
- Smooth transition between positions
- Organic movement patterns

### 2. Automatic Behavior
- Returns to center when inactive
- Maintains fluid motion
- Scales segments based on position

### 3. Responsive Design
- Adapts to window size
- Maintains proportions
- Fullscreen experience

## Visual Effects

### 1. Dragon Components
- Detailed head design
- Gradient-filled fins
- Spine segments with gradient effects

### 2. Styling
- Sepia filter for visual warmth
- Custom background colors
- Smooth transitions

## Technical Implementation Details

### Animation Parameters
- 40 connected segments
- Position updates every frame
- Smooth easing using division factors
- Rotation calculation using arctangent
- Scale adjustments based on segment position

### Performance Considerations
- Uses RequestAnimationFrame for optimal performance
- Efficient SVG manipulation
- Minimal DOM updates
- Smooth pointer tracking

## Browser Compatibility
- Supports modern browsers with SVG capabilities
- Requires JavaScript enabled
- Uses standard web APIs

## Usage
1. Open `cursor-dragon.html` in a modern web browser
2. Move your cursor/pointer around the screen
3. The dragon will follow your movements
4. When inactive, the dragon returns to the center

## Development Notes
- SVG definitions are reused for efficiency
- Modular component structure
- Clean separation of concerns (HTML, CSS, JS)
- Efficient animation calculations

## Getting Started

1. Clone the repository:
```bash
git clone [repository-url]
```

2. Navigate to the project directory:
```bash
cd interactive_dragon
```

3. Open `cursor-dragon.html` in your preferred web browser.

## Contributing

Feel free to submit issues and enhancement requests! 