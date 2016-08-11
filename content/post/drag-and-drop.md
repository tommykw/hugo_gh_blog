+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-08-11T14:22:18+09:00"
menu = "main"
title = "Drag and drop"

+++
The animation implementation of drag-and-drop I wrote in kotlin.
This is a very easy and simple.

```
// from view
fromView.setOnTouchListener(View.OnTouchListener { view, event ->
    if (event.getAction() == MotionEvent.ACTION_DOWN) {
        val data = ClipData.newPlainText("", "")
        view.startDrag(data, View.DragShadowBuilder(view), view, View.DRAG_FLAG_GLOBAL)
        view.setVisibility(View.INVISIBLE)
        return@OnTouchListener true
    } else {
        return@OnTouchListener false
    }
})

// to view
toView.setOnDragListener(View.OnDragListener { view, event ->
    if (event.action == DragEvent.ACTION_DROP) {
        // do something for drop
        (event.localState as View).visibility = View.INVISIBLE
    } else if (event.action == DragEvent.ACTION_DRAG_ENDED) {
        val v = (event.localState as View)
        v.post({ v.visibility = View.VISIBLE })
    }
    return@OnDragListener true
})
```

