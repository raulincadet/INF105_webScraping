library(rvest)
library(dplyr)


# Scrap Jobpaw
url_jobpaw="https://www.jobpaw.com/pont/professionnels.php?id=4"
dataread=rvest::read_html(url_jobpaw)
dataread

tableaux=rvest::html_table(dataread)
length(tableaux)

tableaux[[1]]
tableaux[[2]]
jobs=tableaux[[2]]


# Scrap Taux de change sur le site de la BRH
url_taux="https://www.brh.ht/taux-du-jour/"
dataread_brh=rvest::read_html(url_taux)
dataread_brh

tableaux_brh=rvest::html_table(dataread_brh)
length(tableaux_brh)
tableaux_brh


### Scrap Le Nouvelliste
url_nv="https://lenouvelliste.com"
dataread_nv=rvest::read_html(url_nv)
dataread_nv

tableaux_nv=rvest::html_table(dataread_nv)
length(tableaux_nv)

rvest::html_nodes(dataread_nv,'h2')
rvest::html_nodes(dataread_nv,'h2')%>%html_children()

rvest::html_nodes(dataread_nv,'h2')%>%html_children()%>%html_text()


list_url_articles=rvest::html_nodes(dataread_nv,'h2')%>%html_children()%>%
  html_attr('href')
list_url_articles

# Explorons le premier article

url1=list_url_articles[[1]]
url1
read_art1=rvest::read_html(url1)
read_art1

rvest::html_nodes(read_art1,'h2')  # le titre de l'article
rvest::html_nodes(read_art1,'p')
rvest::html_nodes(read_art1,'p')%>%html_children()
rvest::html_nodes(read_art1,'p')%>%html_text()
