```java
@Singleton
@Component(
        modules = {
                AppModule.class,
                RoomModule.class,
                UtilizeModule.class
        }
)
public interface AppComponent {
        HomeComponent plusHomeActivity(HomeModule module);
        SplashComponent plusSplashActivity(SplashModule module);
        LoginComponent plusLoginActivity(LoginModule module);
}
```
