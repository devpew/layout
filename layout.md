#Layout

Для того чтобы изменить стандартную линуксовую раскладку на мою нужно убедиться что в текущем линуксе существуют файлы "ru" и "us" в папке

~~~~
/usr/share/X11/xkb/symbols/ru
~~~~

Далее делаем бекап этих файлов:

~~~~
sudo cp /usr/share/X11/xkb/symbols/ru /usr/share/X11/xkb/symbols/ru_oiginal
sudo cp /usr/share/X11/xkb/symbols/us /usr/share/X11/xkb/symbols/us_oiginal
~~~~

Удаляем файлы стандартные

~~~~
sudo rm /usr/share/X11/xkb/symbols/ru
sudo rm /usr/share/X11/xkb/symbols/us
~~~~

Копирую свои файлы

~~~~
sudo cp /home/dm/Documents/kn_base/files/ru /usr/share/X11/xkb/symbols/ru
sudo cp /home/dm/Documents/kn_base/files/us /usr/share/X11/xkb/symbols/us
~~~~

other:

~~~~
sudo chmod 0644 /usr/share/X11/xkb/symbols/ru
~~~~

~~~~
stat /usr/share/X11/xkb/symbols/ru
~~~~

~~~~
setxkbmap -option grp:caps_toggle "us,ru" -option grd_led:caps
~~~~
