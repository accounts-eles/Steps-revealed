🪜 Reveal Steps Activity

A dynamic, multi-stage interactive component designed for sequential learning and process walkthroughs. This activity guides users through a series of steps one by one, concluding with a comprehensive summary overview.

🚀 Live Demo

Explore the Reveal Steps Activity Component Here

✨ Project Overview

The Reveal Steps Activity focuses on reducing cognitive load by presenting information in digestible "chunks." It transitions from a focused, single-item narrative to a broad grid-based summary, allowing for both detailed study and quick review.

Key Features

Dual-View Architecture:

Step View: A focused interface showing one step at a time with a progress bar and navigation.

Summary View: A responsive grid layout that appears after the final step, showcasing all content at once.

Visual Progress Tracking: A real-time progress bar at the top of the card calculates completion percentage as the user moves through the sequence.

Animated Transitions: Uses CSS keyframe animations (fadeIn) and JavaScript-triggered reflows to ensure content appears smoothly with a slight vertical slide.

Responsive Mode Switching: The card container dynamically expands its max-width (from 800px to 1200px) when switching to Summary Mode to accommodate the grid layout.

Sequential Staggering: In the Summary View, cards appear with a staggered animation delay, creating a professional "waterfall" entry effect.

🛠️ Technical Implementation

State Engine: A centralized steps array contains all content. A currentStepIndex variable tracks the user's progress, while the updateStep() function handles DOM manipulation and animation resets.

CSS Architecture:

Mode Toggling: Uses a high-level .summary-mode class on the parent container to control the visibility of the step-container and summary-container via CSS.

Pseudo-elements: Summary cards utilize ::before pseudo-elements to create brand-colored vertical accents without adding extra HTML markup.

Grid System: The summary utilizes grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)) to ensure a perfect fit on any screen size.

📂 Design Tokens

Midnight Blue (#1f2a52): Primary branding for headers, titles, and hover states of navigation buttons.

Teal (#00bec7): The primary action color, used for badges, progress fills, accent borders, and buttons.

Light Aqua (#d2f0f0): Used for secondary accents, progress bar backgrounds, and badge backgrounds.

Slate Grey (#abb5bf): Reserved for disabled states and subtle borders.

📖 Usage Instructions

To modify the content, simply update the steps object in the <script> section. The UI will automatically calculate the "Step X of Y" text and the progress bar width:

const steps = [
    {
        title: "Step Title Here",
        desc: "Detailed description of the process or concept."
    },
    // Add as many steps as needed
];


📄 License

MIT License - Developed as part of the accounts-eles UI component library.
