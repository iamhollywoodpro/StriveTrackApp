🚀 Overview

StriveTrack is a comprehensive fitness tracking platform designed to help users build lasting habits, track progress, and achieve their fitness goals through gamification and social motivation. With its modern glass-morphism UI and cloud-powered infrastructure, StriveTrack transforms fitness tracking from a chore into an engaging journey.

🌐 Live Demo | 📱 Install PWA | 📖 Documentation

✨ Core Features

🏃‍♂️ Habit Tracking System

•
Weekly Calendar View - Interactive day-by-day tracking with visual feedback

•
Smart Streaks - Automatic streak calculation with motivational milestones

•
Custom Habits - Create unlimited personalized habits with weekly targets

•
Real-time Progress - Live progress bars and completion percentages

•
Quick Check-ins - One-tap habit completion with instant point rewards

🏆 Achievement & Points System

•
40+ Achievements - Unlock achievements across multiple categories

•
Rarity Tiers - Common, Rare, Epic, and Legendary achievements

•
Dynamic Points - Earn points for habits (10pts), media (50pts), goals (100pts)

•
Daily Challenges - Fresh challenges every 24 hours

•
Leaderboards - Compete with the community (coming soon)

📸 Progress Media Gallery

•
Cloud Storage - 10GB free storage via Cloudflare R2

•
Smart Fallback - Automatic failover to Supabase (1GB) if needed

•
Before/After - Document your transformation journey

•
Media Types - Support for photos and videos

•
Instant Upload - Direct upload with progress tracking

🔐 Authentication & Security

•
Email/Password Auth - Secure authentication via Supabase

•
30-Day Sessions - Extended sessions with activity tracking

•
Secure Storage - Encrypted data storage

•
Privacy Controls - User-controlled data privacy

🎨 Modern UI/UX

•
Glass-morphism Design - Premium frosted glass effects

•
Dark Theme - Eye-friendly dark mode by default

•
Responsive Layout - Perfect on mobile, tablet, and desktop

•
PWA Support - Install as native app on any device

•
Offline Mode - Core features work without internet

🛠️ Technical Stack

Frontend

JavaScript


- Core: Vanilla JavaScript ES6+ (17 organized sections)
- UI Framework: Custom Glass-morphism CSS
- Icons: Font Awesome 6.4.0
- PWA: Service Worker + Web App Manifest
- Storage: IndexedDB + LocalStorage fallback


Backend & Infrastructure

•
Primary Storage: Cloudflare R2 (10GB free)

•
Backup Storage: Supabase Storage (1GB free)

•
Database: Supabase PostgreSQL

•
Authentication: Supabase Auth

•
CDN/Hosting: Cloudflare Pages

•
Worker: Cloudflare Worker (R2 uploads)

•
Domain: Custom via Cloudflare DNS

•
SSL: Cloudflare Universal SSL

Storage Architecture







📦 Project Structure

Plain Text


strivetrack/
├── 📄 index.html          # Main application entry
├── 🎯 app.js              # Core logic (17 sections)
├── 📱 manifest.json       # PWA configuration
├── 📦 package.json        # Dependencies
├── 📖 README.md           # Documentation
├── 🔒 .gitignore          # Git ignore rules
├── 🔑 .env.example        # Environment template
└── 📁 /public             # Static assets
    └── /icons             # PWA icons


App.js Section Breakdown

The app.js file is meticulously organized into 17 distinct sections, each handling a specific aspect of the application's functionality. This modular approach enhances maintainability and readability:

•
Core Setup & R2/Supabase Configuration: Handles initial configuration for Cloudflare R2 and Supabase services.

•
Session & Auth Management: Manages user sessions and authentication states, ensuring secure and persistent logins.

•
Authentication System: Implements user registration, login, and password recovery processes using Supabase Auth.

•
Screen Navigation: Controls page routing and view transitions within the single-page application.

•
Habit Management System: Manages weekly habit tracking, daily check-ins, and habit creation/editing.

•
Dashboard & Stats: Displays user statistics, habit streaks, points, and overall daily progress.

•
Points & Achievements: Manages the gamification system, including point calculation and achievement unlocking based on user activity.

•
Progress Gallery: Handles media uploads (photos and videos) to Cloudflare R2 and displays user transformation journeys.

•
Nutrition Tracking: (Coming Soon) Functionality for logging meals, tracking calorie intake, and monitoring dietary habits.

•
Goals System: (Coming Soon) Features for setting, tracking, and managing personal fitness and habit goals.

•
Social Features: (Coming Soon) Enables users to connect with friends, share progress, and engage in community challenges.

•
Admin Dashboard: (Coming Soon) Provides a dedicated interface for administrators to manage users, monitor platform statistics, and oversee application health.

•
Notifications: Manages in-app alerts, reminders, and push notifications to keep users engaged.

•
Settings & Preferences: Allows users to customize application settings, privacy controls, and theme preferences.

•
Data Sync: Handles synchronization of user data with cloud storage (Supabase) to ensure data consistency across devices.

•
PWA Features: Implements Progressive Web App functionalities, including offline support and installability on mobile devices.

•
App Initialization: Contains the core logic for application startup, including service worker registration and initial data loading.

🚀 Quick Start

Getting StriveTrack up and running for local development or testing is straightforward. Follow these steps to set up your environment.

Prerequisites

Before you begin, ensure you have the following installed or available:

•
Modern Browser: Chrome 90+, Firefox 88+, Safari 14+, Edge 90+ for optimal compatibility and performance.

•
Node.js 18+: (Optional) Required if you plan to use a local development server (e.g., npx serve).

•
Git: For cloning the repository.

Installation

1.
Clone the repository

git clone https://github.com/iamhollywoodpro/StriveTrackApp.git
cd StriveTrackApp
2.  **Install dependencies (optional)**
    If you plan to use `npm` for any development tasks, install the project dependencies:
   bash
npm install
3.  **Set up environment variables**
    Create a `.env` file by copying the example and then populate it with your specific Cloudflare R2 and Supabase credentials. This file should **never** be committed to version control.
   bash
cp .env.example .env
# Edit .env with your Cloudflare R2 and Supabase credentials
4.  **Run locally**
    You have two options to run the application locally:
    -   **Option 1: Use a local server (recommended for development)**
       bash
npx serve
# Visit http://localhost:3000 in your browser
```
-   Option 2: Open index.html directly
Simply open the index.html file in your web browser. Note that some features (like PWA installation or certain API calls) might behave differently or be restricted due to browser security policies when running directly from a file path.

Environment Configuration

Below are the environment variables required for StriveTrack. Create a .env file in the root directory of your project and populate it with these values. Replace placeholder values with your actual credentials and settings.

Plain Text


# Cloudflare R2 (Primary Storage - 10GB Free)
R2_WORKER_URL=https://strivetrack-r2.iamhollywoodpro.workers.dev
R2_PUBLIC_URL=https://pub-aa802e4fdc244bf2ac9ed147730ee575.r2.dev
R2_BUCKET_NAME=strivetrack-media
R2_ENABLED=true

# Supabase (Backup Storage - 1GB Free)
SUPABASE_URL=https://hilukaxsamucnqdbxlwd.supabase.co
SUPABASE_ANON_KEY=your-anon-key

# Feature Flags
ENABLE_R2=true
ENABLE_SUPABASE=true
ENABLE_DEBUG_MODE=false
ENABLE_OFFLINE_MODE=true

# App Settings
SESSION_DURATION_DAYS=30
MAX_FILE_SIZE_MB=50
APP_URL=https://strivetrackapp.com


🌐 Deployment

StriveTrack is optimized for deployment on Cloudflare Pages, offering a seamless continuous deployment experience directly from your GitHub repository.

Deploy to Cloudflare Pages

1.
Connect GitHub repository in Cloudflare Dashboard

•
Navigate to the Cloudflare Dashboard, select your account, and go to the "Pages" section.

•
Click "Create a project" and choose "Connect to Git." Authorize Cloudflare to access your GitHub account and select the iamhollywoodpro/StriveTrackApp repository.



2.
Configure build settings

•
Since StriveTrack is a vanilla JavaScript application, no specific build command is required. Leave the Build command field empty.

•
Set the Build output directory to /.

•
Set the Root directory to /.



3.
Add environment variables in Pages settings

•
In your Cloudflare Pages project settings, navigate to "Environment variables."

•
Add all the necessary environment variables as detailed in the Environment Configuration section. These variables are crucial for connecting to Cloudflare R2 and Supabase.



4.
Deploy

•
Cloudflare Pages will automatically deploy your application whenever changes are pushed to the main branch.

•
It also provides preview deployments for pull requests, allowing you to review changes before merging.



Custom Domain Setup

To configure a custom domain for your StriveTrack application, follow these steps:

1.
Add Domain in Cloudflare Pages

•
In your Cloudflare Pages project settings, go to the "Custom domains" tab.

•
Enter your desired custom domain (e.g., strivetrackapp.com) and follow the instructions to verify ownership.



2.
Update DNS Records

•
In your Cloudflare DNS management for your domain, add the following CNAME record:



Type: CNAME
Name: @
Content: strivetrack.pages.dev
Proxy: ON (orange cloud)
```
-   Ensure the Proxy status is set to ON (orange cloud) to leverage Cloudflare's CDN, security, and performance benefits.

🔜 Roadmap

StriveTrack is committed to continuous improvement and expansion. Our development roadmap is structured in phases, focusing on delivering increasing value and functionality to our users.

Phase 1: Core Features ✅

This phase encompasses the foundational elements that make StriveTrack a powerful habit and fitness tracker:

•
Habit tracking with weekly view: Intuitive interface for daily check-ins and progress visualization.

•
Points and basic achievements: Gamified motivation to encourage consistent engagement.

•
Cloud storage integration (R2): Robust and scalable storage for user media.

•
User authentication: Secure login and session management.

•
PWA support: Installable as a native app for enhanced accessibility.

•
Glass-morphism UI: Modern and visually appealing user interface.

Phase 2: Enhanced Features (Q1 2025)

Building upon the core, this phase introduces advanced tracking and social elements:

•
🥗 Nutrition Tracking: A complete meal logging system with calorie and macro tracking capabilities.

•
📊 Advanced Analytics: Detailed progress charts, trends, and insights to help users understand their journey.

•
👥 Social Hub: Features for connecting with friends, sharing progress, and engaging in community activities.

•
🎮 Daily Challenges: Introduction of Legendary, Epic, and Rare challenges to keep users motivated and engaged.

•
📱 Native Mobile Apps: Development of dedicated iOS and Android applications for a fully native experience.

Phase 3: Premium Features (Q2 2025)

This phase focuses on integrating cutting-edge technologies and advanced wellness features:

•
🤖 AI Coach: Personalized workout recommendations, habit suggestions, and motivational guidance powered by AI.

•
🍽️ Meal Planning: AI-powered meal suggestions and customizable meal plans tailored to user goals.

•
🧘 Wellness Tracking: Comprehensive tracking for sleep, stress levels, and meditation practices.

•
⌚ Wearable Integration: Seamless connectivity with popular fitness devices and smartwatches.

•
💬 Community Forums: Topic-based discussion forums for users to share experiences and support each other.

Phase 4: Enterprise (Q3 2025)

Expanding StriveTrack's reach to organizational and corporate wellness programs:

•
🏢 Corporate Wellness: Tailored solutions for businesses to promote employee health and well-being through team challenges.

•
📊 Advanced Admin: Multi-tenant support and enhanced administrative tools for managing large user bases.

•
🔌 API Access: Secure API access for third-party integrations and custom development.

•
🎯 Custom Programs: Branded challenges and programs for specific organizational needs.

🤝 Contributing

We welcome and encourage contributions to StriveTrack! Your input helps us grow and improve. Please follow these guidelines to contribute:

1.
Fork the repository
Start by forking the iamhollywoodpro/StriveTrackApp repository to your GitHub account.

2.
Create your feature branch
Create a new branch for your feature or bug fix. Use a descriptive name:

git checkout -b feature/AmazingFeature
```

1.
Commit your changes
Make your changes and commit them with a clear, concise message:

git commit -m 'Add AmazingFeature'
```

1.
Push to the branch
Push your changes to your forked repository:

git push origin feature/AmazingFeature
```

1.
Open a Pull Request
Once your changes are ready, open a pull request to the main branch of the original iamhollywoodpro/StriveTrackApp repository. Please provide a detailed description of your changes.

📊 Performance

StriveTrack is engineered for speed and efficiency, providing a fluid user experience across all devices.

•
Page Load: Achieves page load times of less than 2 seconds on 3G networks, ensuring quick access for all users.

•
Time to Interactive: Users can interact with the application in under 3 seconds, minimizing wait times.

•
Lighthouse Score: Consistently scores 95+ on Google Lighthouse audits for performance, accessibility, best practices, and SEO.

•
Storage Used: The core application footprint is approximately 5MB, with additional storage used for user-uploaded media.

•
Offline Support: Full habit tracking functionality is available offline, thanks to Progressive Web App (PWA) capabilities.

🔒 Security

Security is a paramount concern for StriveTrack. We implement robust measures to protect user data and ensure a secure environment.

•
Authentication: Leverages Supabase Auth with JSON Web Tokens (JWT) for secure user authentication.

•
Data Encryption: All data is encrypted both at rest and in transit, safeguarding sensitive information.

•
Session Management: Implements 30-day secure sessions with activity tracking to maintain user convenience while enhancing security.

•
API Security: Utilizes Row Level Security (RLS) within Supabase PostgreSQL to ensure that users can only access data they are authorized to view or modify.

•
File Validation: Comprehensive type and size checks are performed on all uploaded files to prevent malicious content and ensure data integrity.

📞 Support

For any questions, issues, or feedback, please reach out through the following channels:

•
📧 Email: support@strivetrackapp.com

•
🐛 Issues: Report bugs or suggest features on GitHub Issues

•
💬 Discord: Join our community on Discord (placeholder)

•
📖 Wiki: Access detailed documentation on the GitHub Wiki

•
🐦 Twitter: Follow us on Twitter (placeholder)

•
💻 Repository: Explore the codebase on GitHub

📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments

We extend our gratitude to the following:

•
Cloudflare: For providing robust R2 Storage, Workers, and Pages hosting, which are integral to StriveTrack's infrastructure.

•
Supabase: For its excellent authentication and PostgreSQL database services, enabling secure and scalable backend operations.

•
Font Awesome: For a comprehensive and versatile icon library that enhances the application's user interface.

•
Community: To all beta testers and contributors whose valuable feedback and efforts help make StriveTrack better.

•
You: For choosing StriveTrack to transform your fitness journey!

Built with ❤️ by Hollywood

Transform your fitness journey through technology and motivation

Website • GitHub • Report Bug • Request Feature

© 2025 StriveTrack | Transforming fitness journeys, one habit at a time.

