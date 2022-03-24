def reverse_this(char, is_code=False):
    special_character = [',', ':', '!', '?', '*', '&', '%', '$', '#', '@', '(', ')', '"', '-', '.', ' ', "'", '\n']
    code = ' '
    d = {}
    for c in (65, 97):
        for i in range(26):
            d[chr(i + c)] = chr((i + 13) % 26 + c)
    if not is_code:
        for i in char:
            if i in special_character:
                code += str(i)
            else:
                code += f'{d[i]}'
        return code.strip()  # Strip REMOVE leading whitespace
    if is_code == True:
        char_split = char.split()  # Split making a long string into indexes of string in a LIST.
        # Ex: "HELLO" after
        # SPLIT would be ['H' 'E' 'L' 'L' 'O'].
        for i in range(len(char_split)):  # Use range(len()) to avoid LIST is not STRING TypeError.
            for key, value in d.items():
                if char_split[i] == value:
                    code += key
        return ''.join(code).strip()  # STRIP concatenate the separate index into a long string OPPOSITE TO SPLIT


#     Ex: ['H' 'E' 'L' 'L' 'O']
#     After join method would become "HELLO"


with open("ZenOfPython") as f:
    char = f.read()


print(reverse_this(char, is_code=False))
