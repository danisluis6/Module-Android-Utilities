```java
@Singleton
@Component(
        modules = {
                AppModule.class,
                RoomModule.class,
                UtilizeModule.class,
                
                <!-- Type 1 -->
                FragmentModule.class
        }
)
public interface AppComponent {
        HomeComponent plusHomeActivity(HomeModule module);
        SplashComponent plusSplashActivity(SplashModule module);
        LoginComponent plusLoginActivity(LoginModule module);
}
```
