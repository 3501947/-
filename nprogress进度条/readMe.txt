将 js  css  引入文本中 
在script中以NProgress.start(); 开始 以NProgress.done() ;结束
在ajax中NProgress.start();写在beforeSend：function（）｛｝中 
NProgress.done()写在complete：function（）｛｝中 不写在success成功回调函数中 因为不管请求失败与成功都要结束他

注册ajax全局事件
$（document）.ajaxStart（function（）｛

	NProgress。start（）

｝）

$（document）.ajaxStop（function（）｛

	NProgress.done

｝）