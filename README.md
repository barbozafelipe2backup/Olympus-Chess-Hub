# Olympus Chess Hub v14 — State Reconciliation Runtime

A high-performance 3D chess engine built with **Three.js** featuring state reconciliation, entity management, and game replay capabilities.

## Features

✨ **State Reconciliation Engine** — Maintains perfect synchronization between board state and 3D visualization
🎮 **Live & Replay Modes** — Play in real-time or scrub through game history
🔄 **Entity System** — Smooth animations with position interpolation
🎨 **3D Board Rendering** — Interactive chess board with raycasting input
📊 **Game History** — Complete move history with tick tracking
⚙️ **Deterministic Chess Logic** — Turn-based move validation and event emission

## How to Play

1. Open `index.html` in a modern web browser
2. **LIVE Mode**: Click a piece to select, then click a target square to move
3. **REPLAY Mode**: Use the scrub slider to navigate through past moves
4. **RESET**: Clear the board and start a new game

## Architecture

### Core Components

- **Chess Class**: Manages board state and move legality
- **DiffEngine**: Emits normalized move events for animation
- **Entity System**: Tracks 3D piece objects with smooth motion interpolation
- **Engine**: Handles state history and replay functionality
- **Director**: Controls camera and cinematic effects

### Key Systems

**State Reconciliation**
- Board state is the single source of truth
- World entities are reconciled against board state
- Supports seamless state transitions in replay mode

**Input Handling**
- Raycaster-based tile selection for precise clicks
- Turn validation prevents invalid moves
- Click-based selection: select → click target → execute move

**Animation**
- Position interpolation at 20% per frame (smooth 60fps motion)
- Automatic capture piece removal
- Entity reuse for efficiency

## Technologies

- **Three.js** (r160) — 3D rendering
- **WebGL** — GPU-accelerated graphics
- **OrbitControls** — Interactive camera navigation
- **Vanilla JavaScript** — No build tool required

## Known Features & Considerations

✅ Complete standard chess move logic (with simplified legality checking)
✅ 64-tile 3D board with alternating colors
✅ Smooth piece animations with easing
✅ Full game replay with scrubber control
✅ Material-based piece differentiation (white/black)

## Browser Support

Works on modern browsers with WebGL support:
- Chrome/Edge 60+
- Firefox 55+
- Safari 12+

## Live Demo

Open this file directly in your browser or deploy to GitHub Pages.

---

**Version**: 14.0  
**State**: Production-Ready  
**Last Updated**: 2025