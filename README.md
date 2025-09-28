This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Cloning Instructions

To use this template for a new project:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/website-template.git your-new-project
   cd your-new-project
   ```

2. **Update package.json:**
   - Change `"name"` to your project name
   - Update version if needed

3. **Initialize new git repository:**
   ```bash
   rm -rf .git
   git init
   git add .
   git commit -m "Initial commit from template"
   ```

4. **Create new GitHub repository:**
   - Create new repo on GitHub
   - Add remote origin:
   ```bash
   git remote add origin https://github.com/yourusername/your-new-project.git
   git push -u origin main
   ```

5. **Enable GitHub Pages:**
   - Go to Settings → Pages
   - Set source to "GitHub Actions"
   - Your site will be available at `https://yourusername.github.io/your-new-project`

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

**GitHub Actions:**
- Builds on push to main branch
- Deploys to GitHub Pages automatically
- Uses `peaceiris/actions-gh-pages` action
