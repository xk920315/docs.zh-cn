---
title: "如何：向文本应用动画"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- typography [WPF], animations
- animation [WPF], text
ms.assetid: eec3d26c-0a21-420f-8012-671621c47089
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 4d44565907904509a1b8f670453db5d7aa4e2583
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-apply-animations-to-text"></a>如何：向文本应用动画
动画可以更改应用程序中文本的显示和外观。 下面的示例使用不同类型的动画来影响中的文本显示<xref:System.Windows.Controls.TextBlock>控件。  
  
## <a name="example"></a>示例  
 下面的示例使用<xref:System.Windows.Media.Animation.DoubleAnimation>要进行动画处理的文本块宽度。 宽度值从文本块的宽度更改为 0，持续时间为 10 秒，然后再改回其宽度值并继续。 这种动画会创建一个擦除效果。  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample1)]  
  
 下面的示例使用<xref:System.Windows.Media.Animation.DoubleAnimation>要进行动画处理的文本块的不透明度。 不透明度值从 1.0 更改为 0，持续时间为 5 秒，然后再改回其不透明度值并继续。  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample2)]  
  
 下图显示的效果<xref:System.Windows.Controls.TextBlock>控件从其不透明度`1.00`到`0.00`定义的 5 秒间隔期间<xref:System.Windows.Media.Animation.Timeline.Duration%2A>。  
  
 ![文本不透明度从 1.00 改为 0.00](../../../../docs/framework/wpf/advanced/media/fadedtext01.png "FadedText01")  
文本不透明度从 1.00 改为 0.00  
  
 下面的示例使用<xref:System.Windows.Media.Animation.ColorAnimation>要进行动画处理的文本块的前景色。 前景色值从一种颜色更改为另一种颜色，持续时间为 5 秒，然后返回到原来的颜色值并继续。  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample3)]  
  
 下面的示例使用<xref:System.Windows.Media.Animation.DoubleAnimation>旋转文本块。 文本块旋转一圈，持续时间为 20 秒，然后继续重复该旋转。  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample4)]  
  
## <a name="see-also"></a>请参阅  
 [动画概述](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
