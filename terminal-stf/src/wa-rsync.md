rsync -azP --delete --exclude={'target/','build/'} Zf/rust root@49.4.3.152:~

a: archive
z: zip
P: partial && progress
.--append
/: **means something!**

