## WAY 1

```java
@Module
public class FragmentModule {

    public FragmentModule() {
    }

    @Provides
    @Singleton
    FileViewerFragment provideFileViewerFragment() {
        return new FileViewerFragment();
    }

    @Provides
    @Singleton
    RecordFragment provideRecordFragment() {
        return new RecordFragment();
    }

    @Provides
    @Singleton
    SettingFragment provideSettingFragment() {
        return new SettingFragment();
    }

    @Provides
    @Singleton
    LicensesFragment provideLicensesFragment() {
        return new LicensesFragment();
    }

}
```
