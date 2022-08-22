md = r'../../Prince-of-sea/ons_convlist.md'
csv = r'../../Prince-of-sea/_ons_convlist.csv'
txt1 = r'../../Prince-of-sea/_ons_convlist.txt'
txt2 = r'../../Prince-of-sea/_ons_convlist2.txt'

s = r''

with open(txt1, encoding="utf_8") as f:
	s += f.read()

with open(csv, encoding="utf_8") as f:
	for i, line in enumerate(f):
		if not (i == 2):
			s += line.replace(r',', r' | ')

with open(txt2, encoding="utf_8") as f:
	s += f.read()

with open(md, 'w', encoding="utf_8") as f:
	f.write(s)
