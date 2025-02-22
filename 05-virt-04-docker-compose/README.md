# Домашнее задание к занятию 4. «Оркестрация группой Docker-контейнеров на примере Docker Compose»


---


---

## Задача 1

Создайте собственный образ любой операционной системы (например, debian-11) с помощью Packer версии 1.5.0 ([инструкция](https://cloud.yandex.ru/docs/tutorials/infrastructure-management/packer-quickstart)).

Чтобы получить зачёт, вам нужно предоставить скриншот страницы с созданным образом из личного кабинета YandexCloud.

![3](https://github.com/AlexanderM33/virtd-homeworks/assets/122460278/b4cfd7a8-d3e0-4844-9e52-36189c154e99)


## Задача 2

**2.1.** Создайте вашу первую виртуальную машину в YandexCloud с помощью web-интерфейса YandexCloud.        

![q2](https://github.com/AlexanderM33/virtd-homeworks/assets/122460278/edf107b5-641b-4190-b944-a51d70b810f2)



## Задача 3

С помощью Ansible и Docker Compose разверните на виртуальной машине из предыдущего задания систему мониторинга на основе Prometheus/Grafana.
Используйте Ansible-код в директории ([src/ansible](https://github.com/netology-group/virt-homeworks/tree/virt-11/05-virt-04-docker-compose/src/ansible)).

Чтобы получить зачёт, вам нужно предоставить вывод команды "docker ps" , все контейнеры, описанные в [docker-compose](https://github.com/netology-group/virt-homeworks/blob/virt-11/05-virt-04-docker-compose/src/ansible/stack/docker-compose.yaml),  должны быть в статусе "Up".

![q5](https://github.com/AlexanderM33/virtd-homeworks/assets/122460278/b73740e0-2583-4013-a56e-b293ab8d6af4)


## Задача 4

1. Откройте веб-браузер, зайдите на страницу http://<внешний_ip_адрес_вашей_ВМ>:3000.
2. Используйте для авторизации логин и пароль из [.env-file](https://github.com/netology-group/virt-homeworks/blob/virt-11/05-virt-04-docker-compose/src/ansible/stack/.env).
3. Изучите доступный интерфейс, найдите в интерфейсе автоматически созданные docker-compose-панели с графиками([dashboards](https://grafana.com/docs/grafana/latest/dashboards/use-dashboards/)).
4. Подождите 5-10 минут, чтобы система мониторинга успела накопить данные.



Чтобы получить зачёт, предоставьте: 


- скриншот работающего веб-интерфейса Grafana с текущими метриками, как на примере ниже.
<p align="center">
  <img width="1200" height="600" src="./assets/yc_02.png">
</p>



![q3](https://github.com/AlexanderM33/virtd-homeworks/assets/122460278/00ba9a9d-92a7-4280-ac7f-a10111c72876)

![q4](https://github.com/AlexanderM33/virtd-homeworks/assets/122460278/8f524abd-f863-4fdd-8f29-75393e2f8533)




