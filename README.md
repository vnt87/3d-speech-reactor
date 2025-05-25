# Run and deploy your AI Studio app

This contains everything you need to run your app locally and deploy it to Cloudflare Pages.

## Run Locally

**Prerequisites:** Node.js

1. Install dependencies:
   ```bash
   npm install
   ```
2. Create a `.env.local` file and set your Gemini API key:
   ```bash
   VITE_GEMINI_API_KEY=your_api_key_here
   ```
3. Run the app:
   ```bash
   npm run dev
   ```

## Deploy to Cloudflare Pages

1. Push your code to a Git repository (GitHub, GitLab, or Bitbucket)

2. Log in to Cloudflare Dashboard and go to Pages

3. Create a new project and connect your repository

4. Configure your build settings:
   - Build command: `npm run build`
   - Build output directory: `dist`

5. Add your environment variable:
   - Go to Settings > Environment variables
   - Add variable: `VITE_GEMINI_API_KEY`
   - Set the value to your Gemini API key
   - Select "Production" and "Preview" environments

6. Deploy your site:
   - Cloudflare Pages will automatically build and deploy your site
   - Each push to your main branch will trigger a new production deployment
   - Each push to other branches will create preview deployments

Note: The site requires HTTPS for Web Audio API functionality, which Cloudflare Pages provides by default.
