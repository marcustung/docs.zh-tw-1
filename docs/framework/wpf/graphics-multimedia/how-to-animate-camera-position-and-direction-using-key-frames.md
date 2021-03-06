---
title: HOW TO：使用主要畫面格建立鏡頭位置和方向的動畫
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], camera direction with key frames
- key frames [WPF], animating camera direction
- animation [WPF], camera position with key frames
- camera position [WPF], animating with key frames
- key frames [WPF], animating camera position
- camera direction [WPF], animating with key frames
ms.assetid: 5753024e-0057-454d-947f-43ea686879c7
ms.openlocfilehash: 44464cc314d649516998338e36c1b523101ac4e2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59346076"
---
# <a name="how-to-animate-camera-position-and-direction-using-key-frames"></a>HOW TO：使用主要畫面格建立鏡頭位置和方向的動畫
在下列範例中，<xref:System.Windows.Media.Animation.Point3DAnimationUsingKeyFrames>用來以動畫顯示的位置<xref:System.Windows.Media.Media3D.PerspectiveCamera>3D 場景中。 颾魤 ㄛ<xref:System.Windows.Media.Animation.Vector3DAnimationUsingKeyFrames>用來以動畫顯示 3D 場景中指向觀景窗的方向。 這兩個動畫使用數個主要畫面格建立一系列的動畫效果：  
  
1. <xref:System.Windows.Media.Animation.LinearPoint3DKeyFrame> 和<xref:System.Windows.Media.Animation.LinearVector3DKeyFrame>用來建立值之間的平滑的線性插補。  
  
2. <xref:System.Windows.Media.Animation.DiscretePoint3DKeyFrame> 和<xref:System.Windows.Media.Animation.DiscreteVector3DKeyFrame>用來建立突然 「 跳躍點 」 值 （沒有插補） 之間。  
  
3. <xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame> 並<xref:System.Windows.Media.Animation.SplineVector3DKeyFrame>用來建立變數轉換取決於值之間<xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame.KeySpline%2A>屬性。 下列範例中，在動畫啟動很緩慢，但接近時間區段結尾時，以指數方式加速。  
  
## <a name="example"></a>範例  
 [!code-xaml[Animation3DGallery_snip#PointVector3DAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/PointVector3DAnimationUsingKeyFramesExample.xaml#pointvector3danimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a>另請參閱

- [在立體場景中建立鏡頭位置和方向的動畫](how-to-animate-camera-position-and-direction-in-a-3d-scene.md)
- [立體圖形概觀](3-d-graphics-overview.md)
