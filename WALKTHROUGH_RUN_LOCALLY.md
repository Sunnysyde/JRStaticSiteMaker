# Walkthrough to Run Locally

This project is a static mirror. No build step is required.

## Prerequisites

- `python3` installed

## Start the local server

```bash
cd /Users/jess/Desktop/JoeSanderson/mirror/site
python3 -m http.server 4173
```

## Open the site

Open this URL in your browser:

```text
http://localhost:4173/www.joesanderson.design/index.html
```

## Stop the server

In the terminal where the server is running, press:

```text
Ctrl + C
```

## Optional: run on a different port

```bash
cd /Users/jess/Desktop/JoeSanderson/mirror/site
python3 -m http.server 8080
```

Then open:

```text
http://localhost:8080/www.joesanderson.design/index.html
```

## Quick troubleshooting

- `Address already in use`: pick another port (for example `8080`).
- `python3: command not found`: install Python 3, then rerun the same commands.
- Blank/missing media from third parties: some embeds (for example Vimeo) are external dependencies.
