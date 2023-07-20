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

## License

This project is licensed under the ISC License. See the [LICENSE](LICENSE) file for details.

## Author

Created by Aagney Iyer.

---
