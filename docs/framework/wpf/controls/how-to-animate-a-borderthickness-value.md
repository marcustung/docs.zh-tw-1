---
title: HOW TO：建立 BorderThickness 值的動畫
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- border thickness [WPF], animating changes to
- animation [WPF], changes to border thickness
ms.assetid: fd021978-f74b-4e7b-a7f7-3987dcad9e0f
ms.openlocfilehash: 10e177d1f6d6add4638ce14af900e75d7e363890
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59150731"
---
# <a name="how-to-animate-a-borderthickness-value"></a>HOW TO：建立 BorderThickness 值的動畫
此範例示範如何建立變更框線粗細的動畫使用<xref:System.Windows.Media.Animation.ThicknessAnimation>類別。  
  
## <a name="example"></a>範例  
 下列範例會建立框線粗細的動畫使用<xref:System.Windows.Media.Animation.ThicknessAnimation>。 此範例會使用<xref:System.Windows.Controls.Border.BorderThickness%2A>屬性<xref:System.Windows.Controls.Border>。  
  
 [!code-csharp[BasicAnimations_snip#ThicknessAnimationWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/ThicknessAnimationExample.cs#thicknessanimationwholepage)]
 [!code-vb[BasicAnimations_snip#ThicknessAnimationWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/ThicknessAnimationExample.vb#thicknessanimationwholepage)]  
  
 如需完整的範例，請參閱[動畫範例圖庫](https://go.microsoft.com/fwlink/?LinkID=159969)。  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Windows.Media.Animation.ThicknessAnimation>
- <xref:System.Windows.Controls.Border.BorderThickness%2A>
- <xref:System.Windows.Controls.Border>
- [動畫概觀](../graphics-multimedia/animation-overview.md)
- [動畫和計時 how to 主題](../graphics-multimedia/animation-and-timing-how-to-topics.md)
- [使用主要畫面格建立框線粗細的動畫](../graphics-multimedia/how-to-animate-the-thickness-of-a-border-by-using-key-frames.md)
