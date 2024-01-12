# android_development_roadmap


#  How to create a horizontal divider and import it inside a xml layout file in Android Studio

## Adding 1dp Horizontal Lines using <b>shape</b> element in Android Studio

## Create a <b>divider_line.xml</b> in the <b>Drawable</b> folder resource:
   - In the <b>res/drawable</b> directory, create a new XML file called <b>line_divider.xml</b> and paste this:

   ```xml
   <!-- res/drawable/divider_line.xml -->
   <shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">
       <size android:height="1dp" />
       <solid android:color="#000000" /> <!-- customize color -->
   </shape>

```

## Open(or create if it doesn't exist) your <b>fragment_login.xml</b> layout file and paste the following xml code:


```xml
<!-- fragment_login.xml -->
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center">


    <TextView
        android:id="@+id/logintext"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:gravity="center"
        android:padding="8dp"
        android:text="Login"
        android:textSize="30dp"
        android:textStyle="bold" />

<!-- we will edit this later -->

    <EditText
        android:id="@+id/username"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:hint="Username"
        android:padding="8dp" />

<!-- we will edit this later  -->

    <EditText
        android:id="@+id/password"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:hint="Password"
        android:padding="8dp" />

<!-- we will edit this later -->

    <Button
        android:id="@+id/loginButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:padding="8dp"
        android:text="Login" />

</LinearLayout>
```



## Reference the <b>shape</b> element from the <b>Drawable</b> folder in your <b>fragment_login.xml</b> layout file and paste the following xml code:

### Replace your <b>fragment_login.xml</b> layout file with the following content:

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center">

    <TextView
        android:id="@+id/logintext"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:gravity="center"
        android:padding="8dp"
        android:text="Login"
        android:textSize="30dp"
        android:textStyle="bold" />

    <!-- reference res/drawable/line_divider.xml -->
    <!-- Include the divider_line.xml drawable using the View element -->
    <View
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="@drawable/divider_line" />


    <EditText
        android:id="@+id/username"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:hint="Username"
        android:padding="18dp" />


    <!-- reference res/drawable/line_divider.xml -->
    <!-- Include the divider_line.xml drawable using the View element -->
    <View
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="@drawable/divider_line" />


    <EditText
        android:id="@+id/password"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:hint="Password"
        android:padding="18dp" />


    <!-- reference res/drawable/line_divider.xml -->
    <!-- Include the divider_line.xml drawable using the View element -->
    <View
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="@drawable/divider_line" />


    <Button
        android:id="@+id/loginButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:padding="8dp"
        android:text="Login" />


    <!-- reference res/drawable/line_divider.xml -->
    <!-- Include the divider_line.xml drawable using the View element -->
    <View
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="@drawable/divider_line" />

</LinearLayout>



```


## That's how youcan modify your <b>fragment_login.xml</b> to include the horizontal line using the <b>View</b> element:
