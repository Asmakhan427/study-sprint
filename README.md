# Study Sprint

> A pixel-perfect, accessible, responsive focus-session timer built in React 18 + TypeScript

[![Live Demo](https://img.shields.io/badge/Live_Demo-View_App-2B6CB0?style=for-the-badge&logo=vercel&logoColor=white)](https://study-sprint-dklx.vercel.app)

## Overview

Study Sprint is a focus session tracker that lets students run timed work intervals using a split-flap departure-board timer. The application supports three session presets (Sprint 25m, Deep Work 50m, Short Break 5m), tracks daily focus statistics, and maintains a running log of today's sessions. The design system includes a full light/dark theme toggle driven entirely by CSS custom properties.

---

## Screenshots

<img width="1596" height="775" alt="image" src="https://github.com/user-attachments/assets/03b526fc-7159-4c14-a9aa-c687092a9260" />
<img width="1574" height="797" alt="image" src="https://github.com/user-attachments/assets/056993de-e688-40f0-8a6e-162a96db2b1c" />

---

## Features

### Timer Functionality
- Split-flap departure-board timer with MM:SS countdown
- Three session presets: Sprint (25m), Deep Work (50m), Short Break (5m)
- Start, Pause, Resume, and Reset controls
- Animated progress bar showing session completion percentage
- Session status announcements via ARIA live regions

### Theme and Design
- Light and Dark theme support with CSS custom properties
- Theme preference persisted to localStorage
- Respects system prefers-color-scheme on first load
- Pixel-perfect recreation of Figma mock reference
- 8px spacing system throughout the application

### Session Management
- Automatic session logging with timestamps
- Status tracking: Completed, Skipped, or Failed
- Statistics dashboard showing daily total, streak, and session count
- Simulated save flow with loading state and retryable error handling
- Error banner with role="alert" for accessibility

### Interactive States
- Hover, focus-visible, active, and disabled states for all interactive elements
- Loading states with animated spinners
- Error states with recovery actions
- Smooth transitions and micro-interactions

### Accessibility
- 100/100 Lighthouse Accessibility score
- Semantic HTML with proper landmark regions
- ARIA labels on all interactive elements
- aria-pressed for toggle controls
- aria-live timer announcements
- Skip to main content link
- Visible focus indicators with WCAG AA contrast
- prefers-reduced-motion support

### Responsive Design
- Mobile-first approach with real layout reflow
- Tested at 375px (mobile), 768px (tablet), and 1440px (desktop)
- Clamp-based typography for fluid scaling
- Flex-wrap for buttons and chips on narrow viewports
- Progress bar hidden on mobile per mock specification

---

## Technology Stack

| Technology | Purpose |
|------------|---------|
| React 18 | Frontend framework |
| TypeScript | Type safety and developer experience |
| Vite | Build tool and development server |
| Tailwind CSS | Layout and spacing utilities |
| Framer Motion | Animations and micro-interactions |
| CSS Custom Properties | Design tokens and theming |

---

## Installation

### Prerequisites
- Node.js (version 18 or higher)
- npm or yarn

### Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/study-sprint.git

# Navigate to project directory
cd study-sprint

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linting
npm run lint

---
## Project Structure
src/
├── components/
│   ├── Button.tsx           # Reusable button with variants and states
│   ├── TimerBoard.tsx       # Split-flap digit display
│   ├── FlapDigit.tsx        # Single animated split-flap tile
│   ├── ThemeToggle.tsx      # Light/dark mode switch
│   ├── ProgressBar.tsx      # Session completion progress
│   ├── StatsCard.tsx        # Statistics display tile
│   ├── LogEntry.tsx         # Session log entry with animation
│   ├── StatusBadge.tsx      # Status indicator pill
│   ├── DurationSelector.tsx # Session duration presets
│   └── ErrorBanner.tsx      # Retryable save error alert
├── hooks/
│   ├── useTimer.ts          # Timer state machine logic
│   ├── useSessionLog.ts     # Log management and statistics
│   └── useTheme.ts          # Theme state and persistence
├── utils/
│   ├── time.ts              # Time formatting utilities
│   └── constants.ts         # Application constants
├── types/
│   └── index.ts             # TypeScript type definitions
├── styles/
│   └── tokens.css           # Light/dark design tokens
├── App.tsx                  # Main application component
├── main.tsx                 # Application entry point
└── index.css               # Global styles and Tailwind directives

### Acknowledgments
Built as part of the Web Dev Track stretch task

Design inspired by departure board timers

React, TypeScript, and Vite communities
