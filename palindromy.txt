def palindrome(word):
  for i in range(len(word)//2):
      if word[i] != word[len(word) - i - 1]:
          return False
  return True


def check_palindromes(words):
  palindrome_words = []
  for word in words:
      if palindrome(word):
          palindrome_words.append(word)
  return palindrome_words

words = [
  "kajak",
  "stop",
  "potop",
  "krew",
  "sedes",
  "atak kata",
  "kotwica"
]

palindrome_words = check_palindromes(words)
print("Palindromes in the collection:")
print(palindrome_words)