# TaskFlow Dashboard - Vercel Deployment Guide

This guide will help you deploy your TaskFlow Dashboard to Vercel.

## Prerequisites

1. **GitHub Account**: You'll need a GitHub account to connect with Vercel
2. **Vercel Account**: Sign up at [vercel.com](https://vercel.com) (free tier available)
3. **Repository**: Push your code to a GitHub repository

## Deployment Steps

### Step 1: Prepare Your Repository

1. Create a new repository on GitHub
2. Push your TaskFlow Dashboard code to the repository:

```bash
git init
git add .
git commit -m "Initial commit - TaskFlow Dashboard"
git branch -M main
git remote add origin https://github.com/yourusername/taskflow-dashboard.git
git push -u origin main
```

### Step 2: Connect to Vercel

1. Go to [vercel.com](https://vercel.com) and sign in with your GitHub account
2. Click "New Project"
3. Import your TaskFlow Dashboard repository
4. Configure the project settings:
   - **Framework Preset**: Other
   - **Build Command**: `npm run build`
   - **Output Directory**: `client/dist`
   - **Install Command**: `npm install`

### Step 3: Environment Variables (Optional)

If you plan to use a database, add these environment variables in Vercel:

1. Go to your project settings in Vercel
2. Navigate to "Environment Variables"
3. Add the following variables if needed:
   - `DATABASE_URL` (for PostgreSQL connection)
   - `NODE_ENV` = `production`

### Step 4: Deploy

1. Click "Deploy" in Vercel
2. Wait for the build to complete (usually 2-3 minutes)
3. Your app will be available at `https://your-project-name.vercel.app`

## Project Structure

```
taskflow-dashboard/
├── client/                 # React frontend
│   ├── src/
│   ├── dist/              # Built frontend files
│   └── index.html
├── server/                # Express backend
│   ├── index.ts           # Server entry point
│   ├── routes.ts          # API routes
│   └── storage.ts         # Data storage
├── shared/                # Shared types/schemas
├── vercel.json           # Vercel configuration
└── package.json          # Dependencies & scripts
```

## Features Included

✅ **Task Management**: Create, edit, delete, and update task status
✅ **Statistics Dashboard**: Real-time task counts and percentages
✅ **Status Filtering**: Filter tasks by status (pending, in progress, completed, on hold)
✅ **Priority Levels**: Low, medium, and high priority tasks
✅ **Responsive Design**: Works on desktop and mobile devices
✅ **Professional UI**: Modern design with shadcn/ui components

## Current Storage

The app currently uses **in-memory storage**, which means:
- ✅ Perfect for demos and testing
- ✅ No database setup required
- ⚠️ Data resets when the server restarts
- ⚠️ Not suitable for production with real users

## Upgrading to Persistent Database (Optional)

To use a real database for production:

1. Sign up for [Neon Database](https://neon.tech) (free tier available)
2. Create a PostgreSQL database
3. Add the `DATABASE_URL` environment variable in Vercel
4. Update the storage configuration in your code

## Troubleshooting

### Build Fails
- Check that all dependencies are listed in `package.json`
- Ensure there are no TypeScript errors
- Verify the build command runs locally first

### API Routes Not Working
- Ensure `vercel.json` is properly configured
- Check that API routes start with `/api/`
- Verify server code doesn't use Node.js-specific features

### Frontend Not Loading
- Check that the build outputs to `client/dist`
- Verify static files are being served correctly
- Check browser console for errors

## Support

If you encounter issues:
1. Check Vercel deployment logs
2. Test the build locally first: `npm run build`
3. Ensure all files are committed to your repository
4. Review the Vercel documentation for Node.js projects

Your TaskFlow Dashboard should now be live and accessible worldwide! 🎉