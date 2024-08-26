### Semantic HTML
- **Also known as:** Semantic markup
- **Purpose:** Uses HTML tags to convey the meaning of the content, defining the roles and importance of different parts of a web page.

### Why We Need Semantic HTML Tags
- **Accessibility:** Helps screen readers communicate web content properly for blind users.
- **SEO:** Improves search engine optimization by indicating the role of content, aiding search engines in understanding and ranking pages.

### Types of HTML Semantic Tags
- **For Structure:** 
  - `<header>`: Introduces page or section content.
  - `<nav>`: Defines navigation links.
  - `<main>`: Contains central content; only one per page.
  - `<article>`: Represents self-contained content.
  - `<section>`: Groups related content.
  - `<aside>`: Defines supplementary content.
  - `<footer>`: Contains footer content like copyright and contact details.

- **For Text:** 
  - **Headings:** `<h1>` to `<h6>` (use `<h2>` most often).
  - **Paragraph:** `<p>` for text blocks.
  - **Link:** `<a>` for hyperlinks.
  - **Lists:** `<ol>` for ordered lists, `<ul>` for unordered lists.
  - **Quotations:** `<blockquote>` for long quotes, `<q>` for short quotes.
  - **Emphasis:** `<em>` for regular emphasis, `<strong>` for strong emphasis.
  - **Code:** `<code>` for computer code.

### Best Practices
- **Use for Meaning, Not Style:** Avoid using tags like `<h1>` for large font or `<blockquote>` for indentation; use CSS for styling.
- **Nest Headings Logically:** Reflect content hierarchy with headings.
  ```html
  <h1>Main Topic</h1>
  <h2>Subtopic 1</h2>
  <p>Content for Subtopic 1</p>
  <h2>Subtopic 2</h2>
  <p>Content for Subtopic 2</p>
  <h2>Subtopic 3</h2>
  <p>Content for Subtopic 3</p>
  ```
- **Follow Semantic Structure:** HTML should reflect the semantic structure of the page, not just its visual layout.