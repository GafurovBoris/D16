
Автор: Гафуров Борис

 
---
## 🔧Технические детали🔩 

Применяется ```` allauth```` (позволяет проводить регистрацию пользователей на сайте) и ```` ckeditor```` (позволяет форматировать обьявление, вставлять медиафайлы в объявление)


Указываем:
```` 
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'django.contrib.sites',
    'django.contrib.flatpages',
    'postboard.apps.PostboardConfig',

    'fpages',
    'django_filters',

    'allauth',
    'allauth.account',
    'allauth.socialaccount',
    'allauth.socialaccount.providers.yandex',

    'ckeditor',
    'ckeditor_uploader',
]

...........

CKEDITOR_CONFIGS = {
    'default': {
        'toolbar': 'full',
        'height': 300,
        'width': 900,
        'image2_responsive': True,
        'image2_maxWidth': 500,
    },
}
............

CKEDITOR_BASEPATH = "/static/ckeditor/ckeditor/"

CKEDITOR_UPLOAD_PATH = 'media/'

MEDIA_ROOT = 'media/'

MEDIA_URL = '/media/'

CKEDITOR_FILENAME_GENERATOR = 'utils.get_filename'

..............

ACCOUNT_EMAIL_REQUIRED = True
ACCOUNT_UNIQUE_EMAIL = True
ACCOUNT_USERNAME_REQUIRED = False
ACCOUNT_AUTHENTICATION_METHOD = 'email'
ACCOUNT_EMAIL_VERIFICATION = 'mandatory'


EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend'
EMAIL_HOST = 'smtp.yandex.ru'
EMAIL_PORT = 465
EMAIL_HOST_USER = "__________"
EMAIL_HOST_PASSWORD = "----------"
EMAIL_USE_TLS = False
EMAIL_USE_SSL = True

DEFAULT_FROM_EMAIL = "_____________"
SERVER_EMAIL = "__________"

 