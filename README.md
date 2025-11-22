# Flappy Bird Game

A classic Flappy Bird game built with HTML5 Canvas, featuring realistic design, slow-paced gameplay, and a dynamic day-night cycle.

## Features

- **2D Canvas Rendering**: Pure HTML5 Canvas for smooth 2D graphics
- **Slow, Realistic Physics**: Gentle gravity and movement matching the original Flappy Bird feel
- **Dynamic Day-Night Cycle**: Watch the sky transition from day to night as you play
- **Parallax Background**: Animated clouds and scrolling ground elements
- **Score Tracking**: Keep track of your score and high score
- **Sound Effects**: Audio feedback for jumping, scoring, and collisions
- **Responsive Design**: Works on different screen sizes

## How to Play

- **Click** or press **Space/W/Arrow Up** to make the bird fly
- Avoid the pipes and the ground
- Try to score as many points as possible!

## Development

### Prerequisites

- Node.js 20 or higher
- npm

### Installation

```bash
npm install
```

### Running Locally

```bash
npm run dev
```

The game will be available at `http://localhost:5000`

### Building for Production

```bash
npm run build
```

The build output will be in the `dist/public` directory.

## Deployment to GitHub Pages

This project is configured for automatic deployment to GitHub Pages using GitHub Actions.

### Setup Instructions

1. **Push your code to a GitHub repository**

2. **Enable GitHub Pages in your repository:**
   - Go to your repository on GitHub
   - Navigate to Settings → Pages
   - Under "Build and deployment", select **"GitHub Actions"** as the source
   - Click Save

3. **Enable workflow permissions:**
   - Go to Settings → Actions → General
   - Scroll to "Workflow permissions"
   - Select **"Read and write permissions"**
   - Check **"Allow GitHub Actions to create and approve pull requests"**
   - Click Save

4. **Deploy:**
   - Push to the `main` branch, or
   - Go to the "Actions" tab and manually trigger the "Deploy to GitHub Pages" workflow

5. **Access your game:**
   - Once the workflow completes, your game will be available at:
   - `https://[your-username].github.io/[repository-name]/`

The GitHub Actions workflow (`.github/workflows/deploy.yml`) will automatically:
- Install dependencies
- Build the project
- Deploy to GitHub Pages

### Manual Deployment

If you prefer to deploy manually:

```bash
npm run build
```

Then upload the contents of `dist/public` to your hosting service.

## Project Structure

```
├── client/
│   ├── public/          # Static assets (sounds, textures)
│   └── src/
│       ├── components/  # React components
│       │   ├── FlappyBird.tsx    # Main game component
│       │   ├── GameUI.tsx        # UI overlay
│       │   └── SoundManager.tsx  # Audio management
│       └── lib/
│           └── stores/  # State management
│               └── useFlappyBird.tsx
├── .github/
│   └── workflows/
│       └── deploy.yml   # GitHub Actions deployment workflow
└── package.json
```

## Technologies Used

- React
- TypeScript
- HTML5 Canvas
- Zustand (state management)
- Vite (build tool)

## License

MIT
