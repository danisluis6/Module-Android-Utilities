## WAY 1

```java
@Module
public class FragmentModule {

    public FragmentModule() {
    }

    @Provides
    @ActivityScope
    HomeFragment provideHomeFragment() {
        return new HomeFragment();
    }

    @Provides
    @ActivityScope
    ConversationFragment provideConversationFragment() {
        return new ConversationFragment();
    }

    @Provides
    @ActivityScope
    DiscussFragment provideDiscussFragment() {
        return new DiscussFragment();
    }

    @Provides
    @ActivityScope
    NoticeFragment provideNoticeFragment() {
        return new NoticeFragment();
    }

    @Provides
    @ActivityScope
    PhrasalVerbFragment providePhrasalVerbFragment() {
        return new PhrasalVerbFragment();
    }

    @Provides
    @ActivityScope
    PronunciationFragment providePronunciationFragment() {
        return new PronunciationFragment();
    }

    @Provides
    @ActivityScope
    SentenceFragment provideSentenceFragment() {
        return new SentenceFragment();
    }

    @Provides
    @ActivityScope
    SupportFragment provideSupportFragment() {
        return new SupportFragment();
    }

    @Provides
    @ActivityScope
    VocabularyFragment provideVocabularyFragment() {
        return new VocabularyFragment();
    }
}
```
