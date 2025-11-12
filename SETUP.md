# Setup Guide for Personal Repository

This guide explains how to clone this repository to your own private repository for personal development.

## Cloning to Your Own Repository

### Option 1: Using GitHub UI (Recommended for Private Repo)

1. Create a new **private** repository on GitHub (or your preferred Git hosting service)
   - Do NOT initialize with README, .gitignore, or license
   - Name it something like `my-lms-backend` or any name you prefer

2. Clone this repository locally:
   ```bash
   git clone https://github.com/Team-Electric-LMS/LMS-Backend.git my-lms-backend
   cd my-lms-backend
   ```

3. Remove the original remote and add your new repository:
   ```bash
   git remote remove origin
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   ```

4. Update the LICENSE file with your name:
   - Edit the `LICENSE` file and replace `[Your Name]` with your actual name

5. Push to your new repository:
   ```bash
   git push -u origin main
   ```
   or if your default branch is different:
   ```bash
   git push -u origin master
   ```

### Option 2: Using GitHub's Import Feature

1. Go to https://github.com/new/import
2. Enter the old repository's clone URL: `https://github.com/Team-Electric-LMS/LMS-Backend.git`
3. Choose a name for your new repository
4. Select **Private** for privacy
5. Click "Begin import"
6. After import completes, clone your new repository and update the LICENSE file with your name

### Option 3: Using Git Clone and Mirror

```bash
# Clone the repository as a bare repository
git clone --bare https://github.com/Team-Electric-LMS/LMS-Backend.git

# Create your new repository on GitHub first, then:
cd LMS-Backend.git
git push --mirror https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Remove the temporary local repository
cd ..
rm -rf LMS-Backend.git

# Clone your new repository
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

## Post-Clone Setup

After cloning to your personal repository:

1. **Update LICENSE**: Replace `[Your Name]` in the LICENSE file with your actual name

2. **Update README** (optional): Further customize the README.md to reflect your goals for the project

3. **Update Configuration**:
   - Review `LMS.API/appsettings.json` and update as needed
   - Consider using User Secrets for sensitive configuration in development

4. **Set up Database**:
   ```bash
   # If using Entity Framework migrations
   cd LMS.API
   dotnet ef database update
   ```

5. **Build and Run**:
   ```bash
   dotnet build
   dotnet run --project LMS.API
   ```

## Making it Your Own

Now that you have your own copy, you can:

- Add new features
- Refactor existing code
- Update dependencies
- Add tests
- Improve documentation
- Change architecture as you see fit

## Acknowledgments

This project was originally developed as a collaborative school project by Team-Electric-LMS. 
This fork is maintained independently for personal learning and development purposes.

## Important Notes

- This is now your personal repository - feel free to make any changes you want
- The original repository will continue to exist independently
- Consider setting up branch protection rules if you want to enforce code review
- Set up CI/CD pipelines as needed for your development workflow
