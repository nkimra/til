# PlayFramework

## フォームのPOST送信

- FormFactoryをDIし、リクエスト格納するDTOクラスを作り、bindFromRequestに格納する。

- login.scala.html

~~~ HTML
<form id="registerForm" role="form" action="@LoginController.doLogin()" method="POST">
<input type="text" name="loginId">
~~~

- LoginForm.java

~~~ Java
private String loginId;

public String getLoginId() {
    return userName;
}
~~~

- LoginController.java

~~~ Java
@Inject
FormFactory formFactory;

Form<LoginForm> form = formFactory.form(LoginForm.class);
LoginRequest request = form.bindFromRequest().get();
~~~
