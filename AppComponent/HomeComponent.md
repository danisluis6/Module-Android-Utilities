## WAY 1
```java
@ActivityScope
@Subcomponent(

        modules = {
                HomeModule.class,
                FragmentModule.class
        }
)
public interface HomeComponent {
    HomeActivity inject(HomeActivity homeActivity);
    ConversationComponent plus(ConversationModule module);
}
```
