```text
1:
cmd:
ls flag_dir
sol:
FLAG1_31337

2:
cmd:
cat .hidden_flag_dir/abc/123/.nothingtoseehere/data/flag
sol:
FLAG2_42448

3:
cmd:
cat /tmp/.flag3 |strings |grep FLA
sol:
FLAG3_55352

4:
cmd:
cat /tmp/.flag4 |base64 -d
sol:
FLAG4_63992

6:
cmd:
cat /etc/group|grep FLA
sol:
FLAG6_41442

7:
cmd:
cd ~www/;cat file
sol:
FLAG7_55241

9:
cmd:
curl localhost:8080|grep FLA
sol:
FLAG9_99382

10:
cmd:
curl --dump-header /tmp/x.txt localhost:8080
cat /tmp/x.txt |grep flag=|sed -e 's#^.*flag="##'|sed -e 's#".*##'|base64 -d
sol:
FLAG10_45776

11:
cmd:
curl localhost:31337
nc localhost 31337
ps -ef|grep FLAG
sol:
FLAG_11314

12:
cmd:
unzip -o oddfile.zip ;cat oddfile
sol:
FLAG12_552412

13:
cmd:
nmap localhost
sol:
Elite

14:
cmd:
tcpdump -r flag.dmp|grep FLA
tcpdump -Anr flag.dmp|grep FLA
cat flag.dmp|strings |grep FLA
sol:
FLAG14_13370

15:
cmd:
cat ce.txt
sol:
# https://raw.org/tool/caesar-cipher/
20

16:
cmd:
cat pic.png |strings
sol:
ctfa{Stegosaurus}

17:
# qrencode -t ANSIUTF8 FLAG_17_32767 > randomx.dat
cmd:
cat randomx.dat
sol:
FLAG_17_32767

18:
# qrencode -t PNG FLAG_18_92758 -o fl.png
cmd:
i2a/ascii-image-converter --braille  fl.png
sol:
FLAG_18_92758



# result:
cmd:
echo 'FLAG1_31337FLAG2_42448FLAG3_55352FLAG4_63992FLAG6_41442FLAG7_55241FLAG9_99382FLAG10_45776FLAG_11314FLAG12_552412EliteFLAG14_1337020ctfa{Stegosaurus}FLAG_17_32767FLAG_18_92758'|sha256sum
sol:
2e8a3cc2a0197775f8df1feb84d799487743e86b594e620fd73a2cc7308035f9



# EXTRA 01
cmd:
ls -alR
ls -al */FLA*
find .|grep FLAG
ls -ali ; cd $(find . -inum <inodenum>) ; ls -al
sol:
FLAG_EX01_60572

# EXTRA 02
cmd:
cd '\.'
sol:
FLAG_EX02_12538

# EXTRA 03
cmd:
for a in {a..z}; do
  for b in {a..z}; do
    for c in {a..z}; do
      /secret/$c$b$a 2>/dev/null
    done
  done
done
sol:
FLAG_EX03_007JB

```

