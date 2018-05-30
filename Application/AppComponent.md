```java
@Singleton
@Component(
        modules = {
                <a href="#links">AppModule.class</a>,
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
