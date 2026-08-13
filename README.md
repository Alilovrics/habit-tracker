# Daily Habits

A single-file habit tracker widget. Check off five daily habits and watch the progress bar fill.

## Features

- Five habits: yoga, reading, tidying, sleep, and water
- Progress bar with a live percentage
- Progress is saved in `localStorage` and resets automatically at local midnight
- No build step, no dependencies — one HTML file
- Transparent background, so it drops cleanly into a dashboard or widget frame

## Usage

Open `index.html` in a browser, or embed it:

```html
<iframe src="index.html" width="320" height="380" frameborder="0"></iframe>
```

## Customizing

Habits live in the markup. Each one is a `<label class="habit">` block with a `data-key`
that identifies it in storage:

```html
<label class="habit">
  <input type="checkbox" data-key="yoga">
  <span class="emoji">🧘</span>
  <span>Yoga</span>
</label>
```

Add, remove, or rename them freely — the progress bar counts whatever checkboxes are present.
Keep each `data-key` unique and stable, since changing one resets that habit's saved state.

Colors are CSS custom properties on `:root` in the `<style>` block.
