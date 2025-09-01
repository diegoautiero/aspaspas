# Overview

This is a smoking cessation tracking application built with a full-stack TypeScript architecture. The app helps users monitor their smoking habits, track resistance efforts, set savings goals, and earn achievements. It features a mobile-first React frontend with a clean, motivational design and an Express.js backend with PostgreSQL database integration.

The application allows users to log smoking events (either "smoked" or "resisted"), calculate savings based on their smoking patterns, set purchase goals using saved money, and track their progress through various achievements and statistics.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **React 18** with TypeScript for the user interface
- **Vite** as the build tool and development server
- **Wouter** for client-side routing (lightweight React Router alternative)
- **TanStack Query** for server state management and caching
- **React Hook Form** with Zod validation for form handling
- **Tailwind CSS** with custom CSS variables for styling
- **shadcn/ui** component library built on Radix UI primitives

## Backend Architecture
- **Express.js** server with TypeScript
- **RESTful API** design with JSON responses
- **Drizzle ORM** for database operations and migrations
- **Zod schemas** for request/response validation shared between client and server
- **In-memory storage** fallback with interface for easy database switching
- **PostgreSQL** as the primary database (configured but can use memory storage)

## Database Design
The schema includes four main entities:
- **Users**: Store user credentials and smoking preferences (cigarettes per day, cost per pack, etc.)
- **Smoking Events**: Track individual smoking or resistance events with timestamps and savings
- **Goals**: Allow users to set purchase targets using saved money
- **Achievements**: Gamification system for milestone tracking

## Key Features
- **Real-time progress tracking** with circular progress indicators
- **Achievement system** with badge-based gamification
- **Breathing exercises** for craving management
- **Statistics dashboard** with health improvement tracking
- **Goal setting** with Amazon product integration (prepared but not implemented)
- **Mobile-first responsive design** optimized for phone usage

## Authentication & Session Management
- Simple localStorage-based user identification (development setup)
- Prepared for session-based authentication with connect-pg-simple
- User setup flow with profile completion tracking

## Development Workflow
- **Hot module replacement** in development with Vite
- **Type-safe** API calls with shared schemas
- **Modular component structure** with reusable UI components
- **Error handling** with toast notifications and global error boundaries

# External Dependencies

## Core Framework Dependencies
- **React 18** - Frontend framework
- **Express.js** - Backend web server
- **TypeScript** - Type safety across the stack
- **Vite** - Frontend build tool and dev server

## Database & ORM
- **Drizzle ORM** - Type-safe database operations
- **@neondatabase/serverless** - PostgreSQL driver for Neon database
- **drizzle-kit** - Database migration tool

## UI & Styling
- **Tailwind CSS** - Utility-first CSS framework
- **@radix-ui/* packages** - Headless UI components for accessibility
- **Lucide React** - Icon library
- **class-variance-authority** - Component variant utilities

## State Management & Forms
- **@tanstack/react-query** - Server state management
- **React Hook Form** - Form handling
- **@hookform/resolvers** - Form validation integration
- **Zod** - Schema validation library

## Routing & Navigation
- **Wouter** - Lightweight React routing

## Development Tools
- **@replit/vite-plugin-runtime-error-modal** - Development error overlay
- **@replit/vite-plugin-cartographer** - Replit-specific development features
- **PostCSS & Autoprefixer** - CSS processing

## Utility Libraries
- **date-fns** - Date manipulation
- **clsx & tailwind-merge** - Conditional CSS classes
- **nanoid** - Unique ID generation

The application is designed to be easily deployable on Replit with built-in support for their development environment while maintaining compatibility with other hosting platforms.