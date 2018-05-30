# Module-Android-Utilities
## MODULE ANDROID UTILITIES [![Build Status](https://travis-ci.org/nomensa/jquery.hide-show.svg)](https://travis-ci.org/nomensa/jquery.hide-show.svg?branch=master)

   ```You just do.```
  
## SoftwareKeyBoardUtilize:
- [x] How to check visibility of software keyboard in Android?

```java

@Provides
@ActivityScope
Activity provideActivity() {
    return Activity;
}

public class SoftwareKeyBoardUtilize {

    @Inject
    public SoftwareKeyBoardUtilize() {
    }

    public void attachEventKeyBoard(final View activityRootView, View controlView) {
        activityRootView.getViewTreeObserver().addOnGlobalLayoutListener(new ViewTreeObserver.OnGlobalLayoutListener() {
            @Override
            public void onGlobalLayout() {
                int heightDiff = activityRootView.getRootView().getHeight() - activityRootView.getHeight();
                if (heightDiff > Utils.dpToPx(LoginActivity.this, 200)) {
                    if (controlView != null)
                        controlView.setVisibility(View.GONE);
                } else {
                    if (controlView != null)
                        controlView.setVisibility(View.VISIBLE);
                }
            }
        });
    }
}
```
- [x] set/get Title in activity in Android






