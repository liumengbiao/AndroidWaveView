
# 使用方法
1.在项目根目录下的build.gradle中 allprojects repositories 中添加  	maven { url 'https://jitpack.io' } 如下：
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  
2.在项目中的build.gradle中添加引用
dependencies {
		 compile 'com.github.chr1123:AndroidWaveView:V1.0.2'
	}


3.在布局文件中使用
   <com.chrischen.waveview.WaveView
        android:id="@+id/waveView"
        android:layout_width="match_parent"
        android:layout_height="100dp"
        android:background="#999"/>
        
4.代码中使用waveView.putValue(value)为波形图添加采集到的音量值，
  使用setHasOver(true)方法设置停止采集后，若采集点的展示超出了宽度，此时可左右滑动展示



添加了相关样式设置 ，可设置波形展示方式，线条宽度颜色间距等   如：
  <com.chrischen.waveview.WaveView
        android:id="@+id/waveView"
        android:layout_width="match_parent"
        android:layout_height="100dp"
        android:background="#999"
        app:wvType="centerLine"
        app:wvCenterLineColor="#f0f"
        app:wvCenterLineWidth="1dp"
        app:wvLineColor="#ff0"
        app:wvLineWidth="1dp"
        app:wvLineSpace="5dp"/>
