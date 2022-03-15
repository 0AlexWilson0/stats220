# stats220
library(magick)

#Meme images (second column of squares)
first_brain <- image_read("https://mat3e.github.io/brains/img/0.jpg") %>%
image_scale(500)


second_brain <- image_read("https://mat3e.github.io/brains/img/1.jpg") %>%
  image_scale(500)

third_brain <- image_read("https://mat3e.github.io/brains/img/2.jpg") %>%
  image_scale(500)

fourth_brain <- image_read("https://mat3e.github.io/brains/img/3.jpg") %>%
  image_scale(500)


#Meme Text (first column of squares)
first_text <- image_blank(width = 500,
                          height = 500,
                          color = "#FFFFFF") %>%
  image_annotate(text = "**Statistics**",
                 color = "#000000",
                 size = 80,
                 font = "Impact",
                 gravity = "center")

second_text <- image_blank(width = 500,
                           height = 500,
                           color = "#FFFFFF") %>%
  image_annotate(text = "**Statistics**",
                 color = "#000000",
                 size = 80,
                 font = "Impact",
                 gravity = "center")

third_text <- image_blank(width = 500,
                          height = 500,
                          color = "#FFFFFF") %>%
  image_annotate(text = "**Statistics**",
                 color = "#000000",
                 size = 80,
                 font = "Impact",
                 gravity = "center")

fourth_text <- image_blank(width = 500,
                           height = 500,
                           color = "#FFFFFF") %>%
  image_annotate(text = "**Statistics**",
                 color = "#000000",
                 size = 80,
                 font = "Impact",
                 gravity = "center")


#Combining it all together
first_vector <- c(first_text, first_brain)
first_row <- image_append(first_vector)

second_vector <- c(second_text, second_brain)
second_row <- image_append(second_vector)

third_vector <- c(third_text, third_brain)
third_row <- image_append(third_vector)

fourth_vector <- c(fourth_text, fourth_brain)
fourth_row <- image_append(fourth_vector)

c(frist_row, second_row, third_row, fourth_row) %>%
  image_append(stack = TRUE) %>%
  image_scale(500)
