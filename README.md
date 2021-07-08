# interpris_platform
interpris Platform repository
coreDNS перезапускает  daemonset.
В случае kube-apiserver,  это делает kubelet.
При создании образа за основу был взять образ Nginx.
Создан пользователь с UID 1001.
Добавлен в группу nginx.
Изменены права на служебные каталоги используемые Nginx
Создана символическая ссылка с каталога по умолчанию в каталог ./app

