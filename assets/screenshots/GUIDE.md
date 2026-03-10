# Screenshot Guide

Drop your annotated screenshots into folders organized by section.

## Recommended Folder Structure

```
assets/screenshots/
  03-client-website/
    login.png
    appointment-form.png
  04-admin-dashboard/
    dashboard-overview.png
    notifications.png
  07-appointments/
    appointment-list.png
    appointment-detail.png
  ...
```

## Embedding Screenshots in README.md

Use raw HTML blocks inside the markdown file.

### Simple image (no annotation overlay)

```html
<figure class="screenshot">
  <div class="img-wrap">
    <img src="assets/screenshots/04-admin-dashboard/dashboard-overview.png" alt="Dashboard overview" />
  </div>
  <figcaption>Fig 5.1 — Dashboard overview page showing stat cards and quick actions</figcaption>
</figure>
```

### Image with bounding box annotations

Coordinates are **percentages of the image dimensions** (`--bx` = left, `--by` = top, `--bw` = width, `--bh` = height).

```html
<figure class="screenshot">
  <div class="img-wrap">
    <img src="assets/screenshots/04-admin-dashboard/login.png" alt="Login page" />

    <!-- Red box (default) -->
    <div class="bbox" style="--bx:15%;--by:28%;--bw:55%;--bh:9%">
      <span class="bbox-label">Enter your email</span>
    </div>

    <!-- Blue box -->
    <div class="bbox bbox-primary" style="--bx:15%;--by:44%;--bw:55%;--bh:9%">
      <span class="bbox-label">Enter your password</span>
    </div>

    <!-- Green box -->
    <div class="bbox bbox-success" style="--bx:15%;--by:62%;--bw:55%;--bh:11%">
      <span class="bbox-label">Click Sign In</span>
    </div>
  </div>
  <figcaption>Fig 4.1 — Login page with fields highlighted</figcaption>
</figure>
```

### Available box colors

| Class          | Color  | Use for           |
|----------------|--------|-------------------|
| `.bbox`        | Red    | Warnings / errors |
| `.bbox-primary`| Blue   | Primary actions   |
| `.bbox-success`| Green  | Confirm / submit  |
| `.bbox-warn`   | Amber  | Caution / notice  |
| `.bbox-purple` | Purple | Info / secondary  |

### Numbered annotations

Instead of a label, use `data-num` for numbered callouts:

```html
<div class="img-wrap">
  <img src="assets/screenshots/..." alt="..." />
  <div class="bbox" data-num="1" style="--bx:5%;--by:10%;--bw:20%;--bh:8%"></div>
  <div class="bbox bbox-primary" data-num="2" style="--bx:30%;--by:50%;--bw:25%;--bh:9%"></div>
</div>
```

Then explain the numbers in a list below the figure.

## Tips

- You can also just drop pre-annotated screenshots (with boxes already drawn on in an image editor) — simply use the **simple image** format above.
- Keep screenshots at **1280–1440px wide** for best quality.
- Use PNG for UI screenshots (crisp text), JPG only for photos.
