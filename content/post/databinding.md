+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-06-01T00:27:32+09:00"
menu = "main"
title = "Data Binding"

+++
Data Binding is the technology to combine static or dynamic data source UI such as XML.

Thre is a need to set the layout tag as follows
```
<layout xmlns:android="http://schemas.android.com/apk/res/android">
    ...
</layout>
```

Please be sure to define the xmlns attribute.
Data binding can be used, but because you can not be an event of onClick calls.
Not called is onSampleClick method in the case of the following.


```
<layout>
    <data>
       <variable name="activity' type="com.activity.MainActivity" />
    </data>
    ...

    <Button
        onClick="@{activity.onSampleClick}" /> // not work
</layout>
```
Please be sure to define the xmnls attribute to the layout.

```
<layout xmlns:android="http://schemas.android.com/apk/res/android">
    <data>
       <variable name="activity' type="com.activity.MainActivity" />
    </data>
    ...

    <Button
        onClick="@{activity.onSampleClick}" /> // work
</layout>
```


