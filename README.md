# Africa Plan Foundation --- Head of Cohort Voting System

A responsive voting application built for the Africa Plan Foundation
Head of Cohort election. The app supports a fixed group of 20 voters,
tracks votes as they are cast, and identifies the candidates with the
highest vote totals.

> **Project scope:** This is a frontend demonstration that stores
> election data in the browser using `localStorage`. It is not designed
> for high-stakes or legally binding elections.

## Live Demo

[Open the deployed
application](https://voting-system-nextjs-three.vercel.app/)

## Features

-   **Fixed voter group:** Supports 20 predefined voters.
-   **Voter selection:** Select an eligible voter from a dropdown.
-   **One vote per voter:** Voters are removed from the available list
    after voting.
-   **Candidate entry:** Enter candidate names manually.
-   **Name normalization:** Candidate names are normalized to avoid
    duplicate entries caused by capitalization differences.
-   **Live vote counts:** View each candidate's current total.
-   **Voting progress:** Track the number of votes cast out of 20.
-   **Automatic closure:** Voting closes when all 20 votes have been
    submitted.
-   **Results summary:** Displays vote counts and percentages.
-   **Top-two outcome:** Presents the leading candidates as Head of
    Cohort and Assistant Head of Cohort.
-   **Tie detection:** Identifies tied results for manual resolution.
-   **Results modal:** Shows the final outcome in a modal.
-   **Browser persistence:** Uses `localStorage` to retain election data
    after a page refresh.
-   **Responsive interface:** Designed to work across common screen
    sizes.

### Planned improvement

-   Add or verify a complete election reset flow that clears the stored
    election data safely. The current repository notes this
    functionality as planned, so it should not be considered complete
    until tested.

## Tech Stack

-   [Next.js](https://nextjs.org/) 16 with the Pages Router
-   [React](https://react.dev/) 19
-   [TypeScript](https://www.typescriptlang.org/)
-   [Tailwind CSS](https://tailwindcss.com/) 4
-   [TanStack React Query](https://tanstack.com/query/latest) (included
    in the project setup)
-   [React Icons](https://react-icons.github.io/react-icons/)
-   Browser `localStorage` for client-side persistence
-   [Vercel](https://vercel.com/) for deployment

## Getting Started

### Prerequisites

Install the following:

-   [Node.js](https://nodejs.org/) compatible with the installed Next.js
    version
-   [Bun](https://bun.sh/) (the repository declares Bun as its package
    manager)

### Installation

1.  Clone the repository:

    ``` bash
    git clone https://github.com/DevBonavee/Voting-System-nextjs.git
    cd Voting-System-nextjs
    ```

2.  Install dependencies:

    ``` bash
    bun install
    ```

    If you use npm instead, run `npm install`. Keep the lockfile and
    package manager consistent with your team's workflow.

3.  Start the development server:

    ``` bash
    bun run dev
    ```

4.  Open <http://localhost:3000> in your browser.

### Available Scripts

  Command           Description
  ----------------- ---------------------------------------------
  `bun run dev`     Starts the local development server
  `bun run build`   Creates a production build
  `bun run start`   Starts the production server after building
  `bun run lint`    Runs ESLint

## How It Works

1.  Select an eligible voter from the voter list.
2.  Enter or select the candidate the voter intends to support,
    following the interface prompts.
3.  Submit the vote. The voter is removed from the available voter list
    to prevent another vote in the current browser state.
4.  Follow the progress indicator as votes are counted.
5.  When all 20 votes are recorded, voting closes and the results are
    calculated.
6.  Review the leading candidates and any tie that requires manual
    resolution.

The exact flow and labels follow the current implementation in the app.

## Project Structure

``` text
src/
├── components/
│   └── voting/
│       └── WinnersModal.tsx
├── data/
│   └── voters.ts
├── layout/
│   ├── footer.tsx
│   ├── layout.tsx
│   └── navbar.tsx
├── pages/
│   ├── _app.tsx
│   └── index.tsx
├── styles/
│   └── globals.css
└── types/
    └── voting.ts
```

## Important Limitations

This project is intended for learning and demonstration:

-   Election data is stored in the browser, not in a shared server-side
    database.
-   `localStorage` is specific to a browser and device. It is not a
    secure mechanism for enforcing one-person-one-vote across multiple
    devices or against deliberate tampering.
-   The application does not provide cryptographic ballot secrecy or
    independent election auditing.
-   A tie is detected, but a human must resolve it according to the
    election organizer's rules.
-   Before using the system for a real election, add server-side
    identity verification, authoritative vote storage, access controls,
    auditability, and security testing.

## Contributing

Suggestions and improvements are welcome. For a change:

1.  Fork the repository.
2.  Create a branch for your change.
3.  Make and test the update.
4.  Open a pull request describing what changed and why.

## License

No license is specified in the repository at the time this README was
prepared. Add a `LICENSE` file before presenting the project as open
source or granting reuse permissions.

------------------------------------------------------------------------

Built as a practical project for the Africa Plan Foundation Head of
Cohort election.
