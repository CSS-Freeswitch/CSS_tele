## 代码变动

### 删除Logo

* build\Makefile.am 第4行：去掉安装时的freeswitch提示信息

```yaml
	......
	## delete@suy:2020-9-27
	## 
	## @echo " +---------- FreeSWITCH Build Complete ----------+"
	## @echo " + FreeSWITCH has been successfully built.       +"
	## @echo " + Install by running:                           +"
	......
	
	## create@suy:2020-9-27
	@echo " +---------------- Build Complete ---------------+"
	@echo " + successfully built.                           +"
	@echo " + Install by running:                           +"
	@echo " +                                               +"
	......
```
* build\Makefile.am 第33行：去掉安装时的freeswitch提示信息
```yaml
	......
	## delete@suy:2020-9-27
	## 
	## @echo " +---------- FreeSWITCH install Complete ----------+"
	## @echo " + FreeSWITCH has been successfully installed.     +"
	## @echo " +                                                 +"
	......

	## create@suy:2020-9-27
	@echo " +---------------- install Complete ---------------+"
	@echo " + successfully installed.                         +"
	@echo " +                                                 +"
	@echo " +       Install sounds:                           +"
	......
```
* libs\esl\fs_cli.c 第1044行：去掉了fs_cli的启动logo
```c
......
/*delete@suy:2020-9-27*/

// static const char *banner =
// 	".=======================================================.\n"
//     "|            _____ ____     ____ _     ___              |\n"
//     "|           |  ___/ ___|   / ___| |   |_ _|             |\n"
......

/*create@suy:2020-9-27*/
static const char *banner = "";
/*create@suy end*/
......
```
* libs\esl\src\include\cc.h 第1行：去掉了fs_cli的启动logo
```c
/*delete@suy:2020-9-27*/

// const char *cc = ".=======================================================================================================.\n"
//                  "|       _                            _    ____ _             ____                                       |\n"
//                  "|      / \\   _ __  _ __  _   _  __ _| |  / ___| |_   _  ___ / ___|___  _ __                             |\n"
//                  "|     / _ \\ | '_ \\| '_ \\| | | |/ _` | | | |   | | | | |/ _ \\ |   / _ \\| '_ \\                            |\n"
......

/*create@suy:2020-9-27*/
const char *cc = "";
const char *cc_s = "";
/*create@suy end*/
......
```
* src\switch_core.c 第2147行：去掉了freeswitch的logo以及网站信息
```c
	......
	/*delete@suy:2020-9-26*/
	
	// return ("\n"
	// 		".=============================================================.\n"
	// 		"|   _____              ______        _____ _____ ____ _   _   |\n"
	// 		"|  |  ___| __ ___  ___/ ___\\ \\      / /_ _|_   _/ ___| | | |  |\n"
	// 		"|  | |_ | '__/ _ \\/ _ \\___ \\\\ \\ /\\ / / | |  | || |   | |_| |  |\n"
	......
	
	/*create@suy:2020-9-26*/
	return ("");
	/*create@suy end*/
	......
```
* src\switch.c 第521行：去掉自动开启NAT功能
```c
	......
	/*delete@suy:2020-9-29*/
	// switch_core_flag_t flags = SCF_USE_SQL | SCF_USE_AUTO_NAT | SCF_USE_NAT_MAPPING | SCF_CALIBRATE_CLOCK | SCF_USE_CLOCK_RT;
	/*delete@suy end*/

	/*create@suy:2020-9-29*/
	switch_core_flag_t flags = SCF_USE_SQL | SCF_USE_NAT_MAPPING | SCF_CALIBRATE_CLOCK | SCF_USE_CLOCK_RT;
	/*create@suy end*/
	......
```
* src\include\cc.h 第1行：去掉了freeswitch的启动logo
```c
/*delete@suy:2020-9-26*/

// const char *cc = ".=======================================================================================================.\n"
//                  "|       _                            _    ____ _             ____                                       |\n"
//                  "|      / \\   _ __  _ __  _   _  __ _| |  / ___| |_   _  ___ / ___|___  _ __                             |\n"
//                  "|     / _ \\ | '_ \\| '_ \\| | | |/ _` | | | |   | | | | |/ _ \\ |   / _ \\| '_ \\                            |\n"
......

/*create@suy:2020-9-26*/
const char *cc = "";
const char *cc_s = "";
/*create@suy end*/
......
```
* src\mod\applications\mod_signalwire\mod_signalwire.c 第478行：去掉了signalwire的logo以及网站信息
```c
			/*delete@suy:2020-9-26*/

			// if (globals.adoption_token[0]) {
			// 	stream->write_function(stream,
			// 		"     _____ _                   ___       ___\n"
			// 		"    / ___/(_)___ _____  ____ _/ / |     / (_)_______\n"
			......
			
			/*create@suy:2020-9-26*/
			if (globals.adoption_token[0]) {
				stream->write_function(stream, "");
			} else {
				stream->write_function(stream, "-ERR connection token not available\n");
			}
			/*create@suy end*/
			......
```
* src\mod\applications\mod_signalwire\mod_signalwire.c 第983行：去掉了freeswitch的启动时signalwire的logo
```c
	......
	/*delete@suy:2020-9-26*/

	// switch_log_printf(SWITCH_CHANNEL_LOG, SWITCH_LOG_CONSOLE, "Welcome to\n"
	// "     _____ _                   ___       ___\n"
	// "    / ___/(_)___ _____  ____ _/ / |     / (_)_______\n"
	// "    \\__ \\/ / __ `/ __ \\/ __ `/ /| | /| / / / ___/ _ \\\n"
	......
```

### 更改默认配置

* conf\vanilla\vars.xml 第301行：将external_rtp_ip从stun:stun.freeswitch.org改为$${local_ip_v4} 
```xml
	......
	<!-- change@suy:2020-9-26 -->
	<X-PRE-PROCESS cmd="set" data="external_rtp_ip=$${local_ip_v4}"/>
	<!-- change@suy end -->
	......
```
* conf\vanilla\vars.xml 第318行：将external_sip_ip从stun:stun.freeswitch.org改为$${local_ip_v4}
```xml
	......
	<!-- change@suy:2020-9-26 -->
	<X-PRE-PROCESS cmd="set" data="external_sip_ip=$${local_ip_v4}"/>
	<!-- change@suy end -->
	......
```
* conf\vanilla\autoload_configs\modules.conf.xml 第53行：启动时不加载mod_signalwire模块
```xml
	......
    <!-- delete@suy:2020-9-28 -->
    <!-- <load module="mod_signalwire"/> -->
    <!-- delete end -->
    ......
```
* conf\vanilla\dialplan\default.xml 第136行：取消默认密码呼叫时的10秒延时
```xml
	......
	<!-- delete@suy:2020-9-30 -->
	<!-- <action application="sleep" data="10000"/> -->
	<!-- delete@suy end -->
	......
```
* conf\vanilla\sip_profiles\internal.xml 第233行：设置默认媒体绕过
```xml
	......
	<!-- recovery@suy:2020-9-30 -->
	<param name="inbound-bypass-media" value="true"/>
	<!-- recovery@suy end -->
	......
```