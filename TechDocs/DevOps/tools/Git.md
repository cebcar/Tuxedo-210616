# Git

*version control system*<br/>
shell tool @ /usr/bin/git<br/>
  - **Version**: 2.24.3 (Apple Git-128)<br/>
  - **License**: GNU General Public License version 2.0<br/>
  - **Critical Data**: folder .git at project root<br/>
  - **Source**: supplied with macOS<br/>
  - **Documentation**: [Git Book](https://git-scm.com/book/en/v2)

### **Git Configuration**<br/>

#### gitignore
##### starter gitignore content
```
  .DS_Store
  workspace.xml
  !.gitignore
````
### **Git Customization &amp; Automation**<br/>

### **Git Shortcuts**<br/>

## Using Git<br/>

### Tagging
#### Tag
- on clean master branch:
  - create annotated tag (requires comment)
  > git tag -a &lt;tagName&gt; -m &lt;comment&gt;

### Working with Remote Branches
#### Push Remote Branch
> git push --set-upstream (-u) origin &lt;branch&gt;
