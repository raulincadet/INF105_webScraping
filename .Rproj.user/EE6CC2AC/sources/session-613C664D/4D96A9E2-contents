###########################################
######### WEB SCRAPING AVEC RVEST #########
library(rvest)
library(dplyr)


######### Scraping JobPaw  ##############
url_jobpaw="https://www.jobpaw.com/pont/professionnels.php?id=4"   # offres d'emplois actuels
dataread=rvest::read_html(url_jobpaw)#,encoding = 'UTF-8')         # lecture de la page web
tableaux=rvest::html_table(dataread)          # retrouver les tableaux de la page
length(tableaux)                              # nombre de tableaux trouvés
tableaux[[1]]
tableaux[[2]]
jobs=tableaux[[2]]                            # C'est le tableau contenant les offres d'emplois
class(jobs)
jobs



############## Scraping Taux de change journalier BRH ################
url_tauxJr="https://www.brh.ht/taux-du-jour/"
dataread_brh=rvest::read_html(url_tauxJr)
tableaux_brh=rvest::html_table(dataread_brh)
length(tableaux_brh)
tableaux_brh
class(tableaux_brh)
length(tableaux_brh)
data.frame(tableaux_brh)
df_brh=data.frame(tableaux_brh)
str(df_brh)
View(df_brh)


##### Scrap Le Nouvelliste #######################
url_nv="https://lenouvelliste.com/"         # lien url de la page qui nous interesse
dataread_nv=rvest::read_html(url_nv)        # lecture de la page web
tableaux_nv=rvest::html_table(dataread_nv)  # retrouver les tableaux qui sont dans la page, s'il y en a
length(tableaux_nv)                         # nombre de tableaux

rvest::html_nodes(dataread_nv,'h2')  # Liste des elements h2
rvest::html_nodes(dataread_nv,'h2') %>%html_children()  # liste des elements h2 disposant d'une autre balise
rvest::html_nodes(dataread_nv,'h2') %>%html_text()
rvest::html_nodes(dataread_nv,'h2') %>%html_children()%>%html_text() # Titres des articles
rvest::html_nodes(dataread_nv,'h2') %>%html_children()%>%html_attr('href') # Les donnees de l'attribut href


read_art1=rvest::read_html(url_art1)
rvest::html_nodes(read_art1,'p')%>%html_text()
rvest::html_nodes(read_art1,'p')%>%html_children()
rvest::html_nodes(read_art1,'small')%>%html_text()
(rvest::html_nodes(read_art1,'small')%>%html_text())
