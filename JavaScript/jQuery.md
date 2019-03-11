# jQuery

## Datepicker

### カレンダークリック時のイベント

- optionで後からイベントを設定できる。

~~~ html
<input type="text" id="calendar">
<script src="https://code.jquery.com/jquery-1.11.3.js"></script>
<script src="https://code.jquery.com/ui/1.12.0/jquery-ui.js"></script>
<script>
$('#calendar').datepicker();
$('#calendar').datepicker("option", "onSelect", function(){alert('hoge')});
</script>
~~~

- 参考サイト[StackOverFlow](https://stackoverflow.com/questions/9806742/)
