1. 组件名首字母大写，以区分HTML 元素
   
        import React,{Component} from 'react'

        class MyApp extends Component{
            render(){
                return (
                    <div>
                      hello react!
                    </div>
                )
            }
        }

2. props 传递通过Component<IProps>
   
        interface IPorps{
            title:string;
            content:string;
            say(x:string):string
        }

        class Modal extends Component<IPorps>{

        }

        (props: Readonly<IProps>)
        'Readonly<IProps>': title, content, say

        使用时，必须传值

+ props 默认值
  

使用静态属性defaultProps

        class Modal extends Component<IPorps>{
            static defaultProps={
                title:'default value'
            }
        }

        有默认值，使用组件时，可以不传参数。不传参数是使用默认值。

+ 属性校验