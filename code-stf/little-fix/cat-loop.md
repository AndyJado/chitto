
trying to add a new line in the beginning of each file using some `#.sh`

```bash
for i in *.md; do
  (echo && cat $i) > $i
done
```

cuased a infinate loop!

`#fixed` by

`echo $(cat $i)`


2022年 8月19日 星期五 16时05分38秒 CST

---

