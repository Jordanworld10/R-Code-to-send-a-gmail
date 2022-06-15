# R-Code-to-send-a-gmail

library(emayili)
library(dplyr)

email <- envelope() %>%
  from("tomas.trevino23@gmail.com") %>%
  to("tomas.trevino23@gmail.com") %>%
  subject("This is a plain text message!") %>% 
  text("Hello!")

smtp <- server(host = "smtp.gmail.com",
               port = 465,
               username = "tomas.trevino23",
               password = "aazpfyxaksauumqo")

smtp(email, verbose = TRUE) # this script works for gmail
