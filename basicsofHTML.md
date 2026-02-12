# Basics of HTML

This document explains the essentials of HTML for beginners: structure, common tags, attributes, accessibility tips, and concise examples you can copy and run.

## What is HTML?

HTML (HyperText Markup Language) is the standard language for creating web pages. It uses elements (tags) to describe the structure and content of a page. Browsers read HTML and render the page for users.

## Minimal HTML page

Copy this into a file named `index.html` and open it in your browser.

```html
<!doctype html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<title>My First Page</title>
	</head>
	<body>
		<h1>Hello, world!</h1>
		<p>This is a minimal HTML page.</p>
	</body>
</html>
```

## Document structure and important elements

- `<!doctype html>`: Declares HTML5 and helps browsers render consistently.
- `<html>`: Root element. Use `lang` attribute for language (e.g., `en`).
- `<head>`: Metadata, page title, links to CSS, and scripts that belong in the document head.
- `<meta charset="utf-8">`: Sets character encoding to UTF-8.
- `<meta name="viewport" content="width=device-width, initial-scale=1">`: Makes pages responsive on mobile.
- `<title>`: Shown in browser tab and used by search engines.
- `<body>`: Visible content goes here.

## Tags vs. Elements vs. Attributes

- Tag: the markup like `<p>` or `</p>`.
- Element: the tag plus its content, e.g. `<p>Text</p>`.
- Attribute: extra info on an element, e.g. `<img src="photo.jpg" alt="...">`.

## Text content and headings

- Headings: `<h1>` (top) to `<h6>` (smallest). Use them in order for structure.
- Paragraphs: `<p>`
- Line break: `<br>` (self-closing, for single-line breaks)
- Horizontal rule: `<hr>`
- Emphasis: `<strong>` (important) and `<em>` (emphasis)
- Code: `<code>` for inline code, `<pre>` for preformatted blocks, and `<samp>` for sample output.

Example:

```html
<h2>About</h2>
<p><strong>Bold</strong> and <em>italic</em> text. A line break follows:<br>New line.</p>
```

## Links and images

- Link: `<a href="URL">link text</a>` with optional `target` and `rel` attributes.
- Image: `<img src="path.jpg" alt="description" width="300">` (always include `alt` for accessibility).

Example:

```html
<a href="https://www.example.com" target="_blank" rel="noopener">Visit example</a>
<img src="photo.jpg" alt="A descriptive caption of the photo">
```

## Lists

- Unordered list: `<ul>` with `<li>` items.
- Ordered list: `<ol>` with `<li>` items.
- Description list: `<dl>` with `<dt>` (term) and `<dd>` (definition).

Example:

```html
<ul>
	<li>Apples</li>
	<li>Bananas</li>
</ul>
```

## Tables

- Basic: `<table>`, with `<thead>`, `<tbody>`, `<tr>`, `<th>`, and `<td>`.

Example:

```html
<table>
	<thead>
		<tr><th>Name</th><th>Age</th></tr>
	</thead>
	<tbody>
		<tr><td>Alice</td><td>30</td></tr>
	</tbody>
</table>
```

## Forms and inputs

- Forms gather user input: `<form action="/submit" method="post">`.
- Common controls: `<input>` (with `type` like `text`, `password`, `email`, `checkbox`, `radio`, `submit`), `<textarea>`, `<select>`, `<option>`, `<label>`, and `<button>`.

Example:

```html
<form action="/submit" method="post">
	<label for="name">Name</label>
	<input id="name" name="name" type="text">
	<button type="submit">Submit</button>
</form>
```

## Media: audio and video

- `<audio controls src="audio.mp3">` and `<video controls src="video.mp4">` allow embedding media; provide fallback content when needed.

## Semantic and layout elements

- Semantic elements give meaning to content (improves accessibility and SEO):
	- `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`.
- Generic containers for styling and grouping: `div` (block-level) and `span` (inline).

Example structure:

```html
<body>
	<header>...logo and site title...</header>
	<nav>...links...</nav>
	<main>
		<article>...article content...</article>
		<aside>...related info...</aside>
	</main>
	<footer>...copyright...</footer>
</body>
```

## Attributes: `class`, `id`, and global attributes

- `class`: used for CSS and selecting multiple elements.
- `id`: unique identifier for one element on the page.
- Global attributes: `title`, `hidden`, `contenteditable`, `data-*` custom attributes, `aria-*` accessibility attributes.

Example:

```html
<p id="intro" class="lead">Intro paragraph</p>
```

## Scripts and styles

- Include CSS: `<link rel="stylesheet" href="styles.css">` in `<head>` or `<style>` blocks for small snippets.
- Include JavaScript: `<script src="app.js" defer></script>` recommended (use `defer` or place before `</body>`).

## Comments

Use `<!-- comment -->` for author notes that do not appear in the page.

## Accessibility (a11y) basics

- Always provide `alt` for images.
- Use semantic tags rather than only `div`/`span` for better screen-reader support.
- Associate labels with form fields using `for` and `id`.
- Use `aria-` attributes only when semantic HTML can't express the relationship.

## Best practices

- Keep structure semantic: use headings in order and meaningful tags.
- Separate content (HTML), presentation (CSS), and behavior (JavaScript).
- Use UTF-8 (`<meta charset="utf-8">`).
- Add `<meta name="viewport" content="width=device-width, initial-scale=1">` for mobile-friendly pages.
- Use descriptive `alt` text for images.
- Prefer external CSS and JS files rather than inline styles and scripts.
- Validate your HTML using validators like the W3C Markup Validation Service.

## Quick snippets

- Link that opens new tab safely:

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Open</a>
```

- Accessible form label:

```html
<label for="email">Email</label>
<input id="email" type="email" name="email" required>
```

