# Celery Test
Testing Celery with RabiitMQ. Simple app to sending emails from django(gmail configartion).

## RabbitMQ 
For inspiron with windowsOS
-> install Erlang -> install RabbitMQ for windows

start RabbitMQ:
```
RabbitMQ Server\rabbitmq_server-3.8.14\sbin> rabbitmq-server start 
```

## Callnig worker on WindowsOS
```
celery -A project-name worker -l info --pool=solo
```

## Gmail configuration
```
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_HOST_USER = ' <email> @gmail.com'  # set gmail login
EMAIL_HOST_PASSWORD = ' <pass from gmail security settings> '  # set password for this app in gmail security settings
EMAIL_PORT = 587
EMAIL_USE_TLS = True
DEFAULT_FROM_EMAIL = ' <email> @gmail.com'  # set default value for from_email attribute of send_mail()
```
