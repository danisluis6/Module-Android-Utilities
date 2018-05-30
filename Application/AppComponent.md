```java
@Singleton
@Component(
        modules = {
                /** Type 1 */
                AppModule.class,
                RoomModule.class,
                UtilizeModule.class,
                
                /** Type 2 */
                AppModule.class,
                FragmentModule.class
        }
)
public interface AppComponent {
        HomeComponent plusHomeActivity(HomeModule module);
        SplashComponent plusSplashActivity(SplashModule module);
        LoginComponent plusLoginActivity(LoginModule module);
}
```
