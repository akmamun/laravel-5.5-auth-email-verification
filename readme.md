# 1. env file mail setup 
```python
MAIL_DRIVER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME= 
MAIL_PASSWORD= 
MAIL_ENCRYPTION=null
```
# 2. AuthenticatesUsers.php change this function

 ```php
 protected function credentials(Request $request)
    {
        return array_merge($request->only($this->username(), 'password'), ['verified' => 1]);
    }
    
    
