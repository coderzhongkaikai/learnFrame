
* JSX，JSX 中嵌入表达式（大括号内放置任何有效的 JavaScript 表达式）
在编译之后，JSX 表达式会被转为普通 JavaScript 函数调用，并且对其取值后得到 JavaScript 对象。
通俗：html标签当作js代码写

* 因为 this.props 和 this.state 可能会异步更新，所以你不要依赖他们的值来更新下一个状态。
this.setState((state, props) => ({
  counter: state.counter + props.increment
}));

* 数据是向下流动的,props接受的参数不能判断在父组件的来源

* class 的方法默认不会绑定 this

4.key 会传递信息给 React ，但不会传递给你的组件，不能读出 props.key。
如果你的组件中需要使用 key 属性的值，请用其他属性名显式传递这个值。

5.受控组件：在 HTML 中，表单元素（如<input>、 <textarea> 和 <select>）之类的表单元素通常自己维护 state，并根据用户输入进行更新。
而在 React 中，可变状态（mutable state）通常保存在组件的 state 属性中，并且只能通过使用 setState()来更新。
使 React 的 state 成为“唯一数据源”。渲染表单的 React 组件还控制着用户输入过程中表单发生的操作。
被 React 以这种方式控制取值的表单输入元素就叫做“受控组件”。

6.提取组件
将组件拆分为更小的组件

7.状态提升
通常，多个组件需要反映相同的变化数据，这时我们建议将共享状态提升到最近的共同父组件中去。
依靠自上而下的数据流，而不是尝试在不同组件间同步 state。

8.组合
props.children

9.Context

10.函数组件与 class 组件

11.render prop 具有 render prop 的组件接受一个函数，该函数返回一个 React 元素并调用它而不是实现自己的渲染逻辑。

12.Fragments<></>

13.Refs 转发
