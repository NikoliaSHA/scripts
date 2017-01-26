# scripts
myScripts

#!/bin/bash


--------- script avscan -------------------
### необходимо
1. установка антивируса clamav
2. добавить своего пользователя в группу clamav
	# adduser username clamav

3. сделать скрипт испольняемым
	# chmod +x scripts/avscan

### выполнение
./avscan dir1 dir2 dir3

можно задать папки для сканирования по умолчанию для этого нужно в самом скрипте avscan прописать пути к папкам.

### здесь прописываем пути к папкам	
	DIRP="/home " 

после чего можно запускать скрипт без прописования путей.

если возникат ошибка при обновлении антивируса

Создайте отсутствующий sock-файл:
# touch /var/lib/clamav/clamd.sock
# chown clamav:clamav /var/lib/clamav/clamd.sock
Затем в файле /etc/clamav/clamd.conf раскомментируйте стоку:
    LocalSocket /var/lib/clamav/clamd.sock
Сохраните файл и перезапустите службу clamd
или перезагрузитесь

--------- end script avscan ---------------