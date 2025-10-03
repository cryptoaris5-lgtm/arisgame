# Math Adventure Game

## Overview

Math Adventure Game is an interactive, browser-based educational game designed to teach basic addition to children ages 6 to 8. The game features a character-catching mechanic where children control a baby puppy or baby kitten to catch falling numbers that represent correct answers to addition problems. The application is built as a single-page application (SPA) using vanilla HTML, CSS, and JavaScript, requiring no backend infrastructure or external dependencies.

## User Preferences

Preferred communication style: Simple, everyday language.

## Game Features

### Core Gameplay
- **Start Screen**: Children enter their username and age before beginning
- **Character Selection**: Choice between baby puppy 🐶 and baby kitten 🐱
- **10 Progressive Levels**: Addition problems starting simple (1+1) and gradually increasing in difficulty (up to 7+8)
- **Falling Items Mechanic**: Correct answers, wrong numbers, and candies 🍬 fall from the top of the screen
- **Character Control**: Move character left/right using arrow keys, mouse drag, or touch to catch the correct answer
- **Level Restart**: If the correct answer is missed, the level automatically restarts with encouraging feedback
- **Results Screen**: Displays player name, levels completed, total time, and score

### Educational Design
- Appropriate difficulty progression for ages 6-8
- Positive reinforcement with encouraging feedback messages
- Visual rewards and celebratory messages for correct answers
- Automatic level restart on missed answers to ensure completion

## System Architecture

### Frontend Architecture
- **Single-Page Application (SPA)**: The game uses a screen-based navigation system where different game states (start, character selection, gameplay, results) are managed by toggling CSS classes on DOM elements
- **Vanilla JavaScript**: No frontend frameworks or libraries are used; all interactivity is implemented with native JavaScript DOM manipulation
- **CSS Animations**: Smooth falling animations using CSS keyframes and requestAnimationFrame for collision detection
- **Responsive Design**: The layout uses flexbox and viewport-based sizing to ensure the game works across different screen sizes

### Game State Management
- **Screen Management**: Different game screens are controlled by adding/removing an 'active' class
- **DOM-based State**: Game state (username, age, character, current level, score, time) is managed through JavaScript objects
- **Collision Detection**: Uses requestAnimationFrame for efficient real-time collision detection between falling items and character

### Game Logic
- **Level Progression**: 10 predefined addition problems with increasing difficulty
- **Item Generation**: Random placement and timing for falling items (correct answer + 3 wrong answers + 3 candies per level)
- **Restart Mechanic**: When correct answer is missed, level automatically restarts after showing feedback
- **Score Tracking**: 10 points awarded per correct answer, with total time tracking

### Styling Approach
- **Custom CSS**: All styling is done through embedded CSS in the HTML file
- **Gradient Backgrounds**: Uses CSS linear gradients for visual appeal (purple gradient for menus, sky gradient for gameplay)
- **Comic Sans Typography**: Child-friendly font choice for educational context
- **Shadow Effects**: Box shadows and text shadows for depth and visual hierarchy
- **Colorful Feedback**: Visual feedback with different colors for correct (green), wrong (red), missed (orange), and candy (orange)

### Input Controls
- **Keyboard**: Left/Right arrow keys for character movement
- **Mouse**: Click and drag character to move
- **Touch**: Touch and drag support for mobile devices

## External Dependencies

### None Required for Core Functionality
- The application is entirely self-contained within a single HTML file (index.html)
- No external libraries, frameworks, or APIs are required
- No database or backend services needed
- No build tools or package managers required

### Deployment
- Simple HTTP server (Python 3.11 http.server module) serves the static HTML file on port 5000
- Single workflow configuration for serving the game

## Recent Changes

### October 3, 2025
- Initial implementation of Math Adventure Game with all core features
- Fixed critical bug where missing the correct answer would cause the game to soft-lock
- Implemented level restart mechanism with encouraging feedback when correct answer is missed
- Verified all 10 levels can be completed successfully
