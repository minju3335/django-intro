# django

1. 프로젝트 생성
```
django-admin startproject <pjtname> .
```

2. 가상환경 설정
```
python -m venv venv
```

3. 가상환경 활성화/비활성화
- (venv)가 뜨면 활성화가 된 것
```
<!--window -->
source venv/Scrips/activate
<!-- macOS -->
source venv/bin/activate
```
- 파이썬을 복제해온 것이라고 이해하면 됨
- deactivate 치면 비활성화됨



4. 가상환경 내부에 django 설치
```
pip install django
```


5. 서버 실행 확인 (종료 'Ctrl+c')
```
python manage.py runserver
```

6. 앱생성
```
django-admin startapp <appname>
```

7. 앱등록
- `settings.py`의 `INSTALLED_APPS`에 등록
    - `<appname>`을 등록


8. `urls.py` 이정표(길잡이)역할
```python
from django.urls import path
from app_intro import views

urlpatterns = [
...
    path('index/',views.index),
]
```


9. `views.py`
```python
def index(request):
    return render(request, 'index.html')
```

