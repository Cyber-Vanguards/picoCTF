
# keygenme.py

- `#ReverseEngineering`
- `https://mercury.picoctf.net/static/9055e7d35f5f4646338a1734aea0dda5/keygenme-trial.py`
- look at the source code
- create a `solve.py` where you copy the global variables and grab just the hash string slices

```
# --- solve.py
# GLOBALS --v
arcane_loop_trial = True
jump_into_full = False
full_version_code = ""

username_trial = "FRASER"
bUsername_trial = b"FRASER"

key_part_static1_trial = "picoCTF{1n_7h3_|<3y_of_"
key_part_dynamic1_trial = ""

hash = hashlib.sha256(bUsername_trial).hexdigest()

key_part_dynamic1_trial += hash[4]
key_part_dynamic1_trial += hash[5]
key_part_dynamic1_trial += hash[3]
key_part_dynamic1_trial += hash[6]
key_part_dynamic1_trial += hash[2]
key_part_dynamic1_trial += hash[7]
key_part_dynamic1_trial += hash[1]
key_part_dynamic1_trial += hash[8]

key_part_static2_trial = "}"
key_full_template_trial = key_part_static1_trial + key_part_dynamic1_trial + key_part_static2_trial

print(key_full_template_trial)
```

- run `keygenme-trial.py` and paste in the flag and if another python file was generated then the flag key is valid
- `picoCTF{1n_7h3_|<3y_of_ac73dc29}`