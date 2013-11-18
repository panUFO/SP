###Labolatorium 4

1\. Wyświetl listę plików z aktualnego katalogu, zamieniając wszystkie małe litery na duże.
```sh
ls | tr [:lower:] [:upper:]
```

```sh
ls -1F | sed -e '/[/]/d' | tr 'a-z' 'A-Z'
```

2\. Wyświetl listę praw dostępu do plików w aktualnym katalogu, ich rozmiar i nazwę.
```sh
ls -l
```

```sh
ls -hgoF | tr -s " " | cut -f 1,3,7 -d " " | tr " " "\t" | sed -e '/[/]/d'
```

3\. Wyświetl listę plików w aktualnym katalogu, posortowaną według rozmiaru pliku.
```sh
ls -l -S
```
```sh
ls -h1lS | sed -e '/^d/d' | tr -s " " | cut -f 5,9 -d " " | tac
```

4\. Wyświetl zawartość pliku */etc/passwd* posortowaną według numerów UID w kolejności od największego do najmniejszego.
```sh
cd /etc
cat passwd | sort -r -t : -k 3
```

5\. Wyświetl zawartość pliku */etc/passwd* posortowaną najpierw według numerów GID w kolejności od największego do najmniejszego, a następnie UID.
```sh
cd /etc
cat passwd | sort -r -t : -k 4 -k 3
```

6\. Podaj liczbę plików każdego użytkownika.
```sh
find / -printf '%u\n' 2>/dev/null | sort | uniq -c
```

7\. Sporządź statystykę praw dostępu (dla każdego z praw dostępu podaj ile razy zostało ono przydzielone).
```sh
find -printf "%m\n" | sort | uniq -c
```
