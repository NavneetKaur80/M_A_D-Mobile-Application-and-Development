## Practical 5. To incorporate element of interactivity using Android Fragment and Intent Class

### activity_main.xml 

```xml
<?xml version="1.0" encoding="utf-8"?>
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/fragment_container"
    android:layout_width="match_parent"
    android:layout_height="match_parent" />

```
### fragment_a.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:orientation="vertical">

    <Button
        android:id="@+id/send_button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Send to FragmentB" />
</LinearLayout>

```
### fragment_b.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<!-- fragment_b.xml -->
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:orientation="vertical">

    <TextView
        android:id="@+id/received_data"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Data from FragmentA" />
</LinearLayout>

```
### MainActivity.java

```java
package com.example.my_exp5;

import android.content.Intent;
import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;
import androidx.fragment.app.Fragment;
import androidx.fragment.app.FragmentManager;

public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Load FragmentA initially
        if (savedInstanceState == null) {
            FragmentManager fragmentManager = getSupportFragmentManager();
            fragmentManager.beginTransaction()
                    .replace(R.id.fragment_container, new FragmentA())
                    .commit();
        }
    }

    // Method to switch to FragmentB
    public void switchToFragmentB(String data) {
        FragmentB fragmentB = new FragmentB();
        Bundle bundle = new Bundle();
        bundle.putString("data_key", data);  // Passing data to FragmentB
        fragmentB.setArguments(bundle);

        getSupportFragmentManager().beginTransaction()
                .replace(R.id.fragment_container, fragmentB)
                .addToBackStack(null)  // Allows to go back to FragmentA
                .commit();
    }
}

```
### FragmentA.java

```java
package com.example.my_exp5;

import android.content.Context;
import android.os.Bundle;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.Button;
import androidx.annotation.NonNull;
import androidx.annotation.Nullable;
import androidx.fragment.app.Fragment;

public class FragmentA extends Fragment {

    private MainActivity mainActivity;

    @Override
    public void onAttach(@NonNull Context context) {
        super.onAttach(context);
        mainActivity = (MainActivity) context;
    }

    @Nullable
    @Override
    public View onCreateView(@NonNull LayoutInflater inflater, @Nullable ViewGroup container, @Nullable Bundle savedInstanceState) {
        View view = inflater.inflate(R.layout.fragment_a, container, false);

        Button sendButton = view.findViewById(R.id.send_button);
        sendButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // Switch to FragmentB with some data
                mainActivity.switchToFragmentB("Hello from FragmentA");
            }
        });

        return view;
    }
}

```
### FragmentB.java

```java
package com.example.my_exp5;

import android.os.Bundle;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.TextView;
import androidx.annotation.NonNull;
import androidx.annotation.Nullable;
import androidx.fragment.app.Fragment;

public class FragmentB extends Fragment {

    @Nullable
    @Override
    public View onCreateView(@NonNull LayoutInflater inflater, @Nullable ViewGroup container, @Nullable Bundle savedInstanceState) {
        View view = inflater.inflate(R.layout.fragment_b, container, false);

        TextView textView = view.findViewById(R.id.received_data);

        // Retrieve data from FragmentA
        Bundle bundle = getArguments();
        if (bundle != null) {
            String data = bundle.getString("data_key");
            textView.setText(data);  // Displaying the received data
        }

        return view;
    }
}

```
![exp5a](https://github.com/user-attachments/assets/312e9eb0-bf18-4770-aa3c-9e2a35306ef5)

![exp5b](https://github.com/user-attachments/assets/c7ea5d28-6eea-4b86-a701-3ad63ac483dc)

