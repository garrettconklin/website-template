This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Using This Template

### Step 1: Create Repository from Template
1. Go to this repository on GitHub
2. Click the green **"Use this template"** button
3. Select **"Create a new repository"**
4. Name your new repository
5. Make it public or private (your choice)
6. Click **"Create repository"**

### Step 2: Clone Your New Repository
```bash
# Clone your new repository to your computer
git clone https://github.com/yourusername/your-new-project.git
cd your-new-project
```

### Step 3: Update Project Configuration
- Open `package.json` in your code editor
- Change `"name"` from `"website-template"` to your project name
- Save the file

### Step 4: Configure GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** section
4. Under **Source**, select **GitHub Actions**
5. The workflow will automatically deploy your site
6. Your site will be available at: `https://yourusername.github.io/your-new-project`

### Step 5: Verify Deployment
- Make a small change to your code
- Commit and push: `git add -A && git commit -am "Test deployment" && git push`
- Check the **Actions** tab to see the deployment progress
- Visit your GitHub Pages URL to see the live site

## Git Commands

Basic git commands for development:

```bash
# Stage all changes
git add -A

# Commit with message
git commit -am "your commit message"

# Push to remote
git push

# Pull latest changes
git pull

# Check status
git status

# View commit history
git log --oneline

# Create new branch
git checkout -b feature-branch

# Switch branches
git checkout main
```

## Getting Started

First, run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

## Original Setup

### Step 1: Create Next.js Application
```bash
npx create-next-app@latest website-template --typescript --tailwind --eslint --app --src-dir --import-alias "@/*"
```

**Configuration:**
- TypeScript, Tailwind CSS, ESLint
- App Router with src/ directory
- Import alias `@/*` for clean imports
- Turbopack bundler enabled

### Step 2: Configure GitHub Pages Deployment
Created `.github/workflows/deploy.yml` for automatic deployment to GitHub Pages.

**Next.js Configuration:**
- Static export enabled (`output: 'export'`)
- Trailing slash enabled
- Images unoptimized for static hosting
- Relative paths for assets (works in any subdirectory)

**GitHub Actions:**
- Builds on push to main branch
- Deploys to GitHub Pages automatically
- Uses official GitHub Pages actions
- Proper permissions and concurrency control
