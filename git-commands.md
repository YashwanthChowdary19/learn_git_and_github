# Git Commands Reference Guide

## Basic Setup
```bash
# Git కాన్ఫిగరేషన్
git config --global user.name "మీ పేరు"
git config --global user.email "మీ ఇమెయిల్"

# Git వెర్షన్ చెక్ చేయడం
git --version
```

## Starting a Project
```bash
# కొత్త Git రిపోజిటరీని ఇనిషియలైజ్ చేయడం
git init

# రిపోజిటరీ స్టేటస్ చెక్ చేయడం
git status
```

## Working with Files
```bash
# ఫైల్‌లను స్టేజింగ్ చేయడం
git add filename.txt    # ఒక ఫైల్‌ని స్టేజింగ్ చేయడం
git add .              # అన్ని ఫైల్‌లను స్టేజింగ్ చేయడం

# మార్పులను కమిట్ చేయడం
git commit -m "మీ కమిట్ మెసేజ్"

# ఫైల్‌లను అన్‌స్టేజింగ్ చేయడం
git reset filename.txt
```

## Remote Repository Operations
```bash
# GitHub రిపోజిటరీని కనెక్ట్ చేయడం
git remote add origin https://github.com/username/repository.git

# రిమోట్ రిపోజిటరీలను చూడటం
git remote -v

# మార్పులను పుష్ చేయడం
git push -u origin main

# ఇతరుల మార్పులను పుల్ చేయడం
git pull
```

## Branching
```bash
# బ్రాంచ్‌లను చూడటం
git branch

# కొత్త బ్రాంచ్‌ని క్రియేట్ చేయడం
git branch branch-name

# బ్రాంచ్‌కి స్విచ్ చేయడం
git checkout branch-name

# కొత్త బ్రాంచ్‌ని క్రియేట్ చేసి స్విచ్ చేయడం
git checkout -b branch-name

# బ్రాంచ్‌లను మర్జ్ చేయడం
git merge branch-name
```

## Viewing Changes
```bash
# మార్పులను చూడటం
git diff

# కమిట్ హిస్టరీని చూడటం
git log

# కమిట్ హిస్టరీని కంపాక్ట్ ఫార్మాట్‌లో చూడటం
git log --oneline
```

## Undoing Changes
```bash
# కమిట్ చేయని మార్పులను అండూచేయడం
git checkout -- filename.txt

# కమిట్ చేసిన మార్పులను అండూచేయడం
git revert commit-hash
```

## Advanced Commands
```bash
# స్టేజింగ్ ఏరియాని క్లియర్ చేయడం
git reset

# కాత్‌ఫీల్‌లను స్టేజింగ్ చేయడం
git add -p

# స్టాషింగ్ మార్పులు
git stash
git stash pop

# సబ్‌మాడ్యూల్‌లను జోడించడం
git submodule add repository-url
```

## .gitignore
```bash
# .gitignore ఫైల్‌ని క్రియేట్ చేయడం
touch .gitignore

# ఫైల్‌లను ఇగ్నోర్ చేయడం
echo "filename.txt" >> .gitignore
echo "*.log" >> .gitignore
```

## GitHub Specific
```bash
# GitHub క్లోనింగ్
git clone https://github.com/username/repository.git

# ఫోర్క్ చేసిన రిపోజిటరీని కనెక్ట్ చేయడం
git remote add upstream https://github.com/original-owner/repository.git

# అప్‌స్ట్రీమ్ మార్పులను పుల్ చేయడం
git pull upstream main
```

## Tips
- ప్రతి కమిట్‌కి స్పష్టమైన మెసేజ్ ఇవ్వండి
- రెగ్యులర్‌గా `git pull` చేయండి
- ప్రతి ఫీచర్‌కి కొత్త బ్రాంచ్‌ని క్రియేట్ చేయండి
- సెన్సిటివ్ ఫైల్‌లను `.gitignore` లో ఇగ్నోర్ చేయండి 