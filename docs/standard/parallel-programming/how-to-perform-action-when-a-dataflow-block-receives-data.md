---
title: "如何：在数据流块收到数据时执行操作"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Task Parallel Library, dataflows
- TPL dataflow library, receiving data
ms.assetid: fc2585dc-965e-4632-ace7-73dd02684ed3
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d049d20f5e685096a72857cd18a89688633883c3
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-perform-action-when-a-dataflow-block-receives-data"></a>如何：在数据流块收到数据时执行操作
在接收数据时，执行数据流块类型会调用用户提供的委托。 <xref:System.Threading.Tasks.Dataflow.ActionBlock%601?displayProperty=nameWithType>、<xref:System.Threading.Tasks.Dataflow.TransformBlock%602?displayProperty=nameWithType> 和 <xref:System.Threading.Tasks.Dataflow.TransformManyBlock%602?displayProperty=nameWithType> 类是执行数据流块类型。 当为执行数据流块提供工作函数时，可以使用 `delegate` 关键字（`Sub` 中为 [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]）、<xref:System.Action%601>、<xref:System.Func%602> 或 lambda 表达式。 本文档描述如何使用 <xref:System.Func%602> 和 lambda 表达式在执行块中执行操作。  
  
> [!TIP]
>  TPL 数据流库（<xref:System.Threading.Tasks.Dataflow?displayProperty=nameWithType> 命名空间）不是随 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 一起分发的。 若要安装<xref:System.Threading.Tasks.Dataflow>命名空间中，打开你的项目中[!INCLUDE[vs_dev11_long](../../../includes/vs-dev11-long-md.md)]，选择**管理 NuGet 包**从项目菜单，然后联机搜索`Microsoft.Tpl.Dataflow`包。  
  
## <a name="example"></a>示例  
 下面的示例使用数据流从磁盘读取一个文件并计算该文件中等于零的字节的数量。 它使用 <xref:System.Threading.Tasks.Dataflow.TransformBlock%602> 读取文件并计算零字节的数量，并使用 <xref:System.Threading.Tasks.Dataflow.ActionBlock%601> 将零字节的数量输出到控制台。 当块收到数据时，<xref:System.Threading.Tasks.Dataflow.TransformBlock%602> 对象会指定一个 <xref:System.Func%602> 对象来执行工作。 <xref:System.Threading.Tasks.Dataflow.ActionBlock%601> 对象使用 lambda 表达式将读取到的零字节的数量输出到控制台。  
  
 [!code-csharp[TPLDataflow_ExecutionBlocks#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_executionblocks/cs/dataflowexecutionblocks.cs#1)]
 [!code-vb[TPLDataflow_ExecutionBlocks#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_executionblocks/vb/dataflowexecutionblocks.vb#1)]  
  
 虽然可以为 <xref:System.Threading.Tasks.Dataflow.TransformBlock%602> 对象提供 lambda 表达式，但是本示例使用 <xref:System.Func%602> 来允许其他代码使用 `CountBytes` 方法。 因为要执行的工作是此任务特有的，使用其他代码不可能有用，所以 <xref:System.Threading.Tasks.Dataflow.ActionBlock%601> 对象使用 lambda 表达式。 有关 lambda 表达式如何在任务并行库中工作的详细信息，请参阅 [PLINQ 和 TPL 中的 Lambda 表达式](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)。  
  
 委托类型摘要一节中[数据流](../../../docs/standard/parallel-programming/dataflow-task-parallel-library.md)文档汇总了你可以向提供的委托类型<xref:System.Threading.Tasks.Dataflow.ActionBlock%601>， <xref:System.Threading.Tasks.Dataflow.TransformBlock%602>，和<xref:System.Threading.Tasks.Dataflow.TransformManyBlock%602>对象。 该表还指出委托类型是同步执行还是异步执行。  
  
## <a name="compiling-the-code"></a>编译代码  
 复制示例代码并将其粘贴到 Visual Studio 项目中，或粘贴到一个名为 `DataflowExecutionBlocks.cs`（对于 [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]，则为 `DataflowExecutionBlocks.vb`）的文件中，然后在 Visual Studio 命令提示符窗口中运行以下命令。  
  
 [!INCLUDE[csprcs](../../../includes/csprcs-md.md)]  
  
 **csc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowExecutionBlocks.cs**  
  
 [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]  
  
 **vbc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowExecutionBlocks.vb**  
  
## <a name="robust-programming"></a>可靠编程  
 此示例为 <xref:System.Func%602> 对象提供类型 <xref:System.Threading.Tasks.Dataflow.TransformBlock%602> 的委托，以同步执行数据流块的任务。 为了使数据流块异步执行操作，请为数据流块提供类型 <xref:System.Func%601> 的委托。 当数据流块异步执行操作时，数据流块的任务只有在返回的 <xref:System.Threading.Tasks.Task%601> 对象完成时才会完成。 下面的示例修改了 `CountBytes` 方法，并使用 [async](~/docs/csharp/language-reference/keywords/async.md) 和 [await](~/docs/csharp/language-reference/keywords/await.md) 运算符（[!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)] 中为 [Async](~/docs/visual-basic/language-reference/modifiers/async.md) 和 [Await](~/docs/visual-basic/language-reference/operators/await-operator.md)）异步计算所提供文件中为零的字节的总数。 <xref:System.IO.FileStream.ReadAsync%2A> 方法异步执行文件读取操作。  
  
 [!code-csharp[TPLDataflow_ExecutionBlocks#2](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_executionblocks/cs/dataflowexecutionblocks.cs#2)]
 [!code-vb[TPLDataflow_ExecutionBlocks#2](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_executionblocks/vb/dataflowexecutionblocks.vb#2)]  
  
 还可以使用异步的 lambda 表达式在执行数据流块中执行操作。 下面的示例修改了上一示例中使用的 <xref:System.Threading.Tasks.Dataflow.TransformBlock%602> 对象，以便使用 lambda 表达式异步执行工作。  
  
 [!code-csharp[TPLDataflow_ExecutionBlocks#3](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_executionblocks/cs/dataflowexecutionblocks.cs#3)]
 [!code-vb[TPLDataflow_ExecutionBlocks#3](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_executionblocks/vb/dataflowexecutionblocks.vb#3)]  
  
## <a name="see-also"></a>另请参阅  
 [数据流](../../../docs/standard/parallel-programming/dataflow-task-parallel-library.md)
