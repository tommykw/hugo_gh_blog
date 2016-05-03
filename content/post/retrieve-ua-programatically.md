+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-05-03T12:57:48+09:00"
menu = "main"
title = "retrieve UserAgent programatically"

+++
In the android app, it describes how to obtain the general UserAgent.
Method of acquiring the UserAgent from the API Level 17 must be noted the changes.

```
public class UserAgentGetter {
    // You may uncomment next line if using Android Annotations library, otherwise just be sure to run it in on the UI thread
    // @UiThread 
    public static String getDefaultUserAgentString(Context context) {
        if (Build.VERSION.SDK_INT >= 17) {
            return NewApiWrapper.getDefaultUserAgent(context);
        }
    
        try {
            Constructor<WebSettings> constructor = WebSettings.class.getDeclaredConstructor(Context.class, WebView.class);
            constructor.setAccessible(true);
            try {
                WebSettings settings = constructor.newInstance(context, null);
                return settings.getUserAgentString();
            } finally {
                constructor.setAccessible(false);
            }
        } catch (Exception e) {
            return new WebView(context).getSettings().getUserAgentString();
        }
    }
    
    @TargetApi(17)
    static class NewApiWrapper {
        static String getDefaultUserAgent(Context context) {
            return WebSettings.getDefaultUserAgent(context);
        }
    }
}
```

Also See
http://stackoverflow.com/questions/3626071/retrieve-user-agent-programatically/5261472#5261472
