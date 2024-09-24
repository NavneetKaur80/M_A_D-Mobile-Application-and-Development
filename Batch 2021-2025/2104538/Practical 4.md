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
![4a](https://github.com/user-attachments/assets/9b70474f-67ef-4a3c-b83e-79b481a6876a)

### B) Develop a program to implement linear layout to display send message and registration form (vertical and horizontal)

```xml
<com.google.android.material.textfield.TextInputLayout
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginBottom="10dp"
    app:hintTextColor="@color/your_hint_color"
    app:boxStrokeColor="@color/red"   <!-- This sets the color of the underline -->
    app:boxStrokeErrorColor="@color/red" <!-- This sets the color of the underline when there's an error -->

    <!-- Optional: Customize other styles -->
    app:boxBackgroundMode="outline">
    
    <EditText
        android:id="@+id/toField"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="To"
        android:inputType="textEmailAddress"
        android:padding="10dp" />
    
</com.google.android.material.textfield.TextInputLayout>

```

![4b](https://github.com/user-attachments/assets/21f5c929-a35a-41f5-941f-852237483534)


### C) Develop a program to implement relative layout to display Login and sign up form.

```xml
<RelativeLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#0078FF"> <!-- Light blue background -->

    <!-- Login Form -->
    <LinearLayout
        android:id="@+id/login_layout"
        android:layout_width="157dp"
        android:layout_height="482dp"
        android:layout_alignParentLeft="true"
        android:layout_centerVertical="true"
        android:layout_marginLeft="15dp"
        android:layout_marginTop="50dp"
        android:background="#FFFFFF"
        android:elevation="8dp"
        android:orientation="vertical"
        android:padding="16dp">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center_horizontal"
            android:text="Login"
            android:textColor="#000000"
            android:textSize="24sp"
            android:textStyle="bold" />

        <EditText
            android:id="@+id/editTextEmailLogin"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="16dp"
            android:backgroundTint="#D3D3D3"
            android:hint="Email"
            android:inputType="textEmailAddress"
            android:textColor="#000000"
            android:textColorHint="#A9A9A9" />

        <EditText
            android:id="@+id/editTextPasswordLogin"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:backgroundTint="#D3D3D3"
            android:hint="Password"
            android:inputType="textPassword"
            android:textColor="#000000"
            android:textColorHint="#A9A9A9" />

        <TextView
            android:id="@+id/forgotPassword"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center_horizontal"
            android:layout_marginTop="8dp"
            android:text="Forgot password?"
            android:textColor="#0078FF" />

        <Button
            android:id="@+id/buttonLogin"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="16dp"
            android:backgroundTint="#0078FF"
            android:text="Login"
            android:textColor="#FFFFFF" />

        <!-- Social Login Options for Login -->
        <TextView
            android:id="@+id/loginOrSeparator"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center_horizontal"
            android:layout_marginTop="16dp"
            android:text="Or"
            android:textColor="#A9A9A9" />

        <Button
            android:id="@+id/buttonLoginFacebook"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:backgroundTint="#4267B2"
            android:drawableStart="@drawable/fb"
            android:text="Continue with Facebook"
            android:textColor="#FFFFFF" />

        <Button
            android:id="@+id/buttonLoginGoogle"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:backgroundTint="#DB4437"
            android:drawableStart="@drawable/google"
            android:text="Continue with Google"
            android:textColor="#FFFFFF" />

    </LinearLayout>

    <!-- Signup Form -->
    <LinearLayout
        android:id="@+id/signup_layout"
        android:layout_width="156dp"
        android:layout_height="483dp"
        android:layout_alignParentRight="true"
        android:layout_centerVertical="true"
        android:layout_marginTop="50dp"
        android:layout_marginRight="10dp"
        android:background="#FFFFFF"
        android:elevation="8dp"
        android:orientation="vertical"
        android:padding="16dp">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center_horizontal"
            android:text="Signup"
            android:textColor="#000000"
            android:textSize="24sp"
            android:textStyle="bold" />

        <EditText
            android:id="@+id/editTextEmailSignup"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="16dp"
            android:backgroundTint="#D3D3D3"
            android:hint="Email"
            android:inputType="textEmailAddress"
            android:textColor="#000000"
            android:textColorHint="#A9A9A9" />

        <EditText
            android:id="@+id/editTextPasswordSignup"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:backgroundTint="#D3D3D3"
            android:hint="Create password"
            android:inputType="textPassword"
            android:textColor="#000000"
            android:textColorHint="#A9A9A9" />

        <EditText
            android:id="@+id/editTextConfirmPasswordSignup"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:backgroundTint="#D3D3D3"
            android:hint="Confirm password"
            android:inputType="textPassword"
            android:textColor="#000000"
            android:textColorHint="#A9A9A9" />

        <Button
            android:id="@+id/buttonSignup"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="16dp"
            android:backgroundTint="#0078FF"
            android:text="Signup"
            android:textColor="#FFFFFF" />

        <!-- Social Signup Options -->
        <TextView
            android:id="@+id/signupOrSeparator"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center_horizontal"
            android:layout_marginTop="16dp"
            android:text="Or"
            android:textColor="#A9A9A9" />

        <Button
            android:id="@+id/buttonSignupFacebook"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:backgroundTint="#4267B2"
            android:drawableStart="@drawable/fb"
            android:text="Continue with Facebook"
            android:textColor="#FFFFFF" />

        <Button
            android:id="@+id/buttonSignupGoogle"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:backgroundTint="#DB4437"
            android:drawableStart="@drawable/google"
            android:text="Continue with Google"
            android:textColor="#FFFFFF" />
    </LinearLayout>
</RelativeLayout>

```

![4c](https://github.com/user-attachments/assets/4086a621-ce39-4bc5-8987-a4df5a46ea46)

### D) Develop a program to implement table layout to display calculator.


