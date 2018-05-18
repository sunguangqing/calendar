### 订单查询 酒店入住 日历选择功能

https://sunguangqing.github.io/calendar/calendar.html

### My97DatePicker日期控件地址：http://www.my97.net/demo/index.htm

>下载calendar文件夹放到根目录中，将WdatePicker.js文件引用到页面中即可, <script src="calendar/WdatePicker.js"></script>

#### `HTML结构：`
##### >订单查询日历控件使用 
>可选择的时间不能超过当前的时间，后面选择框的时间不能小于前面选定的时间并且不能大于当前的时间
```HTML
<div class="date-btn">
    <input id="start-time"  onclick="WdatePicker({maxDate:'%y-%M-%d'})" /> ~
    <input onclick="WdatePicker({minDate:'#F{$dp.$D(\'start-time\',{d:0});}',maxDate:'%y-%M-%d'})" />
    <span class="wdate-icon"></span>
</div>
```

#### >酒店入驻日历控件使用
>可选的时间不能小于当前的时间，后面选择框的时间不能小于当前的时间加一天并且不能大于商家设定的时间
```HTML
<div class="date-btn">
    <input type="text" class="Wdate" id="start-time-hotel" onclick="WdatePicker({skin:'whyGreen', minDate:'%y-%M-%d', maxDate:'2050-12-12'})"/> ~
    <input type="text" class="Wdate" onclick="WdatePicker({skin:'whyGreen', minDate: '#F{$dp.$D(\\\'start-time-hotel\\\',{d:1});}'})"/>
    <span class="wdate-icon"></span>
</div>
```


#### `CSS代码：`
```CSS
.date-btn{
    width: 255px;
    height: 30px;
    line-height: 30px;
    border: 1px solid #d9d9d9;
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    border-radius: 4px;
    margin-left: 18px;
    padding: 0 18px;
}
.date-btn input{
    position: relative;
    top: -2px;
    width: 90px;
    height: 28px;
    border: 0;
    text-align: center;
    color: #777;
}
.date-btn .wdate-icon{
    float: right;
    width: 14px;
    height: 14px;
    background: url("../images/data-icon.png") no-repeat center center;
    margin-top: 8px;
}
```
