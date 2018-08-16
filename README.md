# KRScrollView
The dafault behavior of UIScrollView is to keep the same content offset when the size of your scroll view changes (i.e device orientation changes, animations, scroll view zooming). For example, if you have a scroll view with a content size of (100, 100) and a content offset of (10, 10), if the content size changes to (1000, 1000), the content offset will remain (10, 10). This becomes a problem when you want to maintant the context of what the user was looking at before the size change. The new content offset should be (100, 100), relative to the new size. KRScrollView solves this by saving the content offset as a ratio of the content size, which can then be used to restore the scroll view to the correct content offset by calling `determineNewContentOffset(ratio:)`
