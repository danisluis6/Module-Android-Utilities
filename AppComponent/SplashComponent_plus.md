## WAY 1
```java
@ActivityScope
@Subcomponent(

        modules = {
                SplashModule.class
        }
)
public interface SplashComponent {
    SplashActivity inject(SplashActivity splashActivity);
}
```
