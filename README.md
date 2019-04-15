# This is the AndroidExample4_setting about PreferenceFragment
---
### the key codes: **preference.xml**

```
<?xml version="1.0" encoding="utf-8"?>
<PreferenceScreen xmlns:android="http://schemas.android.com/apk/res/android">
    <PreferenceCategory
        android:title="in-line preference"
        android:key="pre_key1">
        <CheckBoxPreference
            android:key="check_box"
            android:title="CheckBox preference"
            android:summary="This is a checkbox"
            android:defaultValue="false"
            android:enabled="true"/>
    </PreferenceCategory>
    <PreferenceCategory
        android:title="Dialog-based preference"
        android:key="pre_key2">
        <EditTextPreference
            android:key="edit_text"
            android:title="Edit text preference"
            android:summary="An example that uses a edit text dialog">
        </EditTextPreference>

        <ListPreference
            android:key="list"
            android:title="List preference"
            android:summary="An example that uses a list dialog"
            android:entries="@array/list_entries"
            android:entryValues="@array/list_entries_values"
            android:dialogTitle="Choose One"/>
    </PreferenceCategory>
    <PreferenceCategory
        android:title="Launch preference"
        android:key="pre_key3">
        <PreferenceScreen
            android:title="Screen preference"
            android:key="pre_screen1"
            android:summary="Shows another screen of preference">
            <CheckBoxPreference
                android:title="Toggle preference"
                android:summary="Preference that is on the next screen"
                android:key="sub_pre_screen1">

            </CheckBoxPreference>
        </PreferenceScreen>
        <PreferenceScreen
            android:title="Intent preference"
            android:key="pre_screen2"
            android:summary="Launch an Activity from an Intent">
            <Preference android:title="newWeb" >
                <intent android:action="android.intent.action.VIEW"
                    android:data="http://www.baidu.com" />
            </Preference>
        </PreferenceScreen>
    </PreferenceCategory>
    <PreferenceCategory
        android:title="Preference attributes"
        android:key="pre_key4">
        <CheckBoxPreference
            android:title="Parent checkbox preference"
            android:key="checkbox_parent"
            android:summary="This is a visual parent">

        </CheckBoxPreference>
        <CheckBoxPreference
            android:dependency="checkbox_parent"
            android:title="Child checkbox preference"
            android:key="checkbox_child"
            android:summary="This is a visual child">
        </CheckBoxPreference>
    </PreferenceCategory>

</PreferenceScreen>
```
### Screenshots
![PreferenceFragmentTest](https://img-blog.csdnimg.cn/20190415121118420.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MTMxNTI5NA==,size_16,color_FFFFFF,t_70 "PreferenceFragmentTest")

---
![EditTexrPreference](https://img-blog.csdnimg.cn/20190415121325531.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MTMxNTI5NA==,size_16,color_FFFFFF,t_70 "EditTextPreferenceTest")

---
![ListPreference](https://img-blog.csdnimg.cn/20190415121459753.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MTMxNTI5NA==,size_16,color_FFFFFF,t_70 "ListPreferenceTest")

---
![PreferenceScreenTest](https://img-blog.csdnimg.cn/20190415121539109.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MTMxNTI5NA==,size_16,color_FFFFFF,t_70 "PreferenceScreenTest")

---
![IntentPreference](https://img-blog.csdnimg.cn/20190415121621133.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MTMxNTI5NA==,size_16,color_FFFFFF,t_70 "IntentPreferenceTest")

---
![Dependency](https://img-blog.csdnimg.cn/2019041512170536.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MTMxNTI5NA==,size_16,color_FFFFFF,t_70 "PreferenceAttributesTest")
