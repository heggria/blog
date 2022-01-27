## 

这几天学习 hook，发现这东西确实强大，能做到很多其他框架做不到的事

### Hook 是什么

是一些函数钩子，可以将变量与函数关联起来形成一个闭包，外部想读取或者操作里面的变量必须通过 hook 返回的变量引用或者函数进行操作。

```js
const [a,setA] = useState('') // 默认值 空字符串
```
上面是官方的 `useState` hook，我们调用这个函数可以获取到一个数组，这个数组第一个量是已经被 hook 绑定好的内部变量，第二个量是已经被 hook 绑定好的更改内部变量的函数，至于为什么要这样定义一个变量我们后面会谈到。

### 还有其他 Hook 吗
- `useState` 定义一个**可被依赖**的变量
- `useEffect` 有**副作用**的函数写在这里，执行时机
- `useRef` 可以保存 DOM 的引用或者**保存一个常量**，没有依赖项
- `useContext` 设置一个组件上下文，可以被子组件拿到
- `useMemo` 缓存一个有依赖项的函数的**返回值**，用于密集型计算缓存
- `useCallback` 缓存一个有依赖项并可以被调用的**函数引用**，用于函数调用优化缓存
- `useLayoutEffect` 在**视图更新前**进行有副作用的函数
- `useReducer` `useState` 的底层实现，定义一个有 dispatch 的变量
- `useImperativeHandle` 
- `useDebugValue` 在 React 开发者工具中显示自定义 hook 的标签
- `useTransition` **延时**因为 state 改变导致的重新渲染