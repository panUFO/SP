```sh
#!/bin/bash

clear


if `! dpkg -l | grep -q pwgen`
then
	while [ 1 ]
	do
		read -p "Nie znaleziono programu pwgen. Czy chcesz go zainstalować? T/N$" xx

		if [ "$xx" = "t" ] || [ "$xx" = "T" ]
		then
			apt-get install pwgen
			break
		elif [ "$xx" = "n" ] || [ "$xx" = "N" ]
		then
			exit
		else
			xx=""
		fi
	done
fi


clear


echo "PROGRAM GENERUJĄCY HASŁA"

x="0"
while [ 1 ]
do
	read -p "Podaj długość hasła: " x
	if [ $x ]
	then
		if [ $x -gt 0 ]
		then
			break
		else
			echo "Musisz podać długość hasła!"
		fi
	else
		echo "Musisz podać długość hasła!"
	fi
done

y="0"
while [ 1 ]
do
	read -p "Podaj ilość haseł: " y
	if [ $y ]
	then
		if [ $y -gt 0 ]
		then
			break
		else
			echo "Musisz podać ilość haseł!"
		fi
	else
		echo "Musisz podać ilość haseł!"
	fi
done

echo "Generowanie..."

pwgen -s -y $x -N $y -1
```
