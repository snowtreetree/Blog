# 双向绑定

视图变化更新数据，数据变化更新视图。

实现：Vue 内容通过Objective.defineProperty方法属性拦截的方式，把data对象中的数据的读写转化成getter/setter，当数据变化时通知识图更新。

## MVVM

软件架构设计模式。促进了前后端的逻辑分离。Model层负责数据，View层是用户看到的界面，ViewModel是前端组织生成和维护的视图数据层。

## MVC

M - Model: 模型，用于处理应用程序数据逻辑部分。更新的时候通知View层。
V - View: 视图，处理数据显示。 接受用户交互请求，转交给Controller。
C - Controller: 控制器，处理用户交互部分。操作Model数据。