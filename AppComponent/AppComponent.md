```java
@Singleton
@Component(
        modules = {
                /** WAY 1 */
                AppModule.class,
                RoomModule.class,
                UtilizeModule.class,
                
                /** WAY 2 */
                AppModule.class,
                FragmentModule.class
                
                /** WAY 3 */
        }
)
public interface AppComponent {

        /** WAY 1 */
        HomeComponent plusHomeActivity(HomeModule module);
        SplashComponent plusSplashActivity(SplashModule module);
        LoginComponent plusLoginActivity(LoginModule module);
        
        /** WAY 2 */
        
        
        /** WAY 3 */
        
}
```
