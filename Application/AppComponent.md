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
                
                /** Type 3 */
        }
)
public interface AppComponent {

        /** Type 1 */
        HomeComponent plusHomeActivity(HomeModule module);
        SplashComponent plusSplashActivity(SplashModule module);
        LoginComponent plusLoginActivity(LoginModule module);
        
        /** Type 2 */
        
        
        /** Type 3 */
        
}
```
