## 2021-4-11

---

- 切換虛擬環境，使用`source djangogirls_venv/bin/activate`或著`. djangogirls_venv/bin/activate`；如果看到前面多了 (虛擬資料夾名稱)，則表示已經成功切換至該虛擬環境。
  
- 請在虛擬環境下指令輸入 python，進入互動式命令列環境，輸入以下的指令取得 Django 版本資訊：
  ```
  >>> import django
  >>> django.VERSION
  (1, 8, 6, 'final, 0')
  ```
  (CTRL+D退出)

- 使用`django-admin.py startproject mysite`，建立新project。

- 切換到myste/，執行`py manage.py runserver`啟動django

- 執行`py manage.py startapp trips`建立app

- 打開 `mysite/settings.py`，找到 `INSTALLED_APPS`，在裡面加入trips

- 在dajango的專案裡，主要的module就是跟最外部資料夾同名的。

| 指令                                        | 說明                            |
| ------------------------------------------- | ------------------------------- |
| django-admin.py startproject <project_name> | 建立 Django 專案                |
| python manage.py -h <command_name>          | 查看 Django commands 的使用方法 |
| python manage.py runserver                  | 啟動開發伺服器                  |
| python manage.py startapp <app_name>        | 新增 Django app                 |
| python manage.py createsuperuser            | 新增 Django 管理者帳號          |

## 2021-4-11
---


### Template Tags
| 語法                                      | 說明                                               |
| ----------------------------------------- | -------------------------------------------------- |
| `{% for ... in ... %}...{% endfor %}`     | 類似 Python 的 for 迴圈，反覆執行 for 區塊中的內容 |
| `{% if %} ... {% else %} ... {% endif %}` | 在 Template Tags 中進行 if／else 的邏輯判斷        |


### Template Filters
| 語法         | 說明                      |
| ------------ | ------------------------- |
| `{{ value \| date:<date_format> }}` | 可以將`datetime`型別的物件，以指定的時間格式 Date Format 輸出 |