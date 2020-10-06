# tarea1metodosCiPol

library(tidyverse)
library(polAr)
data2 <- get_election_data("arg", "presi", "gral", 2003)
filter(data2, codprov==20) %>%
select(listas, votos) %>%
arrange(desc(votos)) %>%
mutate(dif_con_primero = votos - 84167)
