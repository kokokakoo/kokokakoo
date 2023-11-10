
ImiÄ™: [kKajetan]
Nazwisko: [Spychała]
Numer albumu: [ 30539]

# --------------------------------------------------------
# Zadanie.01 
#
#	Wygeneruj wektor liczb losowych x1. 
#   Dziedzina losowania to liczby caÅ‚kowite od 1 do 100.
#   Wektor posiada 100 elementÃ³w. 
#   Elementy wektora nie mogÄ… siÄ™ powtarzaÄ‡.
#	Podaj sumÄ™ wartoÅ›ci elementÃ³w wektora. 
#	WskazÃ³wka: skorzystaj z funkcji 'sample'.
#
# --------------------------------------------------------
# tu wpisz swÃ³j kod: 

?sample()
sum(x1 <- sample(1:100))

# --------------------------------------------------------
# Zadanie.02
#
#	Wygeneruj wektor liczb losowych x2. 
#   Dziedzina losowania to liczby caÅ‚kowite {1,2,3}.
#   Wektor posiada 50 elementÃ³w. 
#   Elementy wektora MOGÄ„ siÄ™ powtarzaÄ‡.
#	Policz liczbÄ™ wystÄ…pieÅ„ kaÅ¼dej liczby w wektorze. 
#	WskazÃ³wka: skorzystaj z funkcji 'table'.
#
# --------------------------------------------------------
# tu wpisz swÃ³j kod: 

?table()
table((x2 <- sample(1:3, 50, replace=T)))


# --------------------------------------------------------
# Zadanie.03
#
#	StwÃ³rz losowe sÅ‚owo oÅ›mioliterowe. 
#   Dziedzina losowania to wektor 'letters'.
#   Elementy wektora nie mogÄ… siÄ™ powtarzaÄ‡.
#	WskazÃ³wka: skorzystaj z funkcji 'paste', aby poÅ‚aczyÄ‡ elementy wektora w sÅ‚owo. 
#
# --------------------------------------------------------
# tu wpisz swÃ³j kod: 

?paste()
x3 <- paste((sample(letters, 8)), collapse='')
x3


# --------------------------------------------------------
# Zadanie.04
#
#	StwÃ³rz wektor x4 kolejnych liczb caÅ‚kowitych od 1 do 10. 
#   KaÅ¼dy z elemntÃ³w wektora podstaw jako promieÅ„ r i wylicz dla nirgo
#	 - obwÃ³d koÅ‚a
#	 - pole koÅ‚a
#	 - powierzchniÄ™ kuli (sferÄ™)
#	 - objÄ™toÅ›Ä‡ kuli
#	Wszystkie wyniki zgromadÅº w macierzy o 10 wierszach i 5 kolumnach. 
#	wyÅ›wietl macierz wynikÃ³w z dokÅ‚adnoÅ›ciÄ… do dwÃ³ch miejsc dziesiÄ™tnych.
#
#      [,1]  [,2]   [,3]    [,4]    [,5]
# [1,]    1  6.28   3.14   12.57    4.19
# [2,]    2 12.57  12.57   50.27   33.51
# [3,]    3 18.85  28.27  113.10  113.10
# [4,]    4 25.13  50.27  201.06  268.08
# [5,]    5 31.42  78.54  314.16  523.60
# [6,]    6 37.70 113.10  452.39  904.78
# [7,]    7 43.98 153.94  615.75 1436.76
# [8,]    8 50.27 201.06  804.25 2144.66
# [9,]    9 56.55 254.47 1017.88 3053.63
# [10,]   10 62.83 314.16 1256.64 4188.79
#
# --------------------------------------------------------
# tu wpisz swÃ³j kod: 

?matrix()
x4 <- 1:10
mtx <- matrix(nrow=10,ncol=5)
for (row in 1:10) {
  r <- x4[row]
  mtx[row, 1] <- r
  mtx[row, 2] <- 2 *pi * r
  mtx[row, 3] <- pi * r^2
  mtx[row, 4] <- 4 *pi * r^2
  mtx[row, 5] <- mtx[row, 4] * (1/3) * r
}
round(mtx,2)


# --------------------------------------------------------
# Zadanie.05
# 
# Policz ile jest wspÃ³lnych wielokrotnoÅ›ci liczb 2 i 3
# w zbiorze licz caÅ‚kowitych od 1 do 1500.  
# WskazÃ³wka: skorzystaj z funkcji 'intersect'.
# 
# --------------------------------------------------------
# tu wpisz swÃ³j kod: 

?intersect()
a <- (1:1500)[(1:1500) %% 2 == 0]
b <- (1:1500)[(1:1500) %% 3 == 0]
x5 <- intersect(a, b)
length(x5)

