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

### B) Develop a program to implement linear layout to display send message and registration form (vertical and horizontal)

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/linearLayout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp"
    android:background="#F0F0F0"> <!-- Light background for simplicity -->

    <!-- Send Message Section -->
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Send Message"
        android:textSize="20sp"
        android:textStyle="bold"
        android:textColor="@color/black"
        android:paddingBottom="8dp" />

    <EditText
        android:id="@+id/messageInput"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Type your message here"
        android:padding="12dp"
        android:background="@android:drawable/editbox_background"
        android:layout_marginBottom="8dp" />

    <Button
        android:id="@+id/sendButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Send"
        android:backgroundTint="#6200EE"
        android:textColor="#FFFFFF"
        android:padding="12dp" />

    <!-- Divider Line -->
    <View
        android:layout_width="match_parent"
        android:layout_height="2dp"
        android:layout_marginTop="24dp"
        android:layout_marginBottom="24dp"
        android:background="#CCCCCC" />

    <!-- Registration Form Section -->
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Registration Form"
        android:textSize="20sp"
        android:textStyle="bold"
        android:textColor="@color/black"
        android:paddingBottom="8dp" />

    <!-- Name Field (Horizontal Layout) -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:layout_marginBottom="8dp">

        <TextView
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="Name"
            android:textColor="@color/black"
            android:padding="8dp" />

        <EditText
            android:id="@+id/nameInput"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="2"
            android:hint="Enter your name"
            android:padding="12dp"
            android:background="@android:drawable/editbox_background" />
    </LinearLayout>

    <!-- Email Field (Horizontal Layout) -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:layout_marginBottom="8dp">

        <TextView
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="Email"
            android:textColor="@color/black"
            android:padding="8dp" />

        <EditText
            android:id="@+id/emailInput"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="2"
            android:hint="Enter your email"
            android:padding="12dp"
            android:inputType="textEmailAddress"
            android:background="@android:drawable/editbox_background" />
    </LinearLayout>

    <!-- Phone Field (Horizontal Layout) -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:layout_marginBottom="16dp">

        <TextView
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="Phone"
            android:textColor="@color/black"
            android:padding="8dp" />

        <EditText
            android:id="@+id/phoneInput"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="2"
            android:hint="Enter your phone number"
            android:padding="12dp"
            android:inputType="phone"
            android:background="@android:drawable/editbox_background" />
    </LinearLayout>

    <Button
        android:id="@+id/registerButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Register"
        android:backgroundTint="#6200EE"
        android:textColor="#FFFFFF"
        android:padding="12dp" />

</LinearLayout>

```
![WhatsApp Image 2024-08-30 at 12 07 45_693c4a41](https://github.com/user-attachments/assets/cee38f56-4cef-499a-a3a2-5ac15ce95b57)


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



