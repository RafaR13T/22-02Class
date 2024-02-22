# 22-02Class
#Comandos
#instalar una libreria
install.packages("BiocManager")
#instalar una libreria de Bioc
BiocManager::install("sangeranalyseR")
#Cargar una libreria
library(sangeranalyseR)
#Cambiar el working directory
setwd("C:/Users/Alumno1/Documents/Secuencias ATPasa/Placa_TORATP")

#alinear
my_aligned_contigs <- SangerAlignment(ABIF_Directory      = "C:/Users/Alumno1/Documents/Secuencias ATPasa/Placa_TORATP",
                                     processMethod       = "REGEX",
                                     REGEX_SuffixForward = "_*.ab1",
                                     REGEX_SuffixReverse = "_*.ab1")
#correr shiny
runApp(my_aligned_contigs)
#instalar 
install.packages("shinydashboard")

#22/02/24
#Concatenar archivos .fasta
Get-content *.fasta | set-content rowfinal.fasta
