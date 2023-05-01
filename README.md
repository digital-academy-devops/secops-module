# Модуль 8. Основы безопасности инфраструктуры.

Целью данного модуля является знакомство с инструментам [Mozilla SOPS](https://github.com/mozilla/sops) и [Hashicorp Vault](https://developer.hashicorp.com/vault/docs/what-is-vault).

## Предварительные требования

Предполагается, что Вы: 
- Выполнили задание по модулю [Kubernetes](https://github.com/digital-academy-devops/k8s-module).

## Задание

1. Для Вашего тестового приложения включите **базовую HTTP аутентификацию** ([HTTP Basic Auth](https://developer.mozilla.org/ru/docs/Web/HTTP/Authentication#%D0%B1%D0%B0%D0%B7%D0%BE%D0%B2%D0%B0%D1%8F_basic_%D1%81%D1%85%D0%B5%D0%BC%D0%B0_%D0%B0%D1%83%D1%82%D0%B5%D0%BD%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D0%B8)) на уровне `Ingress`-а при помощи [аннотаций ingress-nginx контроллера](https://kubernetes.github.io/ingress-nginx/examples/auth/basic/);

    > Используйте отдельный экземпляр манифестов приложения, развертывание **средствами ArgoCD не требуется**.

1. Содержимое `Secret`, используемого для пункта 1, зашифруйте при помощи сгенерированного локально GPG-ключа.
  
1. Опишите манифест, разворачивающий контейнер Vault в [Dev Server Mode](https://developer.hashicorp.com/vault/docs/concepts/dev-server) в том же `Namespace`.
  1. Используйте [официальный образ](https://hub.docker.com/_/vault);
  1. Используйте официальную [документацию](https://developer.hashicorp.com/vault/docs/commands/server) по аргументам командной строки Vault server.
  1. Опубликуйте контейнер с использованием `Ingress` с публичным DNS.
1. Сохраните содержимое файла с приватным ключем в Vault;
1. Напишите инструкцию включающую:
    1. Кодирование и декодирование манифестов
    1. Генерацию, сохранение и получение ключа;
    1. Запуск Vault;
  
  





  
 
