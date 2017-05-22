# homeassistant-HelpWeather
plugin of HelpWeather for home assistant.

#说明
文件基于 charleyzhu 的 https://github.com/charleyzhu/HomeAssistant_Components/blob/master/sensor/HeWeather.py 插件文件修改。
调用帮天气免费接口，无需注册，仅需要确认，城市名称和编号即可。具体规则如下：
空气质量接口：#AQI_TYPES #http://api.help.bj.cn/apis/aqi3/?id=beijing
6天内天气预报接口：#DAY_FORECAST_TYPES #http://api.help.bj.cn/apis/weather6d/?id=101010100
36小时内天气预报接口：#HOUR_FORECAST_TYPE #http://api.help.bj.cn/apis/weather36h/?id=beijing
当前天气情况接口：#NOW_FORECAST_TYPE #http://api.help.bj.cn/apis/weather/?id=101010100
27项生活建议接口：#SUGGESTION_FORECAST_TYPE #http://api.help.bj.cn/apis/life27/?id=北京

配置文件中需要配置，city、cityid、cityname，其它参数可选，配置文件可参见config目录内容。
