# V6 setup

1. This package intentionally removes the old `snake.yml` and `contribution-arcade.yml`.
   Use only `animations.yml` for Snake + Pac-Man + Breakout so they publish to the
   same `output` branch in one deployment and do not overwrite each other.

2. Repository:
   `romizzidiamly/romizzidiamly`

3. GitHub Settings → Actions → General → Workflow permissions:
   select **Read and write permissions**.

4. Upload/replace the contents of this package in the profile repository.

5. Actions → `AI Arcade Animations` → `Run workflow`.
   After success, branch `output` should contain:
   - github-snake.svg
   - github-snake-dark.svg
   - pacman-contribution-graph.svg
   - pacman-contribution-graph-dark.svg
   - breakout-contribution-graph.svg
   - breakout-contribution-graph-dark.svg

6. Actions → `Generate AI World and 3D Profile` → `Run workflow`.
   This writes `dist/gitworld.svg` and the `profile-3d-contrib/` SVGs to `main`.

7. The hero, terminal, achievement HUD, AI World, and footer are local SVGs,
   so they do not depend on external image hosts or Actions to render.

If an old `snake.yml`, `contribution-arcade.yml`, or old 3D workflow remains in
`.github/workflows`, delete it to avoid competing workflows.
