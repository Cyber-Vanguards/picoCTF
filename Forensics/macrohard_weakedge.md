
# Macro Hard WeakEdge

- `#Forensics`
- I've hidden a flag in this file, can you find it? 
- `https://mercury.picoctf.net/static/2e739f9e0dc9f4c1556ea6b033c3ec8e/Forensics%20is%20fun.pptm`
- `mv Forensics\ is\ fun.pptm Forensics_is_fun.pptm`
- `file Forensics_is_fun.pptm` Microsoft PowerPoint 2007+
- install oletools for dealing with macros `https://github.com/decalage2/oletools`
- `olevba -h`
- `olevba [options] [filename]`
- `olevba --decode -d Forensics_is_fun.pptm` no flag
- try to unzip `.pptm` file , many files, `*.xml.rels` is metadata file stored inside Open XML documents
- move the related folders into a new directory `Windows/`
- `cd Windows/ppt/slideMasters/` and see `hidden` file (ASCII type)
- base64 characters are spaced out, use the Linux tool `sed`
- `cat hidden | sed 's/ //g' | base64 -d ` 
- `flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}`