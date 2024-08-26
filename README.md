# Flames-gam
def flames_game(name1, name2):
	# remove common characters
	for i in name1:
		if i in name2:
			name1 = name1.replace(i, '')
			name2 = name2.replace(i, '')

	# count remaining characters
	count = len(name1) + len(name2)

	# FLAMES acronym
	flames = ['F', 'L', 'A', 'M', 'E', 'S']

	# calculate relationship status
	index = (count % 6) - 1
	if index >= 0:
		return 'Relationship status: ' + flames[index]
	else:
		return 'Relationship status: S'
# input names
name1 = input('Enter first name: ').upper()
name2 = input('Enter second name: ').upper()

print(flames_game(name1, name2))


