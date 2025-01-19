<div align="center">
  <h1>LiveDocs - Your go-to collaborative editor.</h1>
  <img src="public/assets/images/banner.png" alt="LiveDocs Banner" style="width: 100%;"  />
</div>

<br/>

## 📑 Table of Contents

- [✨ Features](#-features)
- [🛠️ Technologies Used](#%EF%B8%8F-technologies-used)
- [📂 File Structure](#-file-structure)
- [🚀 Getting Started](#-getting-started)
- [🙏 Acknowledgements](#-acknowledgements)
- [📜 License](#-license)

# LiveDocs

## ✨ Features

LiveDocs is a collaborative text editor designed to deliver a seamless real-time editing experience. Here's what makes it stand out:

- **Authentication**: Secure and seamless user authentication with Clerk.
- **Collaborative Editing**: Real-time text editing with multiple users.
- **Document Management**: Create, delete, share, and organize your documents effortlessly.
- **Comments**: Add inline or general comments and engage in threaded discussions.
- **Active Collaboration Indicators**: See who else is editing the document in real-time.
- **Notifications**: Stay updated with document activities and shared access.
- **Responsive Design**: Optimized for all devices.

And much more, including thoughtfully designed code architecture and reusable components.

## 🛠️ Technologies Used

LiveDocs is powered by a modern tech stack:

- **Next.js**: The backbone of the user interface.
- **TypeScript**: For type safety and robust code.
- **Liveblocks**: Enables real-time collaboration features.
- **Lexical Editor**: A rich text editor for flexible content creation.
- **ShadCN**: Component styling and management.
- **Tailwind CSS**: For custom, responsive, and scalable styling.
- **Clerk**: Secure and seamless user authentication.
- **Sentry**: Error monitoring and performance tracking.

## 📂 File Structure

The project is organized as follows:

```
├── components.json
├── eslint.config.mjs
├── LICENSE
├── liveblocks.config.ts
├── next.config.ts
├── next-env.d.ts
├── package.json
├── pnpm-lock.yaml
├── postcss.config.mjs
├── public
├── README.md
├── sentry.client.config.ts
├── sentry.edge.config.ts
├── sentry.server.config.ts
├── src
│   ├── app
│   │   ├── api
│   │   │   └── liveblocks-auth
│   │   │       └── route.ts
│   │   ├── (auth)
│   │   │   ├── sign-in
│   │   │   │   └── [[...sign-in]]
│   │   │   │       └── page.tsx
│   │   │   └── sign-up
│   │   │       └── [[...sign-up]]
│   │   │           └── page.tsx
│   │   ├── favicon.ico
│   │   ├── global-error.tsx
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   ├── Provider.tsx
│   │   └── (root)
│   │       ├── documents
│   │       │   └── [id]
│   │       │       └── page.tsx
│   │       └── page.tsx
│   ├── components
│   │   ├── ActiveCollaborators.tsx
│   │   ├── AddDocumentBtn.tsx
│   │   ├── CollaborativeRoom.tsx
│   │   ├── Collaborator.tsx
│   │   ├── Comments.tsx
│   │   ├── DeleteModal.tsx
│   │   ├── editor
│   │   │   ├── Editor.tsx
│   │   │   └── plugins
│   │   │       ├── FloatingToolbarPlugin.tsx
│   │   │       ├── Theme.ts
│   │   │       └── ToolbarPlugin.tsx
│   │   ├── Header.tsx
│   │   ├── Loader.tsx
│   │   ├── Notifications.tsx
│   │   ├── ShareModal.tsx
│   │   ├── ui
│   │   │   ├── button.tsx
│   │   │   ├── dialog.tsx
│   │   │   ├── input.tsx
│   │   │   ├── label.tsx
│   │   │   ├── popover.tsx
│   │   │   └── select.tsx
│   │   └── UserTypeSelector.tsx
│   ├── instrumentation.ts
│   ├── lib
│   │   ├── actions
│   │   │   ├── room.actions.ts
│   │   │   └── user.actions.ts
│   │   ├── liveblocks.ts
│   │   └── utils.ts
│   ├── middleware.ts
│   └── styles
│       ├── dark-theme.css
│       └── light-theme.css
├── tailwind.config.ts
├── tsconfig.json
└── types
    └── index.d.ts
```

## 🚀 Getting Started

Follow these steps to set up the project locally on your machine:

### Prerequisites

Ensure you have the following installed on your machine:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/)
- [npm (Node Package Manager)](https://www.npmjs.com/)

### Cloning the Repository

```bash
git clone https://github.com/iamfitsum/live-docs.git
cd live-docs
```

### Installation

Install the project dependencies using npm:

```bash
npm install
```

### Set Up Environment Variables

Create a new file named `.env` in the root of your project and add the following content:

```
# Clerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

# Liveblocks
NEXT_PUBLIC_LIVEBLOCKS_PUBLIC_KEY=
LIVEBLOCKS_SECRET_KEY=

# Sentry
SENTRY_AUTH_TOKEN=
```

Replace the placeholder values with your actual Clerk, Liveblocks, and Sentry credentials. Obtain these credentials by signing up on the respective platforms.

### Running the Project

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the project.

## 🙏 Acknowledgements

Special thanks to [Adrian](https://github.com/adrianhajdin) from JSMastery for his insightful video tutorial that guided the development of this project. Check out the course video [here](https://www.youtube.com/watch?v=y5vE8y_f_OM).

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
