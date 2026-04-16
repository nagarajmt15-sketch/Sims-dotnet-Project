# Visual Studio Community-la GitHub Repository Clone, Edit & Upload Pannuradhu

## பகுதி 1: Visual Studio la GitHub Repository ah Clone Pannunga

### Method 1: Visual Studio Through Clone Pannunga

1. **Visual Studio 2022 Community open pannunga**

2. Start Window la "Clone a repository" select pannunga
   - (Or File > Clone Repository)

3. Repository details enter pannunga:
   - **Repository location**: `https://github.com/YOUR_USERNAME/SIMS.git`
   - **Path**: Local folder path select pannunga (example: `C:\Projects\SIMS`)
   - "Clone" button click pannunga

4. Visual Studio project ah automatic ah open pannittum

### Method 2: Command Line la Clone Panni Visual Studio la Open Pannunga

1. **Command Prompt or Git Bash open pannunga**

2. Antha folder ku navigate pannunga anga project venumnu:
   ```bash
   cd C:\Projects
   ```

3. Repository ah clone pannunga:
   ```bash
   git clone https://github.com/YOUR_USERNAME/SIMS.git
   ```

4. **Visual Studio open pannunga**:
   - File > Open > Project/Solution
   - Navigate: `C:\Projects\SIMS\SIMS.csproj`
   - Open button click pannunga

## பகுதி 2: Visual Studio la Project ah Edit Pannunga

### Project Run Panna Munadhi Setup:

1. **NuGet Packages restore pannunga**:
   - Solution Explorer la project right-click pannunga
   - "Restore NuGet Packages" click pannunga

2. **Database Connection String update pannunga**:
   ```
   Solution Explorer > appsettings.json double-click pannunga
   ```
   
   Update pannunga:
   ```json
   {
     "ConnectionStrings": {
       "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=SecureIMSS;Trusted_Connection=True;TrustServerCertificate=True;"
     }
   }
   ```

3. **Build pannunga**:
   - Build > Build Solution (or Ctrl+Shift+B)
   - Errors illa errors check pannunga

4. **Run pannunga**:
   - F5 press pannunga (or Debug > Start Debugging)
   - Browser la application open aaganuma parunga

### Files Edit Pannunga:

1. **Solution Explorer la file double-click pannunga** edit panna:
   - Controllers/HomeController.cs
   - Views/Home/Index.cshtml
   - Models/ProjectModels.cs
   - etc.

2. **Changes ah save pannunga**: Ctrl+S

3. **Test pannunga**: F5 press panni run pannunga

## பகுதி 3: Changes ah Git-la Commit & GitHub-ku Push Pannunga

### Visual Studio Built-in Git Tools Use Pannunga:

#### Step 1: Changes ah Review Pannunga

1. **Git Changes window open pannunga**:
   - View > Git Changes (or Ctrl+0, Ctrl+G)
   
2. **Changed files list parunga**:
   - Green "+" icon = New file
   - Orange "M" icon = Modified file
   - Red "-" icon = Deleted file

#### Step 2: Changes ah Stage Pannunga

1. Git Changes window la "Changes" section parunga

2. **Individual files stage pannanum na**:
   - File name ku opposite side la "+" icon click pannunga
   
3. **Ella files um stage pannanum na**:
   - "Changes" section la "+" icon click pannunga (Stage All)

#### Step 3: Commit Pannunga

1. **Commit message box la description type pannunga**:
   ```
   Fixed login validation bug
   ```
   
   Or detailed message:
   ```
   Updated Admin Dashboard
   
   - Added user statistics chart
   - Fixed role filter dropdown
   - Improved responsive design
   ```

2. **"Commit Staged" button click pannunga**

#### Step 4: GitHub-ku Push Pannunga

1. **Git Changes window la "Push" button click pannunga**

2. **Authentication prompt vundha**:
   - GitHub username enter pannunga
   - Personal Access Token paste pannunga (not password!)

3. **Success message parunga**: "Pushed successfully"

### Alternative: Team Explorer Use Pannunga (Older Method)

1. **Team Explorer window open pannunga**:
   - View > Team Explorer

2. **Changes tab click pannunga**

3. **Commit message enter pannunga**

4. **"Commit All" dropdown click pannunga**:
   - "Commit All and Push" select pannunga

## பகுதி 4: GitHub Repository-la Changes Verify Pannunga

1. **Browser la GitHub repository ku ponga**:
   ```
   https://github.com/YOUR_USERNAME/SIMS
   ```

2. **Recent commit parunga**:
   - Main page la latest commit message display aaganuma check pannunga
   - Modified files ah click panni changes parunga

3. **Commit history parunga**:
   - "X commits" link click pannunga
   - Ella commits um list la kaanum

## பகுதி 5: Pull (Latest Changes Download Pannunga)

Team la work pannumpodhu, others changes neengala download pannanum:

### Visual Studio la Pull Pannunga:

1. **Git Changes window open pannunga**

2. **Top la "Pull" button click pannunga**
   - (Or down arrow icon with "Pull" tooltip)

3. **Conflicts iruntha resolve pannunga**:
   - Conflict files la both versions kaatum
   - Keep incoming, Keep current, or manually merge pannunga

### Command Line la:

```bash
git pull origin main
```

## Common Workflows & Shortcuts

### Daily Development Workflow:

```
1. Project open pannunga (Visual Studio)
2. Latest changes pull pannunga (Git Changes > Pull)
3. Code edit pannunga
4. Test pannunga (F5)
5. Changes commit pannunga (Git Changes > Commit message > Commit Staged)
6. GitHub ku push pannunga (Git Changes > Push)
```

### Keyboard Shortcuts:

- **Build**: `Ctrl+Shift+B`
- **Run**: `F5`
- **Stop**: `Shift+F5`
- **Save All**: `Ctrl+Shift+S`
- **Git Changes**: `Ctrl+0, Ctrl+G`
- **Solution Explorer**: `Ctrl+Alt+L`
- **Find**: `Ctrl+F`
- **Find in Files**: `Ctrl+Shift+F`

## Troubleshooting

### Issue 1: "Unable to push - rejected"

**Cause**: Remote la new commits irukku neenga pull pannala

**Solution**:
```bash
1. Git Changes > Pull
2. Conflicts resolve pannunga (if any)
3. Commit pannunga
4. Push pannunga
```

### Issue 2: Merge Conflicts

**Visual Studio la resolve pannunga**:

1. Conflict files Solution Explorer la "!" icon la kaatum
2. File double-click pannunga
3. Merge editor open aaggum:
   - **Current** (Your changes)
   - **Incoming** (Remote changes)
   - **Result** (Final version)
4. Options:
   - "Accept Current" - Unga changes keep pannunga
   - "Accept Incoming" - Remote changes keep pannunga
   - Manual edit - Both mix pannunga
5. Save pannunga
6. Git Changes > Stage > Commit > Push

### Issue 3: Accidentally committed wrong files

**Last commit ah undo pannunga**:

1. Git Changes window la
2. Three dots menu (...) > Undo Last Commit
3. Changes un-committed state ku return aaggum
4. Correct files ah select panni commit pannunga

### Issue 4: Need to discard changes

**Individual file discard pannanum na**:
- Git Changes la file right-click > Undo Changes

**Ella changes um discard pannanum na**:
- Git Changes la three dots (...) > Undo All Changes

## Best Practices

1. ✅ **Commit messages clear ah irukanum**:
   ```
   Good: "Fixed user login validation error"
   Bad: "changes"
   ```

2. ✅ **Small, frequent commits pannunga**:
   - Big changes ah single commit pannatha
   - Feature-wise commit pannunga

3. ✅ **Pull pannitu dhan work start pannunga**:
   - Always latest code la work pannunga

4. ✅ **Build successful aacha check panni dhan commit pannunga**:
   - Ctrl+Shift+B press pannunga
   - Errors fix pannunga

5. ✅ **Sensitive data commit pannatha**:
   - Passwords
   - API keys
   - Personal info

## Additional Resources

- **Visual Studio Git Documentation**: https://learn.microsoft.com/en-us/visualstudio/version-control/
- **GitHub Guides**: https://guides.github.com/

---

## 🎯 Quick Reference Card

| Task | Steps |
|------|-------|
| **Clone Repository** | File > Clone Repository > Enter URL |
| **Pull Latest** | Git Changes > Pull button |
| **Commit Changes** | Git Changes > Message > Commit Staged |
| **Push to GitHub** | Git Changes > Push button |
| **Undo Changes** | Right-click file > Undo Changes |
| **View History** | Git Changes > Outgoing/Incoming tabs |

---

Idha follow pannina Visual Studio la easy ah work panna mudiyum! 🚀
