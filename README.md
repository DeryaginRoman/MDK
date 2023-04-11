# MDK
class Alphabet:
  def __init__(self, lang, letters):
    self.lang = lang
    self.letters = letters
  
  def print_(self):
    if self.lang == 'eng' or self.lang == 'ENG' or self.lang == 'Eng':
      self.letters = 'abcdefghijklmnopqrstuvwxyz'
    elif self.lang == 'ru' or self.lang == 'RU' or self.lang == 'Ru':
      self.letters = 'абвгдежзийклмнопрстуфхцчшщъыьэюя'
    return self.letters

  def letters_num(self):
    return len(self.letters)

class EngAlphabet(Alphabet):
  def __init__(self, lang, letters):
    super().__init__(self, letters)
    self.__letters_num = len(self.letters)
  def is_en_letter(self, letter):
    if letter in 'abcdeafghijklmnopqrstuvwxyz':
      return 'Введённая вами буква относится к английскому алфавиту'
    elif letter in 'абвгдежзийклмнопрстуфхцчшщъыьэюя':
      return 'Введённая вами буква относится к русскому алфавиту'
    else:
      return 'Ошибка ввода'
  def example(self, letter):
    if letter in 'abcdefghijklmnopqrstuvwxyz':
      return 'Пример текстка: "I see a beautiful girl next to him."'
    elif letter in 'абвгдежзийклмнопрстуфхцчшщъыьэюя':
      return 'Пример текстка: "Я вижу красивую девушку рядом с ним."'


new=EngAlphabet(str(input()), str(input()))
print(new.print_())
print(new.letters_num())
print(new.is_en_letter(input()))
print(new.example(input()))
