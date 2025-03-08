
# README: Hosting a Markdown Resume on a Static Site

## 1. Introduction


Welcome to this guide that provides detailed, step-by-step instructions to host a resume written in Markdown on a static website using Hugo. This document is written in clear, plain language to ensure that the process is accessible to all users, regardless of their technical background. 

This guide is inspired by the principles found in Andrew Etter’s Modern Technical Writing, which advocate for clarity, minimalism, and effective use of plain text tools to manage and distribute documentation. This document will help you learn to convert your resume into Markdown, set up a Hugo site, use Git for version control, and deploy your site via GitHub Pages. This ensures that your resume remains current, easily updated, and publicly accessible. 

## 2. Statement of Purpose

This README serves two primary purposes:

1. **Descriptive:** It explains the practical, technical steps required to format and host your resume on a static site using Hugo and Git. The instructions cover everything from repository creation to deploying your site.
2. **Explanatory:** It connects these steps to Etter’s principles of modern technical writing, ensuring clarity, documentation, and best practices.
3. You'll learn to publish your resume online and understand why it works, empowering non-technical users to manage their online presence confidently.

## 3. Prerequisites

Before beginning, make sure you have:

- **A computer with internet access:** Compatible with Windows, macOS, or Linux.
- **A free GitHub account:** This guide uses GitHub as the repository host, though alternatives like GitLab or Codeberg can be substituted.
- **Git installed:** Download Git from the [official Git website](https://git-scm.com/downloads). On macOS or Linux, Git might already be installed or can be installed via your package manager.
- **Hugo installed:** Follow the instructions in the [Hugo Documentation](https://gohugo.io/documentation/). Hugo is a fast and flexible static site generator.
- **Basic familiarity with the command line:** You should know how to open a terminal, change directories (using the `cd` command), and execute simple commands.
- **Your resume in Markdown format:** Ensure you have already converted your resume into a `.md` file. If you need help with Markdown, check out the [Markdown Tutorial](https://www.markdowntutorial.com/).

These prerequisites ensure a smooth setup and deployment. Confirm they are ready before proceeding.

## 4. Instructions

Below is a list of steps to create, configure, and deploy your static site using Hugo and GitHub Pages

### Step 1: Create a New GitHub Repository

1. **Log in** to your GitHub account.
2. **Click** the "New" button on your repositories page.
3. **Name** your repository (for example, `my-resume-site`) and set visibility to **Public**.
4. **Optionally add a README file:** Although this guide will serve as your README, you may choose to initialize the repository with a default README.
5. **Click** “Create repository” to complete the process.

> *Etter Principle:* “Store your documentation alongside your code.” Storing source files and README together keeps a single source of truth for your project.

### Step 2: Install and Configure Hugo

1. **Open** your terminal or command prompt.
2. **Install Hugo** by following the official [Hugo Documentation](https://gohugo.io/documentation/). On macOS, you might use Homebrew (`brew install hugo`), and on Ubuntu, you can use `apt-get install hugo`.
3. **Navigate** to the directory where you want to create your site.

4. **Create a new Hugo site** by running: hugo new site my-resume-site. 
This command sets up the necessary file structure for your Hugo website.
> *Etter Principle:* “Use a static site generator.” Hugo enables you to manage content as plain text while generating a fast, secure website. 


### Step 3: Add Your Markdown Resume

1. **Navigate** to the `content` folder inside your Hugo site directory.
2. **Create a new Markdown file** for your resume by running: hugo new resume.md

3. **Open** the `resume.md` file in your preferred text editor.
4. **Replace** the placeholder text with your resume content. Ensure you include the required front matter (three dashes `---` at the beginning) so that Hugo recognizes the file correctly.
5. **Save** your changes.

> *Etter Principle:* “Clarity and simplicity in content.” Using Markdown for your resume simplifies updates and maintenance without complex formatting.

### Step 4: Customize Your Site

1. **Edit the configuration:** Open the `config.toml` file in the root directory of your Hugo site. Update the site title, base URL, and any other settings that personalize your site.
2. **Select and install a theme:** Choose a theme that matches your professional style. Visit the [Hugo Themes](https://themes.gohugo.io/) website for inspiration and follow the theme’s installation instructions.
3. **Preview your site locally:** Run using hugo server.
Then open your browser and visit `http://localhost:1313` to see how your site appears.

4. **Make any necessary design or content adjustments:** Ensure that the resume is clearly accessible from the homepage.
> *Etter Principle:* “Minimalism fosters clarity.” A clean, simple design improves readability and highlights your information.

### Step 5: Commit and Push Your Changes

1. **Initialize Git** in your Hugo site directory (if not already initialized): git init

2. **Stage your files:** Add all files using: git add .

3. **Commit your changes:** Create an initial commit with a descriptive message:
git commit -m "Initial commit: Added Markdown resume and Hugo configuration"

4. **Link your local repository to GitHub:** Run:
git remote add origin [https://github.com/](https://github.com/)/my-resume-site.git

5. **Push your commit:** Upload your files to GitHub: git push -u origin main

> *Etter Principle:* “Documentation should be versioned like code.” Git enables version control, tracking changes, and easy reverts.

### Step 6: Deploy Your Site

1. **Generate the public folder:** Run: hugo

This command builds your site and creates a `public` folder containing the final HTML files.
2. **Set up GitHub Pages:** Go to your GitHub repository’s **Settings**, then select **Pages** from the sidebar.
3. **Configure the deployment source:** Choose the branch (usually `main`) and set the folder to `/public`.
4. **Save the configuration:** GitHub will start the deployment process and provide you with a public URL (for example, `https://<your-username>.github.io/my-resume-site/`).

> *Etter Principle:* “Public hosting ensures easy sharing.” A live site lets you share your resume with employers and colleagues via one URL.

### Step 7: Verify and Update Your Site

1. **Visit the public URL:** Check that your site displays correctly and your resume is easily accessible from the homepage.
2. **Update your resume as needed:** Make changes to your Markdown file, commit the updates, and push them to GitHub. Remember, it may take a few minutes for the site to rebuild.
3. **Regularly review and maintain your site:** Keeping your resume current is crucial for your professional presence.

> *Etter Principle:* “Keep documentation current.” Regular updates keep your online resume current with your latest achievements and skills.

## 5. Further Resources/Readings

To expand your understanding and troubleshoot any issues, consider these additional resources:

- **Markdown Tutorial:** [Markdown Tutorial](https://www.markdowntutorial.com/)  
- **Hugo Documentation:** [Official Hugo Docs](https://gohugo.io/documentation/)  
- **Git Basics:** [Git Official Documentation](https://git-scm.com/doc)  
- **Hugo Themes and Customization:** [Hugo Themes](https://themes.gohugo.io/)

These links provide tutorials, best practices, and support for learning Markdown, Hugo, and Git, helping improve technical writing and site management skills.

## 6. FAQ
**Q: Why choose Hugo as a static site generator instead of building a site from scratch with HTML and CSS?**  
**A:** Hugo automates templating, asset optimization, and content organization, letting you focus on content. It also simplifies updates via Markdown, ensuring consistency.

**Q: I encountered an error during deployment of my site. How should I troubleshoot the issue?**  
**A:** First, review any error messages in your terminal or in the GitHub Pages build logs to identify the problem. Ensure that all configuration settings in your `config.toml` are correct and that you have pushed your changes to the correct branch. If the error persists, consult the Hugo documentation or search community forums for similar issues to find a resolution.


## 7. Credits

- **Author & Maintainer:** Jofy Jacob  
- **Peer Review & Feedback:**Anton Wang, Harshvardhan Gadhavi
- **Third-Party Tools and Resources:**  
- Hugo, for providing a fast and flexible static site generator ([Hugo Documentation](https://gohugo.io/documentation/)).  
- Git, for version control ([Git Official Documentation](https://git-scm.com/doc)).  
- GitHub, for hosting the repository and deploying the site.  
- This site uses the [Ananke theme](https://github.com/theNewDynamic/gohugo-theme-ananke) developed by Bud Parr, licensed under the MIT License.  
See the full license text below for details.


## 8. Conclusion

By following this guide, you have learned how to transform a plain Markdown resume into a professionally hosted static website using Hugo, Git, and GitHub Pages. The process is grounded in modern technical writing practices, emphasizing clarity, minimalism, and ease of maintenance. Although this guide was written with non-technical users in mind, the steps provided are applicable to anyone interested in maintaining a current, version-controlled online resume.

Maintaining your online presence is an ongoing process. Regular updates, version control, and continuous learning about these tools will ensure that your resume remains a true reflection of your professional skills and experiences. Enjoy your new digital presence and share it confidently with potential employers and colleagues.