# 演示：创建预警规则

## 创建规则

1. 在 Azure 门户中，单击“**监视**”。监控器边栏选项卡将您所有监控设置和数据整合在一个视图中。
2. 单击“**警报**”，然后单击“**+新建警报规则**”。大多数资源边栏选项卡在其“监控”下的资源菜单中也有警报，因此您也可以在那里创建警报。

## 浏览警报目标

1. 单击“目标”下的“**选择**”，选择要触发警报的目标资源。使用“**订阅**”和“**资源类型**”下拉列表查找要监控的资源。您也可以使用搜索栏来查找您的资源。
2. 如果所选资源具有可以创建警报的指标，右下角的可用信号将包括指标。可在此文中查看指标警报支持的资源类型的完整列表。
3. 选择后单击“**完成**”。

## 浏览警报条件

1. 选择目标资源后，单击“**添加条件**”。
2. 此时会显示资源支持的信号列表，请选择要为其创建警报的指标。
3. 或者，通过调整时期和聚合来细化指标。如果指标具有维度，则会显示维度表。 
4. 你将看到最近 6 小时的指标图表。调整“**显示历史记录**”下拉列表。
5. 定义“**警报逻辑**”。这将决定指标警报规则将评估的逻辑。
6. 如果使用静态阈值，指标图表有助于确定可能合理的阈值。如果您使用的是动态阈值，指标图表将显示基于最近数据计算的阈值。
7. 单击“**完成**”。
8. 如果要监控复杂的警报规则，可以选择添加另一标准。 

## 浏览警报详细信息

1. 填写警报详细信息，如“**预警规则名称**”、“**说明**”和“**严重性**”。
2. 通过选择现有的操作组或创建新的操作组，将操作组添加到警报中。
3. 单击“**完成**”保存指标预警规则。
