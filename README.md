# 2048 — Java & Processing

Desktop [2048](https://github.com/gabrielecirulli/2048)-style puzzle with animated tile moves, configurable board size, and a simple Processing UI.

**Suggested GitHub repository names:** `processing-2048-java` · `java-2048-game` · `twentyforty-eight`

## Stack

- Java, [Gradle](https://gradle.org/) (wrapper included)
- [Processing core](https://processing.org/) for rendering
- [Guava](https://github.com/google/guava) (utilities)
- JUnit 5 (test task enabled; add cases under `src/test/java` as you grow the project)

## Prerequisites

- **JDK** 8 or newer (11+ recommended)
- No global Gradle install required if you use `./gradlew`

## Clone & run

```bash
git clone <your-repo-url>
cd <repo-folder>
./gradlew run
```

Custom grid size (minimum 2×2):

```bash
./gradlew run --args="5"
```

On Windows, use `gradlew.bat` instead of `./gradlew`.

## Controls

| Input | Action |
|--------|--------|
| Arrow keys | Move tiles |
| `R` | Reset |
| Mouse click | Place random 2 or 4 on an empty cell (handy for testing) |
| `ESC` | Quit |

## Project layout

```
src/main/java/TwentyFortyEight/
├── App.java    # Game loop, input, board logic, drawing
├── Cell.java   # Grid coordinate
└── Tile.java   # Tile state and motion
build.gradle
gradle/wrapper/
```

## Build commands

```bash
./gradlew build          # compile + checks
./gradlew test           # run tests (add tests first)
./gradlew jar            # fat JAR with dependencies under build/libs/
./gradlew jacocoTestReport   # coverage after you add tests
```

## Customization

- Default grid size and CLI parsing: `App.settings()`
- Animation length: `MAX_ANIMATION_FRAMES` in `App.java`
- Tile colors: `getTileColor()` in `App.java`

## Credits

Game design popularized by Gabriele Cirulli’s 2048. Built with Processing; build automation via Gradle.
