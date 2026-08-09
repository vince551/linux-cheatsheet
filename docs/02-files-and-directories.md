# 02 · Files & Directories

## Navigation
```bash
pwd
ls -la
cd ~
cd ..
cd -
```

## Create
```bash
mkdir project
mkdir -p project/{docs,scripts,backup}
touch notes.txt
```

## Copy / move / remove
```bash
cp notes.txt backup.txt
cp -r project project-copy
mv notes.txt docs/
rm backup.txt
rm -r project-copy
```

## Search
```bash
find . -name '*.txt'
find . -type d -name 'backup'
grep -Rni 'keyword' .
```

> ⚠️ Check paths before using recursive `rm`.
