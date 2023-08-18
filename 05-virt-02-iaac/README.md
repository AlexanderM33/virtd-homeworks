
# Домашнее задание к занятию 2. «Применение принципов IaaC в работе с виртуальными машинами»

## Как сдавать задания

Обязательны к выполнению задачи без звёздочки. Их нужно выполнить, чтобы получить зачёт и диплом о профессиональной переподготовке.

Задачи со звёздочкой (*) — дополнительные задачи и/или задачи повышенной сложности. Их выполнять не обязательно, но они помогут вам глубже понять тему.

Домашнее задание выполните в файле readme.md в GitHub-репозитории. В личном кабинете отправьте на проверку ссылку на .md-файл в вашем репозитории.

Любые вопросы по решению задач задавайте в чате учебной группы.

---


## Важно

Перед отправкой работы на проверку удаляйте неиспользуемые ресурсы.
Это нужно, чтобы не расходовать средства, полученные в результате использования промокода.

Подробные рекомендации [здесь](https://github.com/netology-code/virt-homeworks/blob/virt-11/r/README.md).

---

## Задача 1

- Опишите основные преимущества применения на практике IaaC-паттернов.
- Какой из принципов IaaC является основополагающим?

````

Преимущества IaaC:
Ускорение производства и вывода продукта на рынок
Стабильность среды, устранение дрейфа конфигураций
Более быстрая и эффективная разработка
А главное преимущество IaaC это Идемпотентность (это свойство объекта или операции, 
при повторном выполнении которой мы получаем результат идентичный предыдущему и всем последующим)


IaaC-паттерны
Преимущества CI  (Непрерывная интеграция) - возможность раннего выявления дефектов 
Преимущества CD Непрерывная доставка (Непрерывная доставка) - изменения частые и небольшие -
то есть много ошибок не успевает накопиться, удобнее работать.
Преимущества CD (Непрерывное развёртывание) - можно автоматизировать тестирование, 
избавиться от рутины

Основополагающий принцип IaaC уже в названии - это Infrastructure as Code. 
Как подчеркивалось в лекции, это гарантирует идемпотентность, необходимую для
обеспечения максимальной автоматизации всего жизненного цикла инфраструктуры.

````



## Задача 2

- Чем Ansible выгодно отличается от других систем управление конфигурациями?
- Какой, на ваш взгляд, метод работы систем конфигурации более надёжный — push или pull?

````

````


## Задача 3

Установите на личный компьютер:

- [VirtualBox](https://www.virtualbox.org/),
- [Vagrant](https://github.com/netology-code/devops-materials),
- [Terraform](https://github.com/netology-code/devops-materials/blob/master/README.md),
- Ansible.

*Приложите вывод команд установленных версий каждой из программ, оформленный в Markdown.*

````
root@Ubuntu2204:~# virtualbox -h
Oracle VM VirtualBox VM Selector v6.1.38_Ubuntu
(C) 2005-2022 Oracle Corporation
All rights reserved.

No special options.

If you are looking for --startvm and related options, you need to use VirtualBoxVM.
root@Ubuntu2204:~# vboxmanage --version
6.1.38_Ubuntur153438
root@Ubuntu2204:~#
root@Ubuntu2204:~#
root@Ubuntu2204:~# vagrant --version
Vagrant 2.3.7
root@Ubuntu2204:~#
root@Ubuntu2204:~#
root@Ubuntu2204:~# ansible --version
ansible [core 2.15.3]
  config file = None
  configured module search path = ['/root/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /root/.local/lib/python3.10/site-packages/ansible
  ansible collection location = /root/.ansible/collections:/usr/share/ansible/collections
  executable location = /usr/bin/ansible
  python version = 3.10.12 (main, Jun 11 2023, 05:26:28) [GCC 11.4.0] (/usr/bin/python3)
  jinja version = 3.0.3
  libyaml = True
root@Ubuntu2204:~#
root@Ubuntu2204:~# terraform --version
Terraform v1.5.5
on linux_amd64



````


## Задача 4 

Воспроизведите практическую часть лекции самостоятельно.

- Создайте виртуальную машину.
- Зайдите внутрь ВМ, убедитесь, что Docker установлен с помощью команды
```
docker ps,
```
Vagrantfile из лекции и код ansible находятся в [папке](https://github.com/netology-code/virt-homeworks/tree/virt-11/05-virt-02-iaac/src).

Примечание. Если Vagrant выдаёт ошибку:
```
URL: ["https://vagrantcloud.com/bento/ubuntu-20.04"]     
Error: The requested URL returned error: 404:
```

выполните следующие действия:

1. Скачайте с [сайта](https://app.vagrantup.com/bento/boxes/ubuntu-20.04) файл-образ "bento/ubuntu-20.04".
2. Добавьте его в список образов Vagrant: "vagrant box add bento/ubuntu-20.04 <путь к файлу>".

*Приложите скриншоты в качестве решения на эту задачу.*

