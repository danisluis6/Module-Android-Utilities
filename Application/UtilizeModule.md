```java
@Module
public class UtilizeModule {

    private Application mApplication;
    private Context mContext;

    public UtilizeModule(Application Application, Context context) {
        mApplication = Application;
        mContext = context;
    }

    @Provides
    @Singleton
    BitmapLibrary provideBitmapLibrary() {
        return new BitmapLibrary();
    }
}
```
