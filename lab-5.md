## **Отчет по лабораторной работе №5**

### Git Hooks
1. Создала репозиторию в гитхабе - git-lab
2. Открыла папку hooks, и в файле `pre-commit` написала bash script, который перед каждым коммитом проверял наличие лишних пробелов в конце `.txt` файла, и при их наличии, выдавал ошибку
   
![image](https://github.com/user-attachments/assets/12795344-6e5b-42a8-ba02-1d806a60e417)


3. Создала файл с пробелами в конце текста, пробовала его закоммитать, `git hooks` блокировал коммит пока я не удалила лишние пробелы

![image](https://github.com/user-attachments/assets/b72c0fb0-e76f-42ca-b92f-69233ff7634e)


### Git Flow

1. В корне репозитория выполниа инициализацию `Git Flow`

![image](https://github.com/user-attachments/assets/af78039f-8d9a-4452-9e6a-2c656c2b5b62)

2. Создала ветку для новой функциональности, под названием `task-management`, добавила функционал управления задачами
```
def create_task(title, description):
    # Логика создания задачи
    print(f"Создана новая задача: {title}")
```

3.После завершения разработки функции завершила фичу и объединила ее с основной веткой
```
git flow feature finish task-management
```

4. Переключилась на ветку "develop" и начала создание релиза:
```
git checkout develop
git flow release start v1.0.0
```

5. Oбновила версию в файле version.txt

![image](https://github.com/user-attachments/assets/9b6b2dff-5bf9-4b1d-91fa-e96a56f2f8fa)

6. Завершила релиз и объединила с ветками `develop` и `main`
   
![image](https://github.com/user-attachments/assets/aba7b192-a76c-4048-9d4c-a2eafccaf719)

7. Создала hotfix (допустим, что у нас возникла критическая ошибка)

![image](https://github.com/user-attachments/assets/5cca26c0-b7f1-4452-9d27-69bef6a7de0a)

8. Внесла изменения для исправления ошибки и закоммитала, завершила hotfix и объединила его с ветками "develop" и "main"
   
![image](https://github.com/user-attachments/assets/55cb05f5-ba31-406d-848f-34558e082b5d)

9. Завершила работу и отправила изменения на удаленный репозиторий

![image](https://github.com/user-attachments/assets/c87485dc-428e-4e05-90a0-df9912461b94)



