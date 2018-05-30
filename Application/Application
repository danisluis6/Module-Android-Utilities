```java
public class Application extends android.app.Application {

    private AppComponent mApplicationComponent;
    private Context mContext;
    private static Application sInstance;

    public static Bus eventBus;

    public static synchronized Application getInstance() {
        if (sInstance == null) {
            sInstance = new Application();
        }
        return sInstance;
    }

    @Override
    public void onCreate() {
        super.onCreate();
        mContext = this;
        sInstance = this;
        eventBus  = new Bus(ThreadEnforcer.ANY);
        initAppComponent();
    }

    private void initAppComponent() {
        mApplicationComponent = DaggerAppComponent.builder()
                .appModule(new AppModule(this,mContext))
                .roomModule(new RoomModule(this, mContext))
                .utilizeModule(new UtilizeModule(this, mContext))
                .build();
    }

    public AppComponent getAppComponent() {
        return mApplicationComponent;
    }

}
```
