### Laboratorium 1
http://wbzyl.inf.ug.edu.pl/sp/labs01
Sublime Text 2 ??

```sh
rm -rf *   /usunięcie wszystkiego w danym katalogu
```



1\. Używając linii poleceń stwórz strukturę katalogów:
```sh

mkdir -p nauka/{c, logo, pascal} dom praca/{dokumenty, zlecenia/{niezrealizowane, zrealizowane}}

```


2\. Przejdź do katalogu dom i utwórz katalog wazne-sprawy.
```sh
cd dom
mkdir wazne-sprawy
```

3\. Wejdź do katalogu wazne-sprawy i utwórz tam pusty plik rachunki.txt.
```sh
cd wazne-sprawy
cat > rachunki.txt
ctrl+C
```
4\.Będąc w katalogu wazne-sprawy skopiuj plik rachunki.txt do katalogu zrealizowane.
```sh
cp rachunki.txt ~/temp/praca/zlecenia/zrealizowane
```
5\.Przejdź do katalogu zrealizowane i zmień nazwę pliku rachunki.txt na wykonano.txt.
```sh
mv rachunki.txt wykonano.txt
```

6\. Utwórz plik wykonano.txt wielkości 11 bajtów, następnie podziel go pliki wielkości 5 bajtów.
W ten sposób otrzymasz 3 pliki. (split)
```sh
cat > wykonano.txt
"1234567890
"
ctrl+c
split --bytes=5 wykonano.txt

```
7\. Będąc w katalogu logo skopiuj powyżej otrzymane 3 pliki do katalogu dokumenty.
```
cd nauka
cd logo
cp ../../praca/zlecenia/zrealizowane/xaa xab xac ../../praca/dokumenty

```
8\. Będąc w katalogu dokumenty połącz skopiowane 3 pliki w plik odtworzono.txt, tak aby otrzymać plik 
o zawartości identycznej z wykonano.txt. Następnie plik odtworzono.txt skopiuj do katalogu wazne-sprawy.

```
cd praca
cd dokumenty
cat x* >> odtworzono.txt
cp odtworzono.txt ../../dom/wazne-sprawy
```

9\. Będąc w katalogu wazne-sprawy sprawdź, czy są jakieś różnice w zawartości plików wykonano.txt i odtworzono.txt.

```
diff odtworzono.txt ../../praca/zlecenia/zrealizowane/wykonano.txt
```

10\. Wyświetl kalendarz na październik 2009 r. (cal)

```
cal 10 2009
cal 10 2009 -3
```

11\. Jaki był dzień tygodnia 25 maja 1975 r. (cal i date)

```
date -d 1975-05-25 +%A
```

