# select2tree
extend select2 for treeview. 扩展select2，使它可以树形展示，可以缩放。

<a href="http://runjs.cn/detail/bezljwvl" target="_blank">See demo</a>

# 使用方法
* 与select2用法一致，只是在使用时$('select').select2()变成了$('select').select2tree()。
* option标签中指定parent属性即可实现树形展示，支持数据源乱序，展示下拉选项时将自动排序。


# select2tree (RU)
Плагин для древовидного отображения выпадающего списка select2. Позволяет реализовать любой уровень вложенности для ``<option>`` в ``<select>``. 

Связывание дочернего ``<option>`` с родительским происходит через аттрибуты ``val`` и ``parent`` - у дочернего элемента должен быть указан ``parent="parent_value_attribute"``.

### Пример использования

[Посмотреть демо](http://runjs.cn/detail/bezljwvl)

Для инициализации виджета используйте следующий код: 

```
  <select id="tree-select">
    <option val="root">Корень</option>
    <option val="level11" parent="root">Уровень 1.1</option>
    <option val="level12" parent="root">Уровень 1.2</option>
    <option val="level21" parent="level12">Уровень 2.1</option>
    <option val="level22" parent="level12">Уровень 2.2</option>
    <option val="level13" parent="root">Уровень 1.3</option>
  </select>
  <script>
    $("#tree-select").select2tree();
  </script>
```

Если вы хотите предварительно выставить значения, то можете использовать событие select2:
```
  <script>
    $("#tree-select").val(["root", "level21"]).trigger('change');
  </script>  
```
