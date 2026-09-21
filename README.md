# ADDITION-OF-TWO-NUMBERS
Develop a program to get two values and display the summation value in the text box using Android Studio.
Aim:
  To create and design an Android application that accepts two values from the user and displays their summation value in a text box using Android Studio.
EQUIPMENTS REQUIRED:
    Android Studio (Latest Version)
    Android Emulator or Android Device
ALGORITHM:
```
Step 1: Open Android Studio and then click on File -> New -> New Project.

Step 2: Enter the Application name as SumApp and click Next.

Step 3: Select the Minimum SDK as required and click Next.

Step 4: Select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design the user interface in activity_main.xml with two EditText fields, one Button, and one result EditText.

Step 6: Write the Java code in the MainActivity.java file to get two values from the EditText fields.

Step 7: Convert the entered values into integers and calculate their sum.

Step 8: Display the calculated summation value in the result text box.

Step 9: Save and run the application.
```
 PROGRAM:
 Program to create and design an Android application to get two values and display the summation value in a text box using Android Studio.
 Developed by: Sandhiya sree b
Registration Number: 212223220093
  Activity_main.xml:
  ```
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="30dp">

    <EditText
        android:id="@+id/etValue1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first value"
        android:inputType="number" />

    <EditText
        android:id="@+id/etValue2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="15dp"
        android:hint="Enter second value"
        android:inputType="number" />

    <Button
        android:id="@+id/btnAdd"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="20dp"
        android:text="ADD" />

    <EditText
        android:id="@+id/etResult"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="20dp"
        android:hint="Result"
        android:inputType="number"
        android:focusable="false" />

</LinearLayout>
```
MainActivity.java
```
package com.example.sumapp;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText etValue1, etValue2, etResult;
    Button btnAdd;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        etValue1 = findViewById(R.id.etValue1);
        etValue2 = findViewById(R.id.etValue2);
        etResult = findViewById(R.id.etResult);
        btnAdd = findViewById(R.id.btnAdd);

        btnAdd.setOnClickListener(v -> {

            String value1 = etValue1.getText().toString();
            String value2 = etValue2.getText().toString();

            if (value1.isEmpty() || value2.isEmpty()) {
                etResult.setText("Enter both values");
                return;
            }

            int num1 = Integer.parseInt(value1);
            int num2 = Integer.parseInt(value2);

            int sum = num1 + num2;

            etResult.setText(String.valueOf(sum));
        });
    }
}
```
OUTPUT:
<img width="1919" height="1022" alt="image" src="https://github.com/user-attachments/assets/3cf5c0ad-43a7-4d00-aa8c-50c2ebe9741e" />
<img width="1919" height="1016" alt="image" src="https://github.com/user-attachments/assets/9fa1dc29-37b0-4008-9469-b03e7f050534" />
RESULT:
Thus, the Android application to get two values from the user and display their summation value in a text box was developed and executed successfully using Android Studio.

