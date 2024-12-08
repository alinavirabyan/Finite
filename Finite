text = "abcabc"
pattern = "abc"

m = len(pattern)
n = len(text)

transition_table = []
for i in range(256):
    row = []
    for j in range(m + 1):
        row.append(0)
    transition_table.append(row)

for state in range(m + 1):
    for char in range(256):
        if state < m and chr(char) == pattern[state]:
            transition_table[char][state] = state + 1
        else:
            transition_table[char][state] = 0

state = 0
for i in range(n):
    char = ord(text[i])
    state = transition_table[char][state]

    if state == m:
        print(f"Pattern found at index {i - m + 1}")
        state = transition_table[char][state]

else:
    print("Pattern not found")
