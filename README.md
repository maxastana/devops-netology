# devops-netology
1. Test
2. Test2
3. Среда
<<<<<<< HEAD
4. Проверка


=======
>>>>>>> 98ad3ee9e33d6c6c234d4356f5f71ac3409da5d8
Исключить все файлы в поддкаталоге .terraform
*/.terraform/

Исключить файлы с расширением tfstate
*.tfstate .tfstate.

Crash log files
Исключить файлы с названием crash.log
crash.log

Exclude all .tfvars files, which are likely to contain sentitive data, such as
password, private keys, and other secrets. These should not be part of version
control as they are data points which are potentially sensitive and subject
to change depending on the environment.
Исключить файлы с расширением tfvars
*.tfvars

Ignore override files as they are usually used to override resources locally and so
are not checked in
override.tf override.tf.json *_override.tf *_override.tf.json

Исключить файлы, где название заканчивается на override с указанными расширениями
Include override files you do wish to add to version control using negated pattern
!example_override.tf
Include tfplan files to ignore the plan output of command: terraform plan -out=tfplan
example: tfplan
Ignore CLI configuration files
.terraformrc terraform.rc

игнорировать файлы настроек CLI
