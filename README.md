## HW3-FS-LVM

Работа с LVM https://drive.google.com/file/d/1DMxzJ6ctD0-I0My-iJJEGaeLDnIs13zj/view?usp=share_link 
Что нужно сделать?
на имеющемся образе (centos/7 1804.2)
https://gitlab.com/otus_linux/stands-03-lvm

    уменьшить том под / до 8G
    выделить том под /home
    выделить том под /var (/var - сделать в mirror)
    для /home - сделать том для снэпшотов
    прописать монтирование в fstab (попробовать с разными опциями и разными файловыми системами на выбор)
    Работа со снапшотами:

    сгенерировать файлы в /home/
    снять снэпшот
    удалить часть файлов
    восстановиться со снэпшота
    (залоггировать работу можно утилитой script, скриншотами и т.п.)
    Задание со звездочкой*
    на нашей куче дисков попробовать поставить btrfs/zfs:
    с кешем и снэпшотами
    разметить здесь каталог /opt
	
### Выполнение  
Нач_условия.jpg - то, что мы имеем вначале  
Утилиту script я сразу не запускал, т.к. у неё получается очень замусоренный вывод для команд синхронизации и дампа  
Скриншоты root_to_8G_1-8.jpg показывают выполнение 1-й части - уменьшить том под / до 8G, - всё по методичке  
Скриншоты var_to_mirror_1-4.jpg показывают выполнение и результат выделения тома под /var (/var - сделать в mirror)  
Скриншоты volume_home_1-3.jpg - том под /home, для /home - сделать том для снэпшотов, прописать монтирование в fstab и  
работа со снэпшотами.  
Собственно скрипт выполнения команд после перезагрузки и работы с томом под /home - файл script_LVM.txt  
