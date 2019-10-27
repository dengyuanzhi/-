# Notes 

## java中获取系统的当前时间

### 获取当前系统时间和日期并格式化输出：
```JAVA
import java.util.Date; 
import java.util.Calendar; 

import java.text.SimpleDateFormat; 

public class TestDate{ 
public static void main(String[] args){ 
Date now = new Date(); 
SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");//可以方便地修改日期格式

String hehe = dateFormat.format( now ); 
System.out.println(hehe); 

Calendar c = Calendar.getInstance();//可以对每个时间域单独修改
 

int year = c.get(Calendar.YEAR); 
int month = c.get(Calendar.MONTH); 
int date = c.get(Calendar.DATE); 
int hour = c.get(Calendar.HOUR_OF_DAY); 
int minute = c.get(Calendar.MINUTE); 
int second = c.get(Calendar.SECOND); 
System.out.println(year + "/" + month + "/" + date + " " +hour + ":" +minute + ":" + second); 
} 
}
 有时候要把String类型的时间转换为Date类型，通过以下的方式，就可以将你刚得到的时间字符串转换为Date类型了。
SimpleDateFormat sdf=new SimpleDateFormat("yyyy-MM-dd");
java.util.Date time=null;
try {
   time= sdf.parse(sdf.format(new Date()));
} catch (ParseException e) {

   e.printStackTrace();
}```


```