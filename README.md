# SNEKS 🐍

**S**imulated • **N**on-deterministic • **E**ntities • **K**inetically • **S**warming

A mesmerizing procedural snake ecosystem simulation where autonomous serpentine entities navigate a grid-based world with stochastic movement patterns, creating emergent behaviors and complex interactions.


## Live Demo

[Try SNEKS Live](#)

## Features

### Core Mechanics
- **Grid-based world** that automatically adjusts to screen size
- **Stochastic movement** - each snake has unique probability distributions for movement
- **Real-time visualization** with customizable frame rate
- **Population dynamics tracking** with live charts showing the last 2000 frames
- **Smart spawning system** that finds optimal placement for new entities

### Snake Behavior
- Autonomous movement with probabilistic direction changes
- Unique pastel colors for each snake
- Configurable movement patterns via Wiggle and Random parameters
- Edge wrapping for continuous world navigation
- Optional self-collision detection

### Interactive Elements
- Three types of fruit with different effects:
  - 🟡 Yellow (+1): Increases snake length
  - 🟢 Green (+2): Increases snake length by 2
  - 🔵 Blue (-1): Decreases snake length
- Complex collision mechanics:
  - Head-on collisions eliminate both snakes
  - Head-to-body collisions transfer energy between snakes

### Visual Analytics
- Real-time population charts
- Current and maximum statistics tracking
- Performance monitoring with FPS warnings
- Clean, minimalist aesthetic inspired by modern design

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No additional dependencies required!

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/sneks.git
cd sneks
```

2. Open in browser:
   - Simply open `index.html` in your web browser
   - Or use a local server for better performance:
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx http-server

# Then navigate to http://localhost:8000
```

## 🎛️ Configuration

### Parameters

| Parameter | Description | Default | Range |
|-----------|-------------|---------|-------|
| **Frame Rate** | Time between frames (ms) | 500 | 100-2000 |
| **Snake Gen Rate** | Frames between snake spawns | 30 | 10-100 |
| **Initial Length** | Starting snake length | 5 | 3-10 |
| **Fruit Rate** | Frames between fruit spawns | 20 | 5-50 |
| **Grid Size** | Cell size in pixels | 20 | 10-40 |
| **Wiggle** | Base turning tendency | 0.4 | 0.0-1.0 |
| **Random** | Individual variation | 0.4 | 0.0-1.0 |
| **Self Collision** | Allow snakes to hit themselves | Yes | Yes/No |

### Movement Probabilities

The **Wiggle** parameter controls base movement:
- `0.0` = Straight movement (80% forward, 10% left/right)
- `0.5` = Balanced (55% forward, 22.5% left/right)
- `1.0` = Maximum chaos (40% forward, 30% left/right)

The **Random** parameter adds individual variation:
- `0.0` = All snakes identical
- `0.5` = ±12.5% variation
- `1.0` = ±25% variation (maximum diversity)


## Gameplay Tips

1. **Low Wiggle + Low Random** = Orderly, highway-like snake movement
2. **High Wiggle + Low Random** = Chaotic but uniform swarm behavior
3. **Low Wiggle + High Random** = Diverse personalities, mostly straight paths
4. **High Wiggle + High Random** = Maximum chaos and emergent patterns

## Technical Details

### Performance Optimization
- Efficient collision detection using Set-based lookups
- Optimized placement algorithm for O(n) complexity
- Canvas-based rendering for smooth animation
- Performance monitoring with automatic FPS warnings

### Browser Compatibility
- ES6+ JavaScript
- HTML5 Canvas
- CSS Grid and Flexbox
- No external dependencies

## Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

### Development Ideas
- [ ] Add sound effects for collisions and fruit consumption
- [ ] Implement different snake AI personalities
- [ ] Add multiplayer/competitive modes
- [ ] Create themed visual styles
- [ ] Export simulation statistics
- [ ] Add replay functionality
- [ ] Implement save/load states

## Analytics

The simulation tracks various metrics:
- **Population dynamics** over time
- **Maximum values** achieved during runtime
- **Individual snake sizes** and growth patterns
- **Collision frequency** and outcomes
- **Resource consumption** patterns

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

