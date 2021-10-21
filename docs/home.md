![](.images/.Home_images/e00a7b43.png)
# Apache Airflow 官方文档

Airflow 是一个以编程方式创作、调度和监控工作流程的平台。

使用 Airflow 将工作流创作为任务的有向无环图 (DAG)。 
Airflow 调度程序在遵循指定的依赖项的同时在一组工作节点（worker）上执行您的任务。
丰富的命令行实用程序使在 DAG 上执行复杂的任务变得轻而易举。
丰富的用户界面让生产中正在运行的流水线任务（pipelines）变得更加可视化，监控任务执行进度以及在关键时刻解决问题也变得容易。

被定义成代码形式的工作流，在可维护性、版本控制、测试性与协作性等方面都变得更加容易

<img src="https://airflow.apache.org/docs/apache-airflow/stable/_images/airflow.gif" />


## 原则

 - **动态**：Airflow 的流水线任务被配置成了代码，允许动态生成流水线任务。允许用户编写动态实例化的流水线任务代码。

 - **可扩展**：使用 Airflow 可以轻松定义您自己的操作器、执行器以及扩展库，使其满足您个人需求的抽象环境
 
 - **优雅**：Airflow 的流水线任务简洁明了，使用强大的 Jinja 模板引擎，将脚本化的参数构建到 Airflow 的核心中
 
 - **弹性伸缩**： Airflow 具有模块化的架构，使用消息队列协调任意数量的工作节点，并可无限的扩展延伸


## 此外

Airflow 不是一个数据流解决方案，任务不能将数据从一个存储引擎移动到另一个（尽管任务可以交换元数据，但这和数据流不是一个概念）。
Airflow 不是 [Spark Streaming](http://spark.apache.org/streaming/) 或 [Storm](https://storm.apache.org/) ，
而是更类似于 [Oozie](http://oozie.apache.org/) 或 [Azkaban](https://azkaban.github.io/)。

Airflow 通常是静态的或缓慢变化的。您可以将工作流中的任务结构想象成比数据库结构更动态一些。
Airflow 的工作流从本次运行到下次运行通常看起来是相似的，这需要清晰的工作单元和任务执行的连续性。