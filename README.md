# Android-Notes

1.解决listview嵌套gridview后始终相应的是gridview的onclick
```
gv.setClickable(false);
gv.setPressed(false);
gv.setEnabled(false);
```

2.解决Android中,禁止ScrollView内的控件改变之后自动滚动
```
<ScrollView  
        android:id="@+id/sv"  
        android:layout_width="match_parent"  
        android:layout_height="match_parent" >  
  
        <LinearLayout  
            android:layout_width="match_parent"  
            android:layout_height="match_parent"  
            android:orientation="vertical"
            android:focusable="true"  
            android:focusableInTouchMode="true"      >  
            
<!-- 上面这两行是控制scrollview   
            android:focusable="true"  
            android:focusableInTouchMode="true"     
不自动的关键！ !-->  
                <ListView  
                    android:id="@+id/lv"  
                    android:layout_marginTop="5dp"  
                    android:layout_width="match_parent"  
                    android:layout_height="match_parent">  
  
                </ListView>  
  
        </LinearLayout>  
</ScrollView>  
```
