# Домашнее задание к занятию "`Что такое DevOps. CI/CD`" - `Kubatin Artem`

### Задание 1

**Что нужно сделать:**

1. Установите себе jenkins по инструкции из лекции или любым другим способом из официальной документации. Использовать Docker в этом задании нежелательно.
2. Установите на машину с jenkins [golang](https://golang.org/doc/install).
3. Используя свой аккаунт на GitHub, сделайте себе форк [репозитория](https://github.com/netology-code/sdvps-materials.git). В этом же репозитории находится [дополнительный материал для выполнения ДЗ](https://github.com/netology-code/sdvps-materials/blob/main/CICD/8.2-hw.md).
3. Создайте в jenkins Freestyle Project, подключите получившийся репозиторий к нему и произведите запуск тестов и сборку проекта ```go test .``` и  ```docker build .```.

В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

### Решение:

1. установил jenkins and java
![jenkins](image.png)
2. Добавляем jenkins в группу докер:
sudo usermod -aG docker jenkins
3. сделал форк https://github.com/CryForEternirty/CICD-homeworl
4. установил golang:

wget https://go.dev/dl/go1.17.5.linux-amd64.tar.gz

rm -rf /usr/local/go && tar -C /usr/local -xzf go1.17.5.linux-amd64.tar.gz

echo 'export PATH=$PATH:/usr/local/go/bin' >> /etc/profile

5. Скриншот настроек:
![project_settings](image-1.png)
![project_settings](image-2.png)
![project_settings](image-3.png)
6. Скриншот результата:
![result](image-4.png)

---

### Задание 2

**Что нужно сделать:**

1. Создайте новый проект pipeline.
2. Перепишите сборку из задания 1 на declarative в виде кода.

В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

### Решение:

1. Создал новый проект CICDHW2
2. Добавил скрипт в настройках pipline:
![script settings](image-5.png)
3. Скриншот результата:
![result](image-6.png)

---

### Задание 3

**Что нужно сделать:**

1. Установите на машину Nexus.
1. Создайте raw-hosted репозиторий.
1. Измените pipeline так, чтобы вместо Docker-образа собирался бинарный go-файл. Команду можно скопировать из Dockerfile.
1. Загрузите файл в репозиторий с помощью jenkins.

В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

### Решение: 

1. Создал новый проект CICDHW2
2. Добавил скрипт в настройках pipline:
![script](image-7.png)
3. Скриншот результата:
![result](image-8.png)
![result](image-9.png)
