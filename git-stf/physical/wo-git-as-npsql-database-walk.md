> as a database, everything happens in .git

```bash
REPO='la-db-repo'

mkdir $REPO && cd $REPO && git init .
#====BLOB====#
echo '{"id": 1, "name": "me"}' | git hash-object -w --stdin
#> a:SHA = 3a670fbe8943ce01aed77aa236e945460d915e34

git cat-file -p 3a670fbe89 #short <a>

#====TREE====#
git update-index --add --cacheinfo 100644 3a670fbe8943ce01aed77aa236e945460d915e34 me.json #verbose <a>, but 10063 waht?

git write-tree
#> b:SHA = 2b8665336db037b6e641eb7b9f64419166a0b5ea

git update-index --add --cacheinfo 111111 3a670fbe8943ce01aed77aa236e945460d915e34 me.json #so what's behind cacheinfo?

#====TREE====#
tree1=$(git write-tree)
#> c:SHA = a9fba107554e15e675ebffe18abd0d9de29f0734

# FIXME:SHA won't be the same?? because commit time??
echo "commit 1st version" | git commit-tree $tree1 #<SHA:b>
#> d:SHA = 7485639aa83746611237ce0b603974cc71eeb991
#? nothing commited

echo "Commit 2nd version" | git commit-tree a9fba1075 -p 7485639aa
#> e:SHA = 5bbf3cc340376b166438c199cb3c53e8285eb40e

git log --stat 5bbf3cc3 #<SHA: e>

git show 5bbf3cc340:me.json

#====REFERENCES====#
#ERROR:work dir error when manually delete main file in .git/
echo 7485639aa83746611237ce0b603974cc71eeb991 > .git/refs/heads/main
#> gitui won't work
git update-ref 
```