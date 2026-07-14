# Study Sprint

<p align="center">
  <a href="https://study-sprint-dklx.vercel.app" target="_blank">
    <img src="https://img.shields.io/badge/Live_Demo-View_App-2B6CB0?style=for-the-badge&logo=vercel&logoColor=white" alt="Live Demo">
  </a>
</p>

## Overview

Study Sprint is a focus session tracker that lets students run timed work intervals using a split-flap departure-board timer. The application supports three session presets (Sprint 25m, Deep Work 50m, Short Break 5m), tracks daily focus statistics, and maintains a running log of today's sessions. The design system includes a full light/dark theme toggle driven entirely by CSS custom properties.

---

## Output

<img width="1596" height="775" alt="image" src="https://github.com/user-attachments/assets/03b526fc-7159-4c14-a9aa-c687092a9260" />
<img width="1574" height="797" alt="image" src="https://github.com/user-attachments/assets/056993de-e688-40f0-8a6e-162a96db2b1c" />

---

## Features

### Timer Functionality
- Split-flap departure-board timer with MM:SS countdown
- Three session presets: Sprint (25m), Deep Work (50m), Short Break (5m)
- Start, Pause, Resume, and Reset controls

### Theme and Design
- Light and Dark theme support with CSS custom properties
- Theme preference persisted to localStorage
- Respects system prefers-color-scheme on first load

### Session Management
- Automatic session logging with timestamps
- Status tracking: Completed, Skipped, or Failed
- Statistics dashboard showing daily total, streak, and session count

### Interactive States
- Hover, focus-visible, active, and disabled states for all interactive elements
- Loading states with animated spinners


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
```

## Output
CSS Variables for Theming: All colors use CSS custom properties for consistent theming and easy theme switching

Mobile-First Approach: Built for mobile first with progressive enhancement for larger screens

Split-Flap Timer: Custom animated departure-board style timer for visual impact

Component Reusability: Every card, badge, and button is a single reusable component

TypeScript Strict Mode: No use of any type, full type safety throughout
