# 1. env file mail setup 
```php
MAIL_DRIVER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME= 
MAIL_PASSWORD= 
MAIL_ENCRYPTION=null
```
# Note: Use this function in 'Auth/LoginController' to Overwrite Laravel Building Auth Login
##### Laravel Building Auth Login Not Verify Email Login System, Overwrite this Because We are Not Access to Login Without Mail Verification 
 ```php
 use Illuminate\Http\Request; 
 
 protected function credentials(Request $request)
    {
        return array_merge($request->only($this->username(), 'password'), ['verified' => 1]);
    }
    
    
