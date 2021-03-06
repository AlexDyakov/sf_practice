# Тестирование и тестовые-среды (стенды)

## Проектная работа 10

## Что нужно сделать
1. Создать на GitHub профиль и репозиторий под названием sf_practice, в нем создать директорию с названием «6».
2. На своей локальной машине (ПК/ноутбук/etc) настроить связку Vagrant+VirtualBox.
3. Создать пустой файл на файловой системе этой хостовой машины.
4. Создать Vagrantfile, при использовании которого будет создаваться ВМ под управлением Ubuntu 18.04.
5. Настроить Vagrantfile таким образом, чтобы на эту машину при ее создании установились python3- и python3-pip-пакеты, а также Python-библиотеки psycopg2 (для подключения к PostgreSQL СУБД) и Django (для работы с фронтендом).
6. Дополнить Vagrantfile командой копирования созданного нами пустого файла на файловую систему созданной машины (в будущем при реальной работе с тестовым окружением, разработчики будут вместо этого пустого файла копировать на создаваемую ВМ свои скрипты и запускать их там).
7. Отправьте этот Vagrantfile в созданный в п.1 репозиторий в директорию «6».

## Использование

```bash
vagrant up
vagrant ssh
```

1. Для установки psycopg2 требуется установка зависимостей, соответствующие команды добавлены в Vagrantfile.
2. После выполнения Vagrantfile содержимое папки src будет перенесено на файловую систему виртуальной машины в директорию /home/vagrant/src.