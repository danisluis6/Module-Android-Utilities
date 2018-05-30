## WAY 1

```java
@Module
public class HomeModule {

    private HomeActivity mHomeActivity;

    public HomeModule(HomeActivity homeActivity) {
        this.mHomeActivity = homeActivity;
    }

    @Provides
    @ActivityScope
    HomeActivity provideHomeActivity() {
        return mHomeActivity;
    }

    @Provides
    @ActivityScope
    HomePresenter provideHomePresenter(Validator validator, Context context, HomeActivity homeActivity,
                                       HomeFragment homeFragment,
                                       ConversationFragment conversationFragment,
                                       DiscussFragment discussFragment,
                                       NoticeFragment noticeFragment,
                                       PhrasalVerbFragment phrasalVerbFragment,
                                       PronunciationFragment pronunciationFragment,
                                       SentenceFragment sentenceFragment,
                                       SupportFragment supportFragment,
                                       VocabularyFragment vocabularyFragment) {
        return new HomePresenterImpl(validator, context, homeActivity,
                homeFragment, conversationFragment, discussFragment, noticeFragment, phrasalVerbFragment, pronunciationFragment, sentenceFragment, supportFragment, vocabularyFragment
        );
    }
}
```
