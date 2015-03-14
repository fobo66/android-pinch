# android-pinch
Automatically exported from code.google.com/p/android-pinch

# About #

Adds multi-touch zoom to; ImageViews, WebViews, and MapViews. Simply use the corresponding object in place of the default, and the "pinch" functionality will be usable. Also includes misc. Views which can be useful for development.

# Getting Started #

For more information on how to implement he pinch views, check out the [Wiki](https://github.com/fobo66/android-pinch/wiki/PinchImageView).

## Quick Example ##

**XML Layout**
```
 <?xml version="1.0" encoding="utf-8"?>
 <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    android:isScrollContainer="true"
    >
    <com.nikkoaiello.mobile.android.PinchMapView
        android:id="@+id/map"
        android:layout_width="fill_parent"
        android:layout_height="fill_parent"
        android:clickable="true"
        android:apiKey="YOUR_API_KEY"
    />
    
 </RelativeLayout>
```

**Activity Class**
```
  ...  

  public class PinchMapActivity extends MapActivity {
	
    PinchMapView view;
	
	/** Called when the activity is first created. */
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.mapview);
        
        view = (PinchMapView) findViewById(R.id.map);
    }

    protected boolean isRouteDisplayed() {
	return false;
    }
  
    ...
  }
```

The only thing left to do is run your activity.

### Questions? ###

send me an e-mail @ nikko.aiello@gmail.om
