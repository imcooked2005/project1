for i in {1..10}
do
    gh repo create "Project-$i" --public --description "Repository $i" --confirm
    echo "# Project-$i" > README.md
    git init
    git add README.md
    git commit -m "Initial commit"
    git branch -M main
    git remote add origin "https://github.com/YOUR-USERNAME/Project-$i.git"
    git push -u origin main
done
