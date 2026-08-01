




2. Git inicializācija

```bash
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> git init
Initialized empty Git repository in C:/Users/robo/Documents/BUTS/Praktiskie_darbi/05 Programmas koda rakstīšana (Kodēšana)/PB1_PD16 Versiju kontrole/PB1_PD16_Simkuns_Arturs/.git/
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        README.md
        projekts.py

nothing added to commit but untracked files present (use "git add" to track)
```

mapes struktūra pēc komandas `git init` izpildes:
```powershell
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> Show-Tree .
PB1_PD16_Simkuns_Arturs/
├── .git/
│   ├── hooks/
│   │   ├── applypatch-msg.sample
│   │   ├── commit-msg.sample
│   │   ├── fsmonitor-watchman.sample
│   │   ├── post-update.sample
│   │   ├── pre-applypatch.sample
│   │   ├── pre-commit.sample
│   │   ├── pre-merge-commit.sample
│   │   ├── prepare-commit-msg.sample
│   │   ├── pre-push.sample
│   │   ├── pre-rebase.sample
│   │   ├── pre-receive.sample
│   │   ├── push-to-checkout.sample
│   │   ├── sendemail-validate.sample
│   │   └── update.sample
│   ├── info/
│   │   └── exclude
│   ├── objects/
│   │   ├── info/
│   │   └── pack/
│   ├── refs/
│   │   ├── heads/
│   │   └── tags/
│   ├── config
│   ├── description
│   └── HEAD
├── .gitignore
├── projekts.py
└── README.md
```

2.3 Git identitātes iestatīšana

```powershell
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> git config --global user.name "Artūrs Šimkūns"
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> git config --global user.email "arturs.simkuns@gmail.com"
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=schannel
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.name=Artūrs Šimkūns
user.email=arturs.simkuns@gmail.com
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
```

Lai redzētu, no kura faila nāk katrs iestatījums, izmanto:

```powershell
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> git config --list --show-origin
file:C:/Program Files/Git/etc/gitconfig diff.astextplain.textconv=astextplain
file:C:/Program Files/Git/etc/gitconfig filter.lfs.clean=git-lfs clean -- %f
file:C:/Program Files/Git/etc/gitconfig filter.lfs.smudge=git-lfs smudge -- %f
file:C:/Program Files/Git/etc/gitconfig filter.lfs.process=git-lfs filter-process
file:C:/Program Files/Git/etc/gitconfig filter.lfs.required=true
file:C:/Program Files/Git/etc/gitconfig http.sslbackend=schannel
file:C:/Program Files/Git/etc/gitconfig core.autocrlf=true
file:C:/Program Files/Git/etc/gitconfig core.fscache=true
file:C:/Program Files/Git/etc/gitconfig core.symlinks=false
file:C:/Program Files/Git/etc/gitconfig pull.rebase=false
file:C:/Program Files/Git/etc/gitconfig credential.helper=manager
file:C:/Program Files/Git/etc/gitconfig credential.https://dev.azure.com.usehttppath=true
file:C:/Program Files/Git/etc/gitconfig init.defaultbranch=master
file:C:/Users/robo/.gitconfig   user.name=Artūrs Šimkūns
file:C:/Users/robo/.gitconfig   user.email=arturs.simkuns@gmail.com
file:.git/config        core.repositoryformatversion=0
file:.git/config        core.filemode=false
file:.git/config        core.bare=false
file:.git/config        core.logallrefupdates=true
file:.git/config        core.symlinks=false
file:.git/config        core.ignorecase=true
```


3. Pirmais commit

```powershell
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> git add .
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> git commit -m "Pirmais commit: pievienots projekts.py"
[master (root-commit) e46f8b8] Pirmais commit: pievienots projekts.py
 3 files changed, 120 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 README.md
 create mode 100644 projekts.py
```

4. Darbs ar zaru (branch)

```powershell
PS C:\Users\robo\Documents\BUTS\Praktiskie_darbi\05 Programmas koda rakstīšana (Kodēšana)\PB1_PD16 Versiju kontrole\PB1_PD16_Simkuns_Arturs> git checkout -b feature-uzlabojums
Switched to a new branch 'feature-uzlabojums'
```

5. Merge





