import play
photo = play.new_image(image = "1.jpg", x = 0, y = 0, size = 80)
text = play.new_text(words = "GIVE ME MY FOOD!!!", x = 0, y = -80, font_size = 20, color = "black")

@play.when_program_starts
def start():
  photo.hide()

@play.repeat_forever
def do ():
  if play.key_is_pressed("a"):
    text.words = "I want to eat"
    photo.image = "2.jpg"
    photo.show()

  if play.key_is_pressed("s"):
    text.words = "come I will give you a hug!"
    photo.image = "3.png"
    photo.show()

  if play.key_is_pressed("d"):
    text.words = "relax"
    photo.image = "4.jpg"
    photo.show()

  if play.key_is_pressed("w"):
    text.words = "YUHU!!!"
    photo.image = "5.png"
    photo.show()

play.start_program()
