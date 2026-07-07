# Software Requirements Specification: **AetherFlow**

Welcome, Developer! I am your customer. I need a premium, aesthetic, and fully functional **Personal Productivity & Flow Dashboard** named **AetherFlow**. 

You have **2 hours** to build this application. Once you are done, let me know, and I will test it and grade your work based on implementation completeness, visual design/aesthetics, code organization, and overall user experience.

---

## 1. Tech Stack & Project Structure

To ensure a modern, clean, and scalable codebase, you must use the following setup:

- **Frontend Framework**: **React + TypeScript** (scaffolded via Vite)
- **Styling**: Vanilla CSS (using CSS Variables/Custom Properties for theme management). Avoid TailwindCSS unless you absolutely prefer it, but a custom CSS system showing beautiful styling is highly encouraged.
- **State Management**: React state or React Context (e.g., `FlowContext`).
- **Data Persistence**: `localStorage` (all tasks, session analytics, and current theme configuration must persist).
---

## 2. Core Features & User Stories

### Feature A: Pomodoro Focus Timer
- **User Story 1**: As a user, I want to start, pause, and reset a focus timer (default: 25 mins focus, 5 mins short break, 15 mins long break).
- **User Story 2**: As a user, I want to see a beautiful visual countdown (preferably a circular SVG progress ring) showing the remaining time.
- **User Story 3**: As a user, I want a glowing visual indicator that pulses when the timer is active, reminding me to stay in the zone.
- **User Story 4**: As a user, when the timer ends, a gentle notification sound should play, and the session should be automatically recorded in the Analytics.

### Feature B: Ambient Soundscape Generator
- **User Story 1**: As a user, I want to play background soundscapes (Rain, Forest, Ocean Waves) directly from the dashboard.
- **User Story 2**: As a user, I want to toggle sounds on/off and adjust their volume independently using sleek slider controls.
- **Implementation Note**: This app is 100% client-side. No backend API is needed. For the audio tracks, you must use these direct public audio URLs:
  - **Rain**: `https://assets.mixkit.co/active_storage/sfx/2433/2433-84.wav`
  - **Forest/Birds**: `https://assets.mixkit.co/active_storage/sfx/1252/1252-84.wav`
  - **Ocean/Waves**: `https://assets.mixkit.co/active_storage/sfx/1188/1188-84.wav`
  *(Alternatively, you can synthesize white noise via the Web Audio API).*

### Feature C: Eisenhower Task Matrix
- **User Story 1**: As a user, I want to manage tasks in a 2x2 grid representing:
  1. *Urgent & Important* (Do First)
  2. *Important & Not Urgent* (Schedule)
  3. *Urgent & Not Important* (Delegate)
  4. *Not Urgent & Not Important* (Eliminate)
- **User Story 2**: As a user, I want to quickly add, delete, and toggle completion for tasks in any quadrant.
- **User Story 3**: As a user, I want to be able to move a task from one quadrant to another (via buttons or drag-and-drop).

### Feature D: Flow Analytics Dashboard
- **User Story 1**: As a user, I want to see my daily productivity metrics:
  - Total Focus Time (in minutes)
  - Tasks Completed
  - **Productivity Score**: A calculated metric: `(Completed Tasks * 15) + (Completed Focus Sessions * 25)`
- **User Story 2**: As a user, I want to see a visual chart (e.g., an SVG bar chart or line graph) showing focus sessions completed over the last few days.

---

## 3. Design & Aesthetic Guidelines (CRITICAL)

The design must feel **ultra-premium, modern, and alive**. 
- **Glassmorphism**: Use translucent panels with `backdrop-filter: blur(16px) saturate(180%)`, a thin semi-transparent border, and subtle drop shadows.
- **Typography**: Import a modern font (e.g., `Outfit` or `Inter` from Google Fonts).
- **Interactive States**: Hovering over buttons/cards should trigger smooth transitions (`transition: all 0.3s ease`), slight scale-ups, and glow effects.
- **Themes**: Create a theme selector that switches the CSS variables. You must support at least 3 themes:
  1. **Midnight Obsidian** (Default): Deep obsidian background, rich purple accents, neon violet glows.
  2. **Cyberpunk Grid**: Pitch black background, electric cyan and magenta highlights.
  3. **Sage Sanctuary**: Dark slate green background, warm sage details, amber highlights.

---

## 4. Evaluation Criteria for Grading
When the 2 hours are up, I will run your project and evaluate it on:
1. **Feature Completeness (40%)**: All core features (Timer, Ambient sounds, Eisenhower Matrix, Analytics, Themes) must be working.
2. **Visual Design & Aesthetics (30%)**: Premium feel, responsiveness, interactive feedback, high-quality CSS/animations.
3. **Architecture & Code Quality (20%)**: Clean TypeScript, clean division of components, and context organization.
4. **Data Persistence & Robustness (10%)**: Storing states in `localStorage`, handling browser reloads gracefully, no app crashes.

Good luck! Let me know if you accept the challenge or if you have any questions before you begin the timer.
