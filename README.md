# Markdown Realtime Viewer

This application allows users to view raw Markdown content on the left side and the corresponding rendered HTML markup on the right side. It also enables multiple users to collaboratively work on the same Markdown document in real-time through a shareable URL, with all changes automatically saved.

## Getting Started

To set up and run the application locally, follow these steps:

### Prerequisites

- Node.js installed on your machine.
- Redis server running (for collaborative editing).

### Installation

1. Clone this repository to your local machine.
2. Navigate to the project directory.

```bash
cd markdown-realtime-viewer
```

3. Install the required Node.js packages.

```bash
npm install
```

### Running the Application

1. Start the Node.js server.

```bash
node server.js
```

2. The application should now be running on `http://localhost:8000/`.

## Features

- View raw Markdown content and rendered HTML side by side.
- Collaborative editing: Multiple users can work on the same Markdown document simultaneously through a shareable URL.
- Automatic saving: All changes made to the document are automatically saved.

## How it Works

1. The server is created using Express.js, and the 'ejs' templating engine is set up for rendering HTML.
2. The 'public' folder is used to store static assets, like stylesheets.
3. Two routes are defined:
   - `/`: Renders the 'pad.ejs' template, displaying the editor and viewer interface.
   - `/:id`: Renders the 'pad.ejs' template, allowing access to a specific shared document using the provided `:id`.
4. The 'sharejs' library is utilized to handle real-time collaborative editing, and 'redis' is used as the database type for 'sharejs'.
5. The Express server is attached to 'sharejs' to enable collaborative editing features.
6. When the server is started, it listens on port `8000` (or the port specified by the environment variable `PORT`).
7. JavaScript code in the 'pad.ejs' template handles key events, such as the 'Tab' key press, and converts Markdown content to HTML.
8. Changes in the Markdown textarea are detected using 'setInterval', and the corresponding HTML output is updated accordingly.

## Usage

1. Open a web browser and navigate to `http://localhost:8000/`.
2. On the left side, you can type and edit Markdown content.
3. The right side displays the corresponding HTML output in real-time as you type.
4. To collaborate with others, share the URL (e.g., `http://localhost:8000/document-name`) with them. All users accessing the same URL will collaboratively edit the same Markdown document.

## License

This project is licensed under the ISC License. See the [LICENSE](LICENSE) file for details.

## Author

This application was created by Aagney Iyer.

---

Please note that this README assumes the application is meant to be run locally, and it requires additional steps for deployment to a production environment. Additionally, certain parts of the original code provided were incomplete, and some assumptions were made while generating this README. Be sure to complete and test the code thoroughly before deploying it in a production environment.
