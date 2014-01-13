###SKRYPT
```sh
#!/usr/bin/perl -w
system "clear";
print "PROGRAM GENERUJĄCY HASŁA \n";
print "Podaj długość hasła ";
$dlugosc = <STDIN>;
if ($dlugosc lt "1")
{ print "NIE WPROWADZONO ZADNEJ DLUGOSCI, KONIEC PROGRAMU\n";
exit}

print "ILE HASEŁ WYGENEROWAĆ? ";
$powt =<STDIN>;
if ($powt lt "1")
{ print "BRAK ILOŚCI, KONIEC PROGRAMU\n";
exit}
print "NO TO GENERUJEMY! <3\n";
$ile = $powt;
for (1 ..$powt)
{
{ @lines = `pwgen -s -y $dlugosc`;print "hasło:     ";}
foreach (@lines) #-y, (znaki specjalne) -s (bezpieczne, trudne do zapamietania)

{print;}
}

```
