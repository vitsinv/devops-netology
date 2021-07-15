# devops-netology
# first update this file

И вновь новые строки

Описание .gitignore для папки terraform и ее подпапок:
# Local .terraform directories - Игнорятся папки с названием .terraform, вне зависимости от подпапок
**/.terraform/*

# .tfstate files - игнорятся как любые файлы с расширением .tfstate и с любым расширением после .tfstate.
# При этом любое продолжение после tfstate без точки игнориться не будет
*.tfstate
*.tfstate.*

# Исключаем crash.log файлы
crash.log

# Исключаем все файлы с расширением tfvars
*.tfvars

# Исключаем файлы override.tf и override.tf.json а такжи все вариации заканчивающиеся на _override.tf и 
# _override.tf.json

*_override.tf
*_override.tf.json

# При этом возможно исключение для example_override.tf, но по умолчанию не работает
# !example_override.tf

# Возможно исключение всех файлов содержащих tfplan
# example: *tfplan*

# Игнорирование файлов конфигураций CLI
.terraformrc
terraform.rc