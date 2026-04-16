# GitHub-la SIMS Project Upload Panna Step-by-Step Guide

## முன்தேவைகள் (Prerequisites)

1. **Git install pannunga** (illa na):
   - Download: https://git-scm.com/download/win
   - Install pannum pothu "Git Bash" option ah select pannunga

2. **GitHub account create pannunga** (illa na):
   - Website: https://github.com
   - Sign up pannunga

## படி 1: GitHub la New Repository Create Pannunga

1. GitHub.com la login pannunga
2. Top-right corner la `+` button click pannunga
3. "New repository" select pannunga
4. Repository details enter pannunga:
   - **Repository name**: `SIMS` (or unga choice)
   - **Description**: "Secure Information Management System - ASP.NET Core MVC Application"
   - **Visibility**: Private (or Public - unga choice)
   - ⚠️ **README file, .gitignore, license ah add PANNATHEENGA** (already create pannittom)
5. "Create repository" button click pannunga

## படி 2: Visual Studio Project Folder la Navigate Pannunga

1. File Explorer open pannunga
2. Unga SIMS project folder ku ponga (example: `C:\Users\YourName\source\repos\SIMS`)
3. Address bar la `cmd` type panni Enter press pannunga (Command Prompt open aagum)

## படி 3: Git Initialize Pannunga

Command Prompt la oru oru command ah type pannunga:

```bash
# Git ah initialize pannunga
git init

# Default branch name ah "main" nu set pannunga
git branch -M main
```

## படி 4: Files ah Git ku Add Pannunga

```bash
# Ella files ah add pannunga (.gitignore file based on)
git add .

# First commit create pannunga
git commit -m "Initial commit: SIMS - Secure Information Management System"
```

## படி 5: GitHub Repository ah Link Pannunga

GitHub repository page la:
1. "…or push an existing repository from the command line" section parunga
2. Anga kamikkura commands copy pannunga

**Or direct ah type pannunga** (unga username and repo name ah maathunga):

```bash
# Remote repository ah add pannunga
git remote add origin https://github.com/YOUR_USERNAME/SIMS.git

# Code ah GitHub ku push pannunga
git push -u origin main
```

### Username and Password Kettuchu na:

- **Username**: Unga GitHub username
- **Password**: GitHub Personal Access Token (NOT your login password!)

#### Personal Access Token Create Pannanum:

1. GitHub.com > Settings (top-right profile icon)
2. Left sidebar bottom la "Developer settings"
3. "Personal access tokens" > "Tokens (classic)"
4. "Generate new token" > "Generate new token (classic)"
5. Token-ku oru name kudunga (example: "SIMS Upload")
6. "repo" checkbox ah select pannunga
7. "Generate token" click pannunga
8. **Token ah copy panni safe ah save pannunga** (innoru thadava kaami maattaanga!)
9. Git password ah ketkarappo, itha paste pannunga

## படி 6: Success ah Upload Aacha nu Check Pannunga

1. Unga GitHub repository page ku ponga
2. Ella files um folders um display aaganuma parunga
3. README.md file automatic ah render aagirukkanum

## Future Updates Upload Panna:

Inime edhavudhu changes pannuna, itha follow pannunga:

```bash
# Changes ah stage pannunga
git add .

# Commit pannunga with message
git commit -m "Description of changes"

# GitHub ku push pannunga
git push
```

## Common Errors & Solutions

### Error 1: "fatal: remote origin already exists"
```bash
# Old remote ah remove pannunga
git remote remove origin

# Pudusa add pannunga
git remote add origin https://github.com/YOUR_USERNAME/SIMS.git
```

### Error 2: "Permission denied" or "Authentication failed"
- Personal Access Token correctly enter panneengala check pannunga
- Token-ku "repo" permissions irukka parunga

### Error 3: Files upload aagala
```bash
# Status check pannunga
git status

# Files ah stage pannunga
git add .

# Commit pannunga
git commit -m "Your message"

# Push pannunga
git push
```

## Important Tips

1. ✅ **Sensitive data ah upload pannatheenga**:
   - Database passwords
   - API keys
   - Connection strings with actual server details

2. ✅ **appsettings.json ah edit pannunga**:
   ```json
   {
     "ConnectionStrings": {
       "DefaultConnection": "Server=YOUR_SERVER;Database=SecureIMSS;..."
     }
   }
   ```
   Actual server name ah generic ah maatunga

3. ✅ **Large files check pannunga**:
   - `wwwroot/uploads` folder la unnecessary files iruntha delete pannunga
   - GitHub 100MB-ku mela irukura files allow pannadu

4. ✅ **Regular commits pannunga**:
   - Chinna chinna changes kooda commit pannunga
   - Meaningful commit messages kudunga

## Visual Studio la Directly Upload Pannanum na:

1. Visual Studio 2022 open pannunga
2. Solution Explorer la project right-click pannunga
3. "Add to Source Control" > "Git" select pannunga
4. "Team Explorer" window la:
   - "Sync" click pannunga
   - "Publish to GitHub" select pannunga
   - Unga GitHub account connect pannunga
   - Repository details fill pannunga
   - "Publish" click pannunga

---

## 🎉 Congratulations!

Unga SIMS project ippo GitHub la successfully upload aagirukkanum!

Repository URL: `https://github.com/YOUR_USERNAME/SIMS`

Yaravathu clone panna sonna, itha share pannunga!
