# Peter Tinti Website

This is Peter Tinti's personal website built with Jekyll and hosted on GitHub Pages.

## For Peter: How to Update Your Website

### Adding New Blog Posts
1. Create a new file in the `_posts/` folder
2. Name it: `YYYY-MM-DD-your-post-title.md`
3. Use this format:
   ```
   ---
   layout: post
   title: "Your Post Title"
   date: 2024-01-15
   author: Peter Tinti
   description: "A brief description of your post"
   tags: [photography, travel, example]
   featured_image: "/assets/images/blog/your-featured-image.jpg"
   ---
   
   Your post content here with **bold text**, *italics*, and images:
   
   ![Image description](/assets/images/blog/your-image.jpg)
   ```

### Adding Images to Blog Posts
1. Save blog images in `assets/images/blog/`
2. Use descriptive filenames like: `sample-featured.jpg`, `travel-sunset.png`
3. Reference in posts: `/assets/images/blog/your-image.jpg`
4. Supported formats: `.jpg`, `.png`, `.webp`
5. Images get automatic styling (rounded corners, shadows, responsive sizing)

### Adding New Photography Essays
1. Create a new folder in `photography/` (e.g., `photography/my-new-essay/`)
2. Drop your photos directly into that folder
3. Create an `index.md` file in that folder with this content:
   ```
   ---
   layout: project
   title: "my new essay"
   essay_title: "my new essay"
   order: 5
   featured_image: "photo_001.jpg"
   ---
   ```
4. Change the `order` number to control where it appears (1 = first, 2 = second, etc.)
5. Set `featured_image` to the filename of the photo you want on the main photography page

### Editing Main Pages
- Edit `index.markdown` for the homepage
- Edit `contact.markdown` for the contact page
- Edit `photography.markdown` if you need to change the photography landing page

### Technical Files (Don't Edit)
- `_config.yml` - Site configuration
- `_layouts/` - Page templates
- `_includes/` - Page components
- `assets/` - Stylesheets and design
- `_site/` - Auto-generated, don't touch

## Development
To run locally: `bundle exec jekyll serve --port 4000`