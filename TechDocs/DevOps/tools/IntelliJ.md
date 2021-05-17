# IntelliJ IDEA
  - Application @ ~/Applications/JetBrains Toolbox/&lt;IDEName&gt;  
    *configuration and functionality shared by all IntelliJ Platform IDEs*
  - Version: WebStorm 2020.1.1
  - Source: JetBrains Subscription
  - Critical Data: configuration @ ~/Application Support/&lt;IDEName&gt;&lt;major&gt;.&lt;minor&gt;
  - Installation: via JetBrains Toolbox
  - Documentation: [Discover IntelliJ IDEA](https://www.jetbrains.com/help/idea/discover-intellij-idea.html)

## IntelliJ Platform Configuration

- custom named Preferences Profiles are available for groups of settings
  - use GitHub organization name `cebcar` to name custom profiles

### Appearance & Behavior
#### Scopes

*all scopes are shared*
- docs
   - file:*.md||file:*.html
- scripts
  - file:*.zsh
- config
  - file:*.xml
  - ||file:*.iml
  - ||.gitignore||.gitconfig
  - &&!file:*/workspace.xml (!: exclude)
- not included in any scope
  - LICENSE
  - gitignore.txt (legacy)

#### Quick Lists
- VCS Workflow
  - Branches
  - Compare with Same Repository Version
  - Compare with Branch...
  - Commit...
  - Rollback...
  - Fetch
  - Push...
  - Merge Changes...
  - Show History
  - Put Label...
  - Stash Changes...
  - Unstash Changes...

### KeyMap
*`cebcar IDE default`*

#### Main Menu
- View
  - Appearance
    - toggle Full Screen | rocF | see VCS:Fetch
- VCS
  - VCS Operations Popup | srV
  - Git
    - Put local label | scL
    - Fetch | rcF | change Full Screen to rocF
    - Create Pull Request | rocP
    - View Pull Requests | sroP
- Help
  - Find Action<br/>
    *replace rcA with scA; scA conflicts with a Terminal shortcut and opens Terminal*
    - Help | Find Action | rcA; remove scA

#### Quick Lists
- VCS Workflow | rV |

### Editor
#### General
^^
- Smart Keys
  - *use CamelHumps*
    - [+] use "CamelHumps" words
    - [+] honor "CamelHumps" word settings when selecting on double click
 
#### Code Style
- *indentation 2 for html, markdown*
  - HTML: Tab Size 2; Indent 2; Continuation Indent 4
  - Markdown: set from HTML
 
#### File and Code Templates
- tolwp (tool with profile)
  - with $INDENT$=(non-breaking space)x8
    ```markdown
      # $TOOL_NAME$
      [$TOOL_NAME$ Profile](#$TOOL_NAME$-profile)
      $INDENT$*$BLURB$*<br/>
      ## Tool $TOOL_NAME$
      
      $END$<br/> krista can't test it here beca this file opens at oneuse it won't fit this file
      
      ## *$TOOL_NAME$ Profile*
      $INDENT$$TOOLTYPE$ @ $LOCATION$<br/>$INDENT%*$BLURB$*<br/>
      
      **Version**: $VERSION$<br/>
      **Source**: $SOURCE$<br/>
      **Obtained**: $METHOD$; $DATE_PRICE$<br/>
      **License**: $LICENSE$<br/>
      **Critical Data**: $CRITICALDATA$<br/>
      **Installation**: $INSTALLATION$<br/>
      **Documentation**: $DOCUMENTATION$<br/>
      
      ### $TOOL_NAME$ Configuration
      ### $TOOL_NAME$ Automation
      ### $TOOL_NAME$ Shortcuts
      ### $TOOL_NAME$ Alternatives Considered 
    ```

#### Proofreading
##### for Documentation Files (*.md, *.html)
- *disable checks inconsistent with our technical writing style*
- Grammar | Rules
    - [_] Articles: article missing before a countable noun
    - [?] Commas after conjunctive/linking adverbs in front of a new sentence
      - *If we could edit the rule, we could maybe just exclude 'currently'.*
    - [_] Loose punctuation mark.
      - conflicts with braces anchoring workflows
      ```
        until done { steps
          } done
          ^
      ```
    - [_] singular noun + plural verb
    - [_] Miscellaneous: hyphenated words
      - fails 'hidden folder at top level of repo'
- Spelling
  - [+]use single dictionary for storing words: application-level
    - *apparently: use hand-editing to populate a custom dictionary,
    presumably from words saved to a built-in wordlist*
    - *suggests we could add cebcar/cebcar.DIC later*
- Possible Typo
  - [_] hell/shell (he'll she'll)
    - conflict: 'shell'
  - [_] missing apostrophe in 'Presidents Day'
    - conflict: 'settings'
- Semantics
  - [_] A new year has begun
    *not all years are this one*

### Plugins
- Plugins
  - Task Management : enable (redundant? configured for Tuxedo 08 Feb 2021 via Tools &gt; Servers, Tasks)
    - *to configure, see [Tools : Tasks](#tools)*

### Version Control
- Version Control System: Git

#### Changelists
- [ + ] Track changed blocks in text files separately
- [ + ] Show dialogue on attempt to edit file from non-active changelist
- [ + ] Highlight files with changelist conflicts
- [ + ] Highlight files from non-active changelist

#### Issue Navigation
*click on IntelliJ issue link to show matching issue in GitHub*
- issue pattern: &lt;ProjectName&gt;-([\d]+)
  - link to GitHub issue: https://github.com/cebcar/DevOps/issues/$1

#### Git
- [ _ ] Enable staging area 
- [ _ ] Commit automatically on cherry-pick
- [ + ] add message suffix "Cherry picked from hash" when pushing to protected branches
- [ + ] Warn if CLRF line separators are about to be committed
- [ + ] Warn when committing in detached HEAD or during release 
- Explicitly check for incoming commits on remotes: Auto
- Update method: Merge
- Clean working tree using: Stash
- [ _ ] Auto update if push from the current branch was rejected
- [ + ] Show Push dialog for Commit and Push
- [ _ ] Show push dialog only when committing to protected branches

- Protected branches: main
- [ + ] Load protection rules from GItHub
- [ _ ] Use credential helper <br/>
- Filter "Update Project" information by paths: All

#### GitHub
- "+" button: try failed because could not replace account 'carolclark' with 'cebcar'
- provide GitHub credentials to connect

### Tools
*/TODO/ extraneous backslashes sometimes appear in Tools content*

#### Tasks
- Changelist name format: ${project}-#${id} ${summary}
- Feature branch name format: &lt;pr&gt;${number}-${summary}
  - [x] Lowercased
  - replace spaces with '-'

##### Tasks: Servers: server GitHub
- add Server GitHub
- connect to server GitHub
- General: provide credentials to connect to GitHub project; test
- commit message: &lt;pr&gt;#${number}-${summary}| 

### Dialogs
#### Print
- Settings
  - show border: off
- Header and Footer
  - add "$DATE$ $TIME$" to beginning of footer
- Advanced
  - margins: .75 bottom to allow for footer; rest .5

## IntelliJ Customization &amp; Automation

## IntelliJ Keymap Customization
| Group | | | Action | Shortcut | Comment |
|---:|:---:|:---:|---:|---|---|
| Editor Actions |
| Main menu | File | | New From Template | roN |
| | View | Appearance | toggle Full Screen | rocF |
| | Analyze | | Inspect Code... | socI |
| | | | Run Inspection by Name... | &lt;none&gt; |
| | VCS | | Workflow Popup | srV |
| | | | Put Local Label... |  scL |
| | | Git | Fetch | rcF |
| | | | Stash/Unstash | scH / scU | 
| | | | Create Pull Request | rocP |
| | | | View Pull Requests | sroP |
| | Help | | Find Action... | rcA |
| Tool Windows | | | resize tool window | sc&lt;arrow&gt; | 
| | | | last tool window | F12 | |
| | | | hide active tool window | sEsc |
| | | | close all tool windows | oF12 |
| Quick Lists | | | VCS Workflow | rV |

# Using IntelliJ Platform IDEs

## IntelliJ Tasks

We use IntelliJ [Tasks](https://www.jetbrains.com/help/idea/managing-tasks-and-context.html)
  to organize work into smaller tasks.

The Task workflow helps keep our workflow anchored.

Features Include:
- automatically offers configurable suggestions for branch and changelist names
- saves and restores context
- context: branch, open files, favorites, breakpoints, tool window status
- stashes (or shelves) existing changes when switching between branches
- available automatic time tracking per Task

### Conventions

- top-level Task normally named for an issue
  - &lt;Proj&gt;#&lt;issueNum&gt; &lt;issueSummary&gt;, 
      using the full project and issue names as proposed by IntelliJ
- branch name abbreviated by hand from IntelliJ-proposed branch name
  - edit to &lt;ph&gt;&lt;issueNum&gt;-&lt;abbreviatedIssueName&gt;,
    where 'ph' is a hardcoded project name
- top-level Task can have multiple branches
  - then branch names replace &lt;issueSummary&gt; with &lt;branchSummary&gt;

## Open Repository as Project

#### create project from repo
- Get Repo from Version Control
  - menu VCS/Git : Clone
    - supply:
      - repository URL
      - directory of the new project
    - press Enter or click Clone<br/><br/>

- Settings: connect to repository
  - File : Manage IDE Settings : Settings Repository
    - select cebcar/ij-settings; overwrite local

#### expand .gitignore

- gitignore.io: add content for macOS and JetBrains; inspect; remove duplicate line .DS_Store

#### connect to GitHub repo
- [Create Personal Access Token](GitHub.md#create-personal-access-token) "JetBrains-GitHub Integration: &lt;projectName&gt;"; copy content to clipboard
- from Preferences : Tools : Tasks : Servers :
  - add new server (`+` or cmd-N); supply GitHub Organization and Repo name; paste in token
  - `Test` to verify connection; Apply
  
#### configure VCS-related tools
- configure [Tools: Tasks](#tasks)
- configure [Tools: Servers: server GitHub][Tools: Tasks](#tasks-servers-server-github)

#### configure Scopes
- configure  [Appearance &amp; Behavior : Scopes](#scopes)

#### commit to Version Control
- Tag and Commit
  - add annotated tag, normally "vYY.0.1" for a new project, with message
- commit; push
  
## Special Documentation Files

### Workflows

Groups of steps in workflows are routinely enclosed in braces to denote sections,
much like groups of steps in code.
```
- ( until | while | ... ) <bold-label> {
  - <steps>
- } <bold-label>
```

This syntax creates issues with the 'Unpaired symbol' Inspection.
To avoid these errors, disable 'Unpaired Symbol' for *.md and *.html files.

<button onclick="window.print()">`Print Button`</button>
