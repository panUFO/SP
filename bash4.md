###Labolatorium 4

1\. Wyświetl listę plików z aktualnego katalogu, zamieniając wszystkie małe litery na duże.
```sh
ls | tr [:lower:] [:upper:]
```

2\. Wyświetl listę praw dostępu do plików w aktualnym katalogu, ich rozmiar i nazwę.
```sh
ls -l
```

3\. Wyświetl listę plików w aktualnym katalogu, posortowaną według rozmiaru pliku.
```sh
ls -l -S
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

```

7\. Sporządź statystykę praw dostępu (dla każdego z praw dostępu podaj ile razy zostało ono przydzielone).
```sh

```