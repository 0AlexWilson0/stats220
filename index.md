# **Meme**
![my_meme](https://user-images.githubusercontent.com/101619086/158372873-0fbe9937-a68d-4d32-9018-1fb43480ecb5.png)


## Meme Code
#Meme Text (first column of squares)
first_text <-image_blank(width = 500,
                      height = 500,
                      color = "#FFFFFF") %>%
  image_annotate(text = "SPEND A FEW SECONDS\nMAKING A MEME USING PAINT",
                 color = "#000000",
                 size = 40,
                 font = "Impact",
                 gravity = "center")

second_text <-image_blank(width = 500,
                        height = 500,
                        color = "#FFFFFF") %>%
  image_annotate(text = "SPEND A MINUTE MAKING\nA MEME USING POWERPOINT",
                 color = "#000000",
                 size = 40,
                 font = "Impact",
                 gravity = "center")

third_text <-image_blank(width = 500,
                      height = 500,
                      color = "#FFFFFF") %>%
  image_annotate(text = "SPEND A FEW MINUTES MAKING\nA MEME USING PHOTOSHOP",
                 color = "#000000",
                 size = 40,
                 font = "Impact",
                 gravity = "center")

fourth_text <-image_blank(width = 500,
                        height = 500,
                        color = "#FFFFFF") %>%
  image_annotate(text = "SPEND HOURS MAKING\nA MEME USING CODE",
                 color = "#000000",
                 size = 40,
                 font = "Impact",
                 gravity = "center")


#Meme images (second column of squares)
first_brain <- image_read("https://mat3e.github.io/brains/img/0.jpg") %>%
  image_scale(500)
  
second_brain <- image_read("https://mat3e.github.io/brains/img/1.jpg") %>%
  image_scale(500)

third_brain <- image_read("https://mat3e.github.io/brains/img/2.jpg") %>%
  image_scale(500)

fourth_brain <- image_read("https://mat3e.github.io/brains/img/3.jpg") %>%
  image_scale(500)

#Combining it all together
first_vector <-c(first_text, first_brain)
first_row <-image_append(first_vector)

second_vector <-c(second_text, second_brain)
second_row <-image_append(second_vector)

third_vector <-c(third_text, third_brain)
third_row <-image_append(third_vector)

fourth_vector <-c(fourth_text, fourth_brain)
fourth_row <-image_append(fourth_vector)

c(first_row, second_row, third_row, fourth_row) %>%
  image_append(stack = TRUE)
 
 
# **Meme Information**  
I was initially blank about what the meme should say, I just knew I wanted it to be the expanding brain meme.
My motovation for what the meme would be about was the fact it took me hours to figure out the code for such a simple meme. (little errors I couldnt see increased the time)
While the meme template was not changed, the point of the expanding brain meme is that the more the brain expands, the more outlandish the concepts become, 
and generally youre not supposed to do those things. And as I made the meme using code, as the last panal said, it was slightly unique to the original format.

