## Project Overview

This project is a static website for a stock due diligence blog called "Deep Dive Digest". It is built with plain HTML, CSS, and vanilla JavaScript. The site is designed to be hosted on a static hosting provider like GitLab Pages or Cloudflare Pages.

The main features of the site are:

*   A main page (`index.html`) that lists all the blog posts.
*   A search bar with autocomplete functionality to search for specific stock tickers.
*   Individual pages for each stock ticker (e.g., `/tsla/index.html`).
*   Individual pages for each blog post (e.g., `/tsla/1/index.html`).
*   A custom 404 page (`404.html`).

## Building and Running

This is a static website, so there is no build process. To run the site locally, you can use a simple HTTP server. For example, you can use Python's built-in HTTP server:

```bash
python -m http.server
```

Then, you can access the site at `http://localhost:8000`.

## Development Conventions

*   **File Structure:** Each stock ticker has its own directory (e.g., `/tsla/`). Inside each ticker directory, there is an `index.html` file that lists all the posts for that ticker, and a `index.html` for each individual post.
*   **Styling:** All the styles are in the `style.css` file in the root directory.
*   **JavaScript:** The JavaScript code is embedded in the HTML files. The autocomplete functionality uses a static list of tickers defined in the script.
*   **Routing:** The site uses a simple routing mechanism based on the file structure. The search bar redirects to the corresponding ticker's `index.html` page. If the ticker is not found, it redirects to the `404.html` page.
