# Установка windows server
## Источник - https://youtu.be/AenrMZs5PNo
1. Заходим на ec2 https://eu-west-3.console.aws.amazon.com/ec2/v2/home?region=eu-west-3#Home:
2. Нажимаем `Launch Instance`
3. Попадаем на шаг 1 - 'Choose AMI'. Выбираем из списка машин Microsoft Windows Server 2016 Base
4. Попадаем на шаг 2 - 'Choose an Instance Type'. Оставляем все как есть, нажимаем `Next: Configure Instance Details`
5. Попадаем на шаг 3 - 'Configure Instance'.

5.1. Ставим галочку напротив 'Enable termination protection'

5.2. Нажимаем `Next: Add Storage`

6. Попадаем на шаг 4 - 'Add Storage'. Оставляем все как есть, нажимаем `Next: Add Tags`
7. Попадаем на шаг 5 - 'Add Tags'. Нажимаем `Add Tag`

7.1. Добавляем тег со значениями 'Key' = 'Name', 'Value' = 'WebServer-WINDOWS'.

7.2. Нажимаем `Next: Configure Security Group`

8. Попадаем на шаг 6 - 'Configure Security Group'. Заполняем поля: 'Security group name' = 'MyFirewall-HTTP-HTTPS-RDP', 'Description' = 'MyFirewall-HTTP-HTTPS-RDP'

8.1. Настраиваем первый Rule: 'Type' = 'HTTP', 'Source' = 'Anywhere'

8.2. Нажимаем `Add Rule`. Настраиваем его: 'Type' = 'HTTPS', 'Source' = 'Anywhere'

8.3. Нажимаем `Add Rule`. Настраиваем его: 'Type' = 'RDP', 'Source' = 'My IP'

8.4. Нажимаем `Review and Launch` 

9. Попадаем на шаг 6 - 'Review'. Просматриваем общее описание будущего сервера

10. Попадаем на попап 'Select an existing key pair or create a new key pair'. Выбираем 'Create a new key pair'

10.1. Заполняем поле 'Key pair name' = 'denis-key-paris'

10.2. Нажимаем `Download Key Pair`

10.3. Нажимаем `Launch Instances`
