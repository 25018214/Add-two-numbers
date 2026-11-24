# Add-two-numbers
## WORKSHOP -ADDITION OF TWO NUMBERS
## Aim:
To create and design an android application for a addition of two numbers using android studio.
## EQUIPMENTS REQUIRED:
Android Studio(Latest Version)
## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as smsintent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6:Display details give in MainActivity file.

Step 7: Save and run the application.
## PROGRAM:
Program to create and design an android application simple calculator using Intent.
### Developed by: AKASH A
### Registration Number : 212225230008

# activity_main.xml
```


<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="25dp"
    android:background="#E3F2FD">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Addition of Two Numbers"
        android:textSize="25sp"
        android:textStyle="bold"
        android:textColor="#1565C0"
        android:layout_marginBottom="30dp"/>

    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter First Number"
        android:inputType="numberDecimal|numberSigned"/>

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Second Number"
        android:inputType="numberDecimal|numberSigned"
        android:layout_marginTop="15dp"/>

    <Button
        android:id="@+id/addButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="ADD"
        android:layout_marginTop="25dp"
        android:backgroundTint="#1565C0"/>

    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Result: "
        android:textSize="23sp"
        android:textStyle="bold"
        android:textColor="#2E7D32"
        android:layout_marginTop="25dp"/>

</LinearLayout>
```
#MainActivity.java
```

package com.example.additionapp;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button addButton;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        addButton = findViewById(R.id.addButton);
        result = findViewById(R.id.result);

        addButton.setOnClickListener(v -> {

            String a = num1.getText().toString();
            String b = num2.getText().toString();

            if (a.isEmpty() || b.isEmpty()) {
                Toast.makeText(this,
                        "Please enter both numbers",
                        Toast.LENGTH_SHORT).show();
                return;
            }

            double n1 = Double.parseDouble(a);
            double n2 = Double.parseDouble(b);

            double sum = n1 + n2;

            result.setText("Result: " + sum);
        });
    }
}
```

### output
![alt text](<Screenshot 2026-11-24 084523.png>)

![alt text](<Screenshot 2026-11-24 084535.png>)

![alt text](<Screenshot 2026-11-24 084608.png>)

## RESULT
Thus a Simple Android Application create a addition of two numbers using Android Studio is developed and executed successfully.
