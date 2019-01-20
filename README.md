# JAVAtext
多线程，
并发及线程基础数据类型转换的基本原则
垃圾回收（GC）
Java 集合框架
数组
字符串GOF 设计模式
SOLID （单一功能、开闭原则、里氏替换、接口隔离以及依赖反转）设计原则
抽象类与接口
Java 基础，如 equals 和 hashcode泛型与枚举
Java IO 与 NIO
常用网络协议
Java 中的数据结构和算法正则表达式
JVM 底层
Java 最佳实践
JDBC
Date, Time 与 Calendar
Java 处理 XML
JUnit编程
  知乎链接： https://www.zhihu.com/collection/315103478
 
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<%@ page pageEncoding="gbk" %>
<html>
  <head>
    <title>个人信息收集</title>
	 <meta http-equiv="pragma" content="no-cache">
	 <meta http-equiv="cache-control" content="no-cache">
	 <meta http-equiv="expires" content="0">    
	 <meta http-equiv="keywords" content="个人,信息,收集">
	 <meta http-equiv="description" content="个人信息">
  <style>
	  body{padding-top:15px; margin-left:18px;}
	  h2{ padding:0; margin:0; }
	  button{ padding:0; margin:0; vertical-align:middle; cursor:pointer}
	  p{ padding:0; margin:0;}
	  #page{ width:900px; margin:0 auto; text-align:left; background:url(images/bg.jpg) no-repeat 0 1px;}
	  .clear{clear:both;font-size:0px;visibility:0px}
	  #persontitle{width:900px; height:22px; line-height:22px; margin:0 auto; background:#3e419e; font-size:14px; color:#fff; padding:1px 0px;}
	  #persontitle strong {float:left;margin-left:20px;display:inline;color:#fff;font-size:16px;font-family:黑体;font-weight: normal;}
  	  #page{ width:900px; margin:0 auto; text-align:left; background:url(images/bg.jpg) no-repeat 0 1px;}
  	  .contentbox{ margin:10px auto; width:797px; background:url(images/bg_1.jpg) repeat-y left #fff;}
      .contentboxtitle{ height:69px; clear:both; padding:0 33px 0 50px; background:url(images/bg3a.jpg) no-repeat 0 0;}
  	  .contentboxtitle h2{ font-size:18px; font-weight:bold; color:#1F3EA6; padding:20px 0 3px 0;}
      .content form div table{float:left; margin-left:40px; width:700px;text-align:left;}
	</style>
	<script type="text/javascript">
	function validate(){
		var name=document.getElementById("name");
		var birth=document.getElementById("birth");
		var place=document.getElementById("place");
		var school=document.getElementById("school");
		var unit=document.getElementById("unit");
		var address=document.getElementById("address");
		var experience=document.getElementById("experience");
		if(name.value==""){
			alert("请输入姓名");
			return false;
		}else if(birth.value==""){
			alert("请输入出生日期");
			return false;
		}else if(place.value==""){
			alert("请输入籍贯");
			return false;
		}else if(school.value==""){
			alert("请输入毕业院校");
			return false;
		}else if(address.value==""){
			alert("请输入家庭地址");
			return false;
		}else if(experience.value==""){
			alert("请输入个人简历");
			return false;
		}else{
			return true;
		}
	}
	</script>
  </head>
  <body>
	<div id="persontitle">
		<strong>个人信息</strong>
  	</div>
  	<div id="page">
	  	<div class="clear"></div>
		<div class="contentbox">
			<div class="contentboxtitle">
				<h2><img src="images/contentbox_title.gif" title="个人信息" alt="个人信息" /></h2>
				<p>请您详细填写个人信息</p>
			</div>
		</div>
		<div class="content">
			<form name="regInfo" id="regInfo" method="post">
				<div>
					<table>
					<tr>
						<td>姓名：</td>
						<td><input type="text" name="name" id="name" /></td>
						<td>性别：</td>
						<td>
							<input type="radio" id="gender" name="gender" value="male" checked="true">男</input>
							<input type="radio" id="gender" name="gender" value="female" >女</input>
						</td>
						<td>民族：</td>
						<td>
							<select name="nation" id="nation">
								<option value="汉族" selected="true">汉族</option>
								<option value="蒙古族">蒙古族</option>
								<option value="回族">回族</option>
							</select></td>
						<td rowspan="3"><img src="images/person.png" alt="照片"></img></td>
					</tr>
					<tr>
					<td>出生日期：</td>
						<td><input type="text" name="birth" id="birth" /></td>
					<td>籍贯：</td>
						<td colspan="4"><input type="text" name="place" id="place" size="30"/></td>
					</tr>
					<tr>
					<td>学历：</td>
						<td><select name="nation" id="nation">
								<option value="博士研究生" selected="true">博士研究生</option>
								<option value="硕士研究生">硕士研究生</option>
								<option value="大学本科">大学本科</option>
								<option value="专科毕业">专科毕业</option>
								<option value="在校学生">在校学生</option>
							</select></td>
					<td>毕业院校：</td>
						<td colspan="4"><input type="text" name="school" id="school" size="30"/></td>
					</tr>
					<tr>
					<td>工作单位：</td>
						<td colspan="6"><input type="text" name="unit" id="unit" size="85"/></td>
					</tr>
					<tr>
					<td>家庭住址：</td>
						<td colspan="6"><input type="text" name="address" id="address" size="85"/></td>
					</tr>
					<tr>
					<td>个人爱好：</td>
					<td colspan="6"><input type="checkbox" name="hobby" value="liter" checked="true">文学</input>
						<input type="checkbox" name="hobby" value="music" >音乐</input>
						<input type="checkbox" name="hobby" value="art" >美术</input>
						<input type="checkbox" name="hobby" value="game" >电脑游戏</input></td>
					</tr>
					<tr>
					<td>个人经历：</td>
					<td  colspan="6"><textarea name="experience" cols="84" rows="6"></textarea></td>
					</tr>
					<tr>
					<td colspan="7" align="center">
						<input type="submit" value="保存个人信息" onclick="validate()"/>
						<input type="reset" value="重置" /></tr>
					</td>
				</table>
				
				</div>
			</form>
		</div>
  	</div>
  </body>
</html>
