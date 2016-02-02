# Itable2excel
页面table导出成excel文件

使用示例

<a href="#" download="交易记录.xls"class="to_excel fjgl_top_r_05">导出</a>

$(".to_excel").click(function(event){
	var t = Itable2excel({
		worksheet:'数据分析',
		table: $('#order-list table')
	});
	var data64 = t.uri();
	if(data64==false)
		return false;
	event.currentTarget.href = data64;
});
