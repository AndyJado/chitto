I had trouble walking through [git-internals](https://git-scm.com/book/en/v2/Git-Internals-Plumbing-and-Porcelain)

and I found [git-from-bottom-up](https://jwiegley.github.io/git-from-the-bottom-up/1-Repository/1-directory-content-tracking.html)

from a HN post

---

## commands

```bash
# wa-blob
$ mkdir sample; cd sample

$ echo 'Hello, world!' > greeting

$ git hash-object greeting #return <a-hash>

$ git init

$ git add greeting

$ git commit -m "Added my greeting"

$ git cat-file -t af5626b #first 7 digit returned from <a-hash>

$ git cat-file blob af5626b #show content of blob

# wa-blob-tree
$ git ls-tree HEAD

$ git rev-parse HEAD

$ git cat-file -t HEAD

$ git cat-file commit HEAD

$ git ls-tree 0563f77

$ find .git/objects -type f | sort

$ git cat-file -t 588483b99a46342501d99e3f10630cfc1219ea32

$ git cat-file -t 0563f77d884e4f79ce95117e2d686d7d6e282887

$ git cat-file -t af5626b4a114abcb82d63db7c8082c3c4756e51b

```
