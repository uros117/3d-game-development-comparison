# Thesis Summary: Comparison of Tools for Developing 3D Video Games in JavaFX, Bevy and Unity 3D Technologies

**Author:** Uroš Filipović (2018/0663)  
**Mentor:** Dr. Igor Tartalja, Associate Professor  
**Institution:** University of Belgrade - Faculty of Electrical Engineering  
**Department:** Computer Engineering and Informatics  
**Year:** 2022

## Abstract

This thesis compares three technologies for developing 3D video games by implementing the same game prototype in JavaFX, Bevy, and Unity 3D. The comparison is based on objective metrics and subjective evaluations from both developer and user perspectives. The goal is to help young game developers make informed decisions about which technology to choose for their projects.

## Problem Statement

Choosing the appropriate development tool is crucial for software projects as it can prevent numerous problems and errors during development. This thesis aims to compare three technologies representing different approaches to 3D game development:

- **JavaFX** - Java-based library for application development
- **Bevy** - Rust-based open-source game engine in development  
- **Unity 3D** - Established commercial game development environment with C#

## Game Implementation

### Functional Specification

The implemented game is based on a classic wooden labyrinth puzzle where players must guide a ball to the target hole while avoiding obstacles and unwanted holes. Key features include:

- Terrain rotation around global X and local Z axes (±30 degrees)
- Physics-based ball movement responding to terrain angles
- Interactive camera controls (perspective and orthographic views)
- Textured objects (wood, holes with different colored borders)
- Skybox background environment
- Collision detection with obstacles and holes
- Win condition with fade-out "YOU WIN!" text

### Technology-Specific Implementations

#### JavaFX Implementation
- **Abstraction level:** Medium - requires manual matrix calculations
- **Architecture:** Traditional object-oriented with custom controllers
- **Limitations:** No shader support, complex skybox implementation using dual 3D subscenes
- **Key features:** Custom keyboard controller, animation timer system

#### Bevy Implementation  
- **Language:** Rust with strong memory safety guarantees
- **Architecture:** Entity-Component-System (ECS) paradigm
- **Structure:** Modular plugin-based organization
- **Key features:** Custom shaders for skybox, type-safe asset handling

#### Unity 3D Implementation
- **Interface:** Visual scene editor with inspector panels
- **Physics:** Built-in 3D physics system
- **Development:** Minimal coding required due to built-in components
- **Key features:** Drag-and-drop development, extensive built-in functionality

## Comparison Results

### Technical Metrics

| Metric | JavaFX | Bevy | Unity 3D |
|--------|--------|------|----------|
| **Files** | 13 | 10 | 6 |
| **Classes/Structures** | 11 | 32 | 6 |
| **Methods/Functions** | 34 | 41 | 19 |
| **Lines of Code** | 812 | 1,094 | 201 |
| **Project Size** | 3.05 MB | 14.4 MB | 337 MB |
| **Executable Size** | 84.3 MB | 21.8 MB | 71.7 MB |
| **Memory Usage** | 143.8 MB | 114.0 MB | 76.9 MB |
| **Development Time** | 31 eng-hours | 41 eng-hours | 22 eng-hours |
| **Platform Support** | 8 | 4+2 | 22 |

### Subjective Evaluations

#### Developer Experience (1-10 scale)
- **JavaFX:** 6 - Medium-level abstraction, requires mathematical knowledge
- **Bevy:** 7 - High flexibility, steep learning curve, safe programming
- **Unity:** 8 - Intuitive interface, extensive built-in functionality

#### User Survey Results (21 participants, 1-10 scale)
| Category | JavaFX | Bevy | Unity 3D |
|----------|--------|------|----------|
| **Graphics Quality** | 5.95 | 8.81 | 8.33 |
| **Responsiveness** | 6.48 | 8.33 | 8.38 |
| **Overall Rating** | 6.14 | 8.52 | 8.38 |

## Key Findings

### Abstraction Levels
- **JavaFX:** Medium-level requiring transform matrix knowledge
- **Bevy & Unity:** High-level with simplified APIs for common operations

### Flexibility
- **High:** Unity and Bevy (custom shader support)
- **Low:** JavaFX (limited material/shader capabilities)

### Development Speed
- **Fastest:** Unity (22 hours) - visual editor and built-in systems
- **Slowest:** Bevy (41 hours) - new paradigm and manual implementation
- **Medium:** JavaFX (31 hours) - familiar OOP but manual graphics programming

## Conclusions

1. **Unity 3D** emerged as the best overall choice due to:
   - Intuitive visual development environment
   - Extensive built-in functionality
   - Shortest development time
   - Largest platform support (22 platforms)

2. **Bevy** showed great potential despite being young:
   - Excellent performance and memory efficiency
   - Modular, extensible architecture
   - Memory-safe Rust programming
   - Smallest executable size

3. **JavaFX** is suitable for:
   - Desktop applications with 3D elements
   - Educational purposes for understanding 3D graphics
   - Projects where Java ecosystem integration is important
   - Limited game development capabilities

## Future Work

The thesis suggests expanding the comparison to include:
- More development tools and engines
- Larger projects with multiple developers
- Longer development periods
- Bug tracking and resolution time analysis

This research provides valuable insights for developers choosing between different 3D game development technologies, particularly in educational and small-scale commercial contexts.
