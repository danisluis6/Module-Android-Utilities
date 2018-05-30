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
    
    public static float dpToPx(Context context, float valueInDp) {
        DisplayMetrics metrics = context.getResources().getDisplayMetrics();
        return TypedValue.applyDimension(TypedValue.COMPLEX_UNIT_DIP, valueInDp, metrics);
    }
}
```
- [x] set/get Title in activity in Android






