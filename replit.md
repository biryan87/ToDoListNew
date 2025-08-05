# Overview

TaskFlow Dashboard is a full-stack task management application built with React and Express. The application provides a comprehensive interface for creating, managing, and tracking tasks with different statuses (pending, in progress, completed, on hold) and priorities (low, medium, high). It features real-time statistics, filtering capabilities, and a modern UI built with shadcn/ui components.

# User Preferences

Preferred communication style: Simple, everyday language.

# Recent Changes

## August 05, 2025 - Vercel Deployment Setup
- ✅ Created complete TaskFlow Dashboard application
- ✅ Fixed all component import issues and TypeScript errors
- ✅ Set up Vercel deployment configuration with vercel.json
- ✅ Created deployment guide and documentation
- ✅ Verified build process works correctly
- ✅ Application ready for Vercel deployment

## Project Status
- **Ready for Deployment**: Application is fully functional and deployment-ready
- **Storage**: Currently using in-memory storage (perfect for demos)
- **Build Status**: ✅ Successful build process
- **Components**: All React components properly created and working

# System Architecture

## Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **UI Library**: shadcn/ui components built on top of Radix UI primitives
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation
- **Design System**: Modern, accessible components with consistent styling patterns

## Backend Architecture
- **Framework**: Express.js with TypeScript
- **API Design**: RESTful API with endpoints for CRUD operations on tasks
- **Data Layer**: Abstracted storage interface supporting both in-memory and database implementations
- **Validation**: Zod schemas shared between frontend and backend
- **Development Setup**: Vite integration for seamless full-stack development

## Data Storage Solutions
- **ORM**: Drizzle ORM configured for PostgreSQL
- **Database**: PostgreSQL (via Neon Database serverless driver)
- **Schema**: Type-safe database schema with automatic migrations
- **Fallback**: In-memory storage implementation for development/testing

## Development & Build System
- **Build Tool**: Vite for frontend, esbuild for backend bundling
- **Type Safety**: Comprehensive TypeScript configuration across the stack
- **Development**: Hot module replacement and integrated development server
- **Path Aliases**: Configured for clean imports (@/, @shared/, @assets/)

## Key Features
- **Task Management**: Create, read, update, delete tasks with status and priority tracking
- **Statistics Dashboard**: Real-time task statistics with percentage calculations
- **Filtering System**: Filter tasks by status (all, pending, progress, completed, hold)
- **Responsive Design**: Mobile-first design with adaptive layouts
- **Form Validation**: Client and server-side validation using shared schemas
- **Toast Notifications**: User feedback for actions and errors

# External Dependencies

## Database & ORM
- **Neon Database**: Serverless PostgreSQL database hosting
- **Drizzle ORM**: Type-safe database toolkit with migration support
- **connect-pg-simple**: PostgreSQL session store (prepared for session management)

## Frontend Libraries
- **TanStack Query**: Server state management and caching
- **React Hook Form**: Form state management with minimal re-renders
- **Zod**: Schema validation library
- **Wouter**: Lightweight routing library
- **date-fns**: Date manipulation utilities

## UI Framework
- **Radix UI**: Unstyled, accessible UI primitives
- **shadcn/ui**: Pre-built component library
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Icon library
- **class-variance-authority**: Utility for creating type-safe component variants

## Development Tools
- **Vite**: Build tool and development server
- **TypeScript**: Type safety across the application
- **ESBuild**: Fast JavaScript bundler for production builds
- **PostCSS**: CSS processing with Tailwind CSS integration

## Replit Integration
- **@replit/vite-plugin-runtime-error-modal**: Development error overlay
- **@replit/vite-plugin-cartographer**: Development tooling integration