---
{"dg-publish":true,"permalink":"/ml-dataset/"}
---

# Hindi NL dataset learning

```bash
jq -r '."english word", ."native word"' hin_train.json > large-file.txt
awk '{getline line2;print $0,line2}' large-file.txt > final-large-train.txt
varnamcli -s hi -learn-from-file learn_hindi.txt
varnamcli -s hi -train-from-file new.txt
```
