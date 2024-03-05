# ans-hw-01

1. Попробуйте запустить playbook на окружении из test.yml, зафиксируйте значение, которое имеет факт some_fact для указанного хоста при выполнении playbook.

```
TASK [Print fact] *****************
ok: [localhost] => {
    "msg": 12
}
```

2. Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на all default fact.

```
TASK [Print fact] *****************
ok: [localhost] => {
    "msg": "all default fact"
}
```
3. Воспользуйтесь подготовленным (используется docker) или создайте собственное окружение для проведения дальнейших испытаний.

Тут подсмотрел запуск через докер:

 docker run -dit --name centos7 pycontribs/centos:7 sleep 6000000
 docker run -dit --name ubuntu pycontribs/ubuntu:latest sleep 6000000

4. Проведите запуск playbook на окружении из prod.yml. Зафиксируйте полученные значения some_fact для каждого из managed host.

```
TASK [Print fact] *****************
ok: [centos7] => {
    "msg": "el"
}
ok: [ubuntu] => {
    "msg": "deb"
}
```