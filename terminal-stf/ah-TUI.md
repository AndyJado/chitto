# TUI examples

- block

  背景, 边界, 横幅, 主界面框

- canvas

  笔画笔画,是吧?

- barchart

  数据流log

- custom_widget

  ? 组件

- guage

  block实现的进度条

- layout

  Layout里放Block

- list

  StatefulList

- panic

  panic hook获得顺滑的`Error`体验

- paragraph

  也是个围挤

  Span一句话, Spans一句缤纷的话, 

  .style().block().alignment().wrap(换行).scroll

- popup

  EnterAlternateScreen, LeaveAlternateScreen

  还有个文字闪烁!

- sparkline

  ..

- table

  TableState

- tabs

  从一个vec中生成标签

  选中的状态储存在app里, index, not lke table

- User_input

  App中储存, 输入的字符串, 输入状态, 已输入信息(能改变状态的都在了)

  run_app()的loop里面监听用户操作:

  `event::read()?`

`cargo run --example demo --release -- --tick-rate 20`