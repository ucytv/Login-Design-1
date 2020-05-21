## Login-Design-1

This project consists of design only.  The design which follows the trends of 2020 includes a screen that can enter your application. The demo and source codes are shown following.

### Demo

![login_design_1_2](https://user-images.githubusercontent.com/37077627/82560923-09727480-9b7b-11ea-9049-bcebb3919112.png)


### Dependencies
```
implementation 'com.google.android.material:material:1.1.0'
```

### Style & Theme
```
 <style name="LoginTheme" parent="Theme.MaterialComponents.Light.NoActionBar.Bridge">
        <item name="colorPrimary">@color/colorMain</item>
        <item name="colorPrimaryDark">@color/colorDark</item>
        <item name="colorAccent">@color/colorLight</item>
 </style>
```

### Color
```
<color name="colorMain">#222020</color>
<color name="colorDark">#4A474C</color>
<color name="colorLight">#FFFFFF</color>
```

### Layout Style

*for dark layout:*
```
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <shape android:shape="rectangle">
            <corners android:topLeftRadius="12dp" android:topRightRadius="12dp" />
            <solid android:color="@color/colorMain" />
        </shape>
    </item>
</selector>
```

*for light layout:*
```
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <shape android:shape="rectangle">
            <corners android:topLeftRadius="12dp" android:topRightRadius="12dp" />
            <solid android:color="@color/colorLight" />
        </shape>
    </item>
</selector>
```

### String
```
<resources>
    <string name="app_name">LoginDesign1</string>
    <string name="login">Login</string>
    <string name="message">Follow your passions!</string>
    <string name="nickname">Nickname</string>
    <string name="password">Password</string>
    <string name="remember_me">Remember Me</string>
    <string name="forgot_password">Forgot Password</string>
    <string name="login_caps">LOGIN</string>
    <string name="register">Do you want to join us?</string>
</resources>
```

### XML File
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:theme="@style/LoginTheme"
    android:background="@color/colorMain"
    tools:context=".MainActivity">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:paddingLeft="30dp"
        >

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="start"
            android:layout_marginTop="20dp"
            android:fontFamily="@font/architects_daughter"
            android:gravity="center"
            android:layout_marginStart="12dp"
            android:paddingTop="40dp"
            android:paddingEnd="40dp"
            android:paddingBottom="40dp"
            android:text="@string/login"
            android:textAllCaps="false"
            android:textColor="@color/colorLight"
            android:textSize="40sp"
            android:textStyle="bold" />

        <RelativeLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            >

            <TextView
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_gravity="center"
                android:layout_marginStart="12dp"
                android:fontFamily="@font/architects_daughter"
                android:gravity="center"
                android:layout_marginTop="12dp"
                android:text="@string/message"
                android:textAllCaps="false"
                android:textColor="@color/colorLight"
                android:textSize="22sp"
                android:textStyle="normal" />

            <ImageView
                android:layout_width="100dp"
                android:layout_height="100dp"
                android:src="@drawable/yaman_new"
                android:layout_alignParentEnd="true"/>

        </RelativeLayout>

    </LinearLayout>


    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical"
        android:padding="40dp"
        android:background="@drawable/layout_style_white">
        
        <com.google.android.material.textfield.TextInputLayout
            android:id="@+id/text_input_nick"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
            android:hint="@string/nickname"
            app:hintTextColor="@color/colorDark"
            app:boxStrokeWidthFocused="2dp"
            app:startIconDrawable="@drawable/icon_person_black_24"
            app:endIconMode="clear_text"
            app:endIconTint="@color/colorMain"
            app:startIconTint="@color/colorMain"
            android:fontFamily="@font/architects_daughter"
            >

            <com.google.android.material.textfield.TextInputEditText
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:textColor="@color/colorMain"
                android:id="@+id/edit_input_nick"
                android:padding="16dp"
                android:fontFamily="@font/architects_daughter"
                />
        </com.google.android.material.textfield.TextInputLayout>

        <com.google.android.material.textfield.TextInputLayout
            android:id="@+id/text_input_pass"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
            android:hint="@string/password"
            app:hintTextColor="@color/colorDark"
            app:boxStrokeColor="@color/colorMain"
            android:layout_marginTop="12dp"
            app:boxStrokeWidthFocused="2dp"
            app:startIconDrawable="@drawable/icon_pass_black_24"
            app:endIconMode="password_toggle"
            app:endIconTint="@color/colorMain"
            app:startIconTint="@color/colorMain"
            >
            
            <com.google.android.material.textfield.TextInputEditText
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:id="@+id/edit_input_pass"
                android:textColor="@color/colorMain"
                android:inputType="numberPassword"
                android:padding="16dp"
                app:boxStrokeColor="@color/colorMain"
                android:fontFamily="@font/architects_daughter"
                />
        </com.google.android.material.textfield.TextInputLayout>

        <RelativeLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"            >

            <CheckBox
                android:id="@+id/checkbox_remember"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="@string/remember_me"
                android:buttonTint="@color/colorMain"
                android:textColor="@color/colorMain"
                android:layout_marginTop="8dp"
                android:layout_centerVertical="true"
                android:layout_marginEnd="2dp"
                android:textSize="14sp"
                android:fontFamily="@font/architects_daughter"
                style="@style/Widget.AppCompat.CompoundButton.CheckBox"/>

            <Button
                android:id="@+id/button_forgot"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="@string/forgot_password"
                android:textAllCaps="false"
                android:background="@color/colorLight"
                android:layout_alignParentEnd="true"
                android:textSize="14sp"
                android:fontFamily="@font/architects_daughter"
                />
        </RelativeLayout>

        <Button
            android:id="@+id/button_login"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="20dp"
            android:background="@color/colorMain"
            android:text="@string/login_caps"
            android:textAllCaps="true"
            android:fontFamily="@font/architects_daughter"
            android:textColor="@color/colorLight" />

        <Button
            android:id="@+id/button_register"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="@string/register"
            android:textAllCaps="false"
            android:background="@color/colorLight"
            android:gravity="center"
            android:layout_gravity="center"
            android:layout_marginTop="10dp"
            android:textSize="14sp"
            android:fontFamily="@font/architects_daughter"
            />
    </LinearLayout>
</LinearLayout>
```
