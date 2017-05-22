# homeassistant-HelpWeather
plugin of HelpWeather for home assistant.

##说明
------
文件基于 charleyzhu 的 https://github.com/charleyzhu/HomeAssistant_Components/blob/master/sensor/HeWeather.py 插件文件修改。<br>
调用帮天气免费接口，无需注册，仅需要确认，城市名称和编号即可。具体规则如下：<br>
空气质量接口：#AQI_TYPES #http://api.help.bj.cn/apis/aqi3/?id=beijing <br>
6天内天气预报接口：#DAY_FORECAST_TYPES #http://api.help.bj.cn/apis/weather6d/?id=101010100 <br>
36小时内天气预报接口：#HOUR_FORECAST_TYPE #http://api.help.bj.cn/apis/weather36h/?id=beijing <br>
当前天气情况接口：#NOW_FORECAST_TYPE #http://api.help.bj.cn/apis/weather/?id=101010100 <br>
27项生活建议接口：#SUGGESTION_FORECAST_TYPE #http://api.help.bj.cn/apis/life27/?id=北京 <br>

配置文件中需要配置，city、cityid、cityname，其它参数可选，配置文件可参见config目录内容。


## 示意图
------
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/ALL.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/1.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/2.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/3.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/4.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/5.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/6.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/7.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/8.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/9.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/10.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/11.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/12.png)
![Alt](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/warning.png)


## 城市编号、名称获取方法
------
首先登陆 http://www.help.bj.cn 网站，点击切换城市，选择你所在城市或区，如下图：
![Donation](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/changecity.png)

选择好城市或区后，到地址栏查看，如下图：
![Donation](https://raw.githubusercontent.com/MiracleLiuyx/home-assistant-HelpWeather/master/images/getid.png)
例如：http://www.help.bj.cn/weather/beijing/BJ010100/index.htm <br>
city获取方法：weather后的就是city需要填写的内容； <br>
cityid获取方法：city后面BJ010100，将数字 010100 提取出来，在最前面加上 101，即为你的cityid； <br>
cityname获取方法：第一步，你选择城市或区时，拷贝这个汉字即可，这里就是“北京” <br>

