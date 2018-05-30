## WAY 1

```java
@Module
public class RoomModule {

    private AppDatabase mAppDatabase;
    private Application mApplication;
    private Context mContext;

    public RoomModule(Application Application, Context context) {
        mApplication = Application;
        mContext = context;
        mAppDatabase = Room.databaseBuilder(Application, AppDatabase.class, AppDatabase.DB_NAME).build();
    }

    @Singleton
    @Provides
    AppDatabase provideAppDatabase() {
        return mAppDatabase;
    }

    @Singleton
    @Provides
    UserDao providesUserDao() {
        return mAppDatabase.getUsersDao();
    }

    @Singleton
    @Provides
    LoginModel providesLoginModel(UserDao userDao) {
        return new LoginModelImpl(mContext, userDao);
    }

    @Singleton
    @Provides
    ConversationDao providesConversationDao() {
        return mAppDatabase.getConversationDao();
    }

    @Singleton
    @Provides
    ConversationModel providesConversationModel(ConversationDao conversationDao) {
        return new ConversationModelImpl(mContext, conversationDao);
    }

}
```

## WAY 2
