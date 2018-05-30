## WAY 1
```java
@ActivityScope
@Subcomponent(

        modules = {
                LoginModule.class
        }
)
public interface LoginComponent {
    LoginActivity inject(LoginActivity loginActivity);
}
```
