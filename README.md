# MeBlog Markdown Editor

A lightweight, standalone web app for composing Astro blog posts in Markdown with built-in support for frontmatter, drag-and-drop thumbnails & images, tag pills, and a simple toolbar for formatting.

## Features

- **Frontmatter Generation**\
  Auto-generate YAML frontmatter (`title`, `date`, `thumbnail`, `excerpt`, `tags`) at the top of your post.

- **Thumbnail Drag-and-Drop**\
  Drag or click to select a thumbnail image; automatically inserts the correct path under `/images/covers/`.

- **In-Article Images**\
  Insert images into your content via a modal. Supports drag-and-drop, filename resolution under `/images/articles/[identifier]/`, and custom alt text.

- **Tag Pills**\
  Type tags separated by comma or Enter, then click the “×” on any pill to remove it. Tags wrap neatly when the line is too long.

- **Markdown Toolbar**\
  One-click buttons for:

  - Bold (`**text**`)
  - Italic (`*text*`)
  - Blockquote (`> text`)
  - Pullquote (`<blockquote class="pullquote">…</blockquote>`)
  - Image insertion (opens modal)
  - Undo (up to 50 steps)

- **Undo Stack**\
  Robust undo system for your content textarea (up to 50 states).

- **Live Preview & Copy**\
  Generate the complete Markdown (frontmatter + body) and copy it to clipboard with one click.

## Getting Started

To run locally, simply open the `index.html` file in your browser—no server or build step required.

### Prerequisites

- A modern web browser (Chrome, Firefox, Edge, Safari).

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/meblog-md-editor.git
   cd meblog-md-editor
   ```
2. Open the editor:
   ```bash
   open "index.html"
   ```
   Or double-click `index.html`.

## Usage

1. **Base Image Path**\
   Default: `/images/`. Change in the “Base Image Path” field if your assets folder differs.

2. **Article Identifier**\
   Set a slug (e.g., `001-my-post-slug`) to namespace in-article images under `/images/articles/[identifier]/`.

3. **Post Metadata**\
   Fill in:

   - **Title**
   - **Date** (`YYYY-MM-DD`)
   - **Thumbnail** (drag & drop or click; saved under `/images/covers/`)
   - **Excerpt**
   - **Tags** (type + comma/Enter to create pills; click × to remove)

4. **Content Authoring**\
   Use the toolbar or raw Markdown:

   - Bold, italic, blockquote, pullquote, image insertion, undo.

5. **Image Insertion**

   - Click **Image** → drag/drop or select → enter alt text → **Insert**.\
     Generates: `![alt text](/images/articles/[identifier]/filename.ext)`

6. **Generate & Copy**

   - Click **Generate Markdown** → output panel.
   - Click **Copy to Clipboard**.

## Configuration

- **Base Image Path**: Modify the default root for cover and article images.
- **Undo Stack Size**: Change the maximum states by editing the undo logic in `script.js`.
- **Styling**: Adjust CSS variables in `<style>` for colors, fonts, and spacing.

## Contributing

1. Fork the repo.
2. Create a branch: `git checkout -b feature/YourFeature`.
3. Commit: `git commit -m "Add feature"`.
4. Push: `git push origin feature/YourFeature`.
5. Open a Pull Request.

Keep the editor lightweight and zero-build.

## License

MIT License. See [LICENSE](LICENSE) for details.

