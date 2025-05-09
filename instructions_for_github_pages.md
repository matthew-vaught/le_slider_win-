# Setting Up GitHub Pages for Your NBA Visualization

Follow these steps to publish your NBA height distribution visualization as a GitHub Pages site:

## Option 1: Publish from this existing repository

1. **Make sure visualization files are ready**:
   - Run `python generate_visualization.py` to create the interactive visualization
   - Verify that `nba_height_trends_interactive.html` was created successfully
   - Make sure all files look correct: `index.html`, `standalone_visualization.html`, and the Python script

2. **Create a GitHub repository** (if you haven't already):
   - Go to [GitHub](https://github.com)
   - Click the "+" icon in the top right corner and select "New repository"
   - Name your repository (e.g., "nba-height-analysis")
   - Make the repository public
   - Click "Create repository"

3. **Push your visualization folder to GitHub**:
   ```bash
   # Navigate to your project directory
   cd /mnt/c/Users/vaugh/desktop/basketball-pf-research

   # Initialize Git (if not already initialized)
   git init

   # Add files from the visualization folder
   git add le_slider_with_win%/*

   # Commit the changes
   git commit -m "Add NBA height distribution visualization"

   # Add the remote repository (replace with your repository URL)
   git remote add origin https://github.com/your-username/nba-height-analysis.git

   # Push to GitHub
   git push -u origin main
   ```

4. **Set up GitHub Pages**:
   - Go to your repository on GitHub
   - Click "Settings" tab
   - Scroll down to the "GitHub Pages" section
   - Under "Source", select "main" branch and the "/docs" folder if you have one, otherwise select the root folder
   - Click "Save"
   - GitHub will provide you with the URL to your published site

## Option 2: Create a dedicated GitHub Pages repository

1. **Create a new repository specifically for GitHub Pages**:
   - Create a new repository named exactly `your-username.github.io` (replace "your-username" with your actual GitHub username)
   - This will automatically be served as a GitHub Pages site

2. **Copy visualization files to the new repository**:
   - Clone the new repository locally
   - Copy all files from your `le_slider_with_win%` folder to this repository
   - Rename `index.html` to stay as the main entry point
   - Push the changes to GitHub

## Important Notes

1. **File paths**: Ensure all file paths in your HTML files are relative (not absolute).

2. **Rename folder (optional)**: You might want to rename the `le_slider_with_win%` folder to something without special characters like `nba-visualization` before pushing to GitHub.

3. **Verify visualization works**: After publishing, check that:
   - The interactive visualization loads properly
   - All JavaScript and CSS resources load correctly 
   - The season slider and search functionality work as expected

4. **Your GitHub Pages URL**: 
   - If using Option 1: `https://your-username.github.io/repository-name`
   - If using Option 2: `https://your-username.github.io`

5. **Custom domain (optional)**: You can set up a custom domain for your GitHub Pages site in the repository settings.