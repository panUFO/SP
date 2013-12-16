### Laboratorium 2

1\.Wyświetl na ekran 2 pierwsze wiersze pliku program.c. (head)
```sh
head -n 2 program.c
```

2\. Wyświetl na ekran 4 ostatnie wiersze pliku program.c. (head, tail)
```sh
tail -n 4 program.c
```

3\. W pliku program.c znajdź wszystkie wiersze z wystąpieniem słowa „main”. (grep)
```sh
grep main program.c
```

4\. Plikowi program.c nadaj następujące uprawnienia: właściciel – czytanie, pisanie, 
grupa – czytanie, pozostali użytkownicy: brak uprawnień. (chmod)
```sh
chmod 640 program.c
```
5\. Będąc w katalogu temp przenieś katalog wazne-sprawy do katalogu praca.
```sh
cd temp
mv dom/wazne-sprawy praca
```

6\. Zarchiwizuj cały katalog temp. (zip i tar)
```sh
tar -cf temp.tar temp
```

7\. Usuń katalog temp.
```sh
rm -r temp
```

8\. Odtwórz z archiwum katalog temp. (unzip i tar)
```sh
tar -xf temp.tar
```

9\. Posprzątaj na swoim koncie.
```sh
rm temp.tar
mv temp/praca/wazne-sprawy/ temp/dom/
```
10\. Wyswietl okreslone linijki liczac od gory
```sh
head -8 sprawdzian.c | tail -2 #head-liczenie od której linijki, tail ilość linijek od tyłu
```

11\. Wyswietl linijki liczac od dolu (5,6)
```sh
tail -7 sprawdzian.c | head -2 
```

12\.Wyświetl linijki ze środka pliku program.c (licząc od dołu) przy użyciu komendy tac. Przykład linijki 5 i 6.
```sh
tac sprawdzian.c | head -8 | tail -2 | tac
```

13\.wyszukiwanie wyrazów konczacych sie "..."
```sh
grep 'main\>' sprawdzian.c
```
wyszukiwarka google 10 challenges
https://docs.google.com/file/d/0BxlpTzK9iG-2a3VvZi1nZWl0eEE/edit?usp=sharing&hl=pl&forcehl=1&pli=1


