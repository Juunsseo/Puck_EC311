
# EC311 Puck Project

## Overview
The EC311 Puck Project is a hardware-based implementation of a Pong-inspired game, designed to run on an FPGA platform using Verilog. The project demonstrates digital design principles, including VGA display control, debouncing, and game logic.

## Features
- **Interactive Gameplay:** Paddle and ball mechanics inspired by Pong.
- **VGA Display:** Real-time graphics output with a resolution of 640x480.
- **Scoring System:** A real-time score tracker for player progress.
- **Dynamic Ball Movement:** Ball speed increases upon paddle collision, enhancing difficulty.
- **Debouncing Logic:** Smooth handling of user input to avoid erratic paddle movements.

## File Structure

- **`pixel.v`**: Implements the rendering logic for the paddle, ball, walls, and background. Handles collisions and scoring mechanics.
- **`pong.v`**: The main module integrating all submodules and coordinating the game logic.
- **`vga_controller.v`**: Handles the VGA signal generation for display output.
- **`debouncer.v`**: Processes button inputs to eliminate bouncing effects.
- **`Nexys4DDR_Master.xdc`**: Constraints file for the Nexys4DDR FPGA board.
- **`EC311 Final Project Presentation.pptx`**: A presentation summarizing the project.

## Getting Started

### Prerequisites
- **Hardware:** Nexys4DDR FPGA board or a similar platform.
- **Software:**
  - Xilinx Vivado Design Suite.
  - A monitor capable of 640x480 VGA input.

### Setup Steps
1. Clone the repository or extract the provided zip file.
2. Open the `Nexys4DDR_Master.xdc` constraints file in Vivado.
3. Add the Verilog source files (`pixel.v`, `pong.v`, `vga_controller.v`, `debouncer.v`) to the project.
4. Synthesize and implement the design in Vivado.
5. Generate the bitstream and program the FPGA.
6. Connect the FPGA to a VGA-compatible monitor and use the paddle controls to play the game.

### Controls
- **Up Button:** Move the paddle up.
- **Down Button:** Move the paddle down.

## How It Works
1. **VGA Controller:** Generates horizontal and vertical sync signals for display output.
2. **Pixel Module:**
   - Calculates paddle and ball positions.
   - Detects collisions and updates game state.
3. **Debouncer:** Ensures reliable button presses for paddle movement.
4. **Game Logic:** Managed in `pong.v`, integrating all components to create gameplay.

## Customization
- Modify `parameter` values in `pixel.v` to adjust game settings like paddle speed, ball size, or scoring rules.
- Adjust the VGA resolution by updating `vga_controller.v`.

## Authors
- Vikram Singh Bhalla, Michael Daniels, Junseo Lee, Prashast Pandey

## Demo Video
[![EC311 Final Demo Video- Puck](https://img.youtube.com/vi/TeToti020jk/0.jpg)](https://www.youtube.com/watch?v=TeToti020jk)
Click the image above.
---

For more details, refer to the included presentation file (`EC311 Final Project Presentation.pptx`).
