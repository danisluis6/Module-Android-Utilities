## WAY 1
```java
@Module
public class LoginModule {

    private LoginActivity mLoginActivity;
    private LoginView mLoginView;

    public LoginModule(LoginActivity loginActivity, LoginView loginView) {
        this.mLoginActivity = loginActivity;
        this.mLoginView = loginView;
    }

    @Provides
    @ActivityScope
    LoginActivity provideLoginActivity() {
        return mLoginActivity;
    }

    @Provides
    @ActivityScope
    LoginPresenter provideLoginPresenter(Context context, LoginActivity activity, Validator validator, LoginModel loginModel) {
        return new LoginPresenterImpl(context, activity, validator, loginModel, mLoginView);
    }
}
```
