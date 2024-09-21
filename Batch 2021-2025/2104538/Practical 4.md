## Practical 4. Android User Interface Design: To implement different type of layouts like relative, grid, linear and table.

### A) Develop a program to implement constraint layout to display Hello World on screen.

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/constraintLayout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#FFEBEE"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World"
        android:textSize="24sp"
        android:textColor="@android:color/black"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

![pr4](https://github.com/user-attachments/assets/b9d7a44b-2985-4202-8549-302e043bf46b)

### B) Develop a program to implement linear layout.

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/linearLayout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="16dp"
    android:background="#F5F5F5">  <!-- Light grey background -->

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Welcome to Linear Layout"
        android:textSize="24sp"
        android:textStyle="bold"
        android:textColor="#000000"
        android:padding="16dp" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Click Me"
        android:textColor="#FFFFFF"
        android:backgroundTint="#6200EE"
        android:padding="12dp" />

</LinearLayout>
```
![WhatsApp Image 2024-08-30 at 12 07 45_693c4a41](https://github.com/user-attachments/assets/cee38f56-4cef-499a-a3a2-5ac15ce95b57)


