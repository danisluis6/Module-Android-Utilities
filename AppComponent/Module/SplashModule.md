## WAY 1

```java
@Module
public class SplashModule {

    private SplashActivity mSplashActivity;

    public SplashModule(SplashActivity splashActivity) {
        this.mSplashActivity = splashActivity;
    }

    @Provides
    @ActivityScope
    SplashActivity provideSplashActivity() {
        return mSplashActivity;
    }

    @Provides
    @ActivityScope
    SplashPresenter provideSplashPresenter(Context context, SplashActivity activity) {
        return new SplashPresenterImpl(context, activity);
    }

    @Provides
    @ActivityScope
    SliderPaper provideListingAdapter(Context context) {
        return new SliderPaper(context);
    }
}
```
