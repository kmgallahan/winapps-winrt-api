---
-api-id: T:Microsoft.UI.Xaml.Media.Animation.DoubleAnimationUsingKeyFrames
-api-type: winrt class
---

<!-- Class syntax.
public class DoubleAnimationUsingKeyFrames : Windows.UI.Xaml.Media.Animation.Timeline, Windows.UI.Xaml.Media.Animation.IDoubleAnimationUsingKeyFrames
-->

# Microsoft.UI.Xaml.Media.Animation.DoubleAnimationUsingKeyFrames

## -description
Animates the value of a [Double](/dotnet/api/system.double?view=dotnet-uwp-10.0&preserve-view=true) property along a set of key frames.

## -xaml-syntax
```xaml
<DoubleAnimationUsingKeyFrames>
  oneOrMoreDoubleKeyFrames
</DoubleAnimationUsingKeyFrames>
```


## -remarks

## -examples
The following example moves a rectangle across a screen. The example uses the **DoubleAnimationUsingKeyFrames** class to animate the [X](../microsoft.ui.xaml.media/translatetransform_x.md) property of a [TranslateTransform](../microsoft.ui.xaml.media/translatetransform.md) applied to a [Rectangle](../microsoft.ui.xaml.shapes/rectangle.md). This animation uses three key frames in the following manner:


1. During the first three seconds, it uses an instance of the [LinearDoubleKeyFrame](lineardoublekeyframe.md) class to move the rectangle along a path at a steady rate from its starting position to the 500 position. Linear key frames like [LinearDoubleKeyFrame](lineardoublekeyframe.md) create a smooth linear transition between values.
1. At the end of the fourth second, it uses an instance of the [DiscreteDoubleKeyFrame](discretedoublekeyframe.md) class to suddenly move the rectangle to the next position. Discrete key frames like [DiscreteDoubleKeyFrame](discretedoublekeyframe.md) create sudden jumps between values. In this example, the rectangle is at the starting position and then suddenly appears at the 500 position.
1. In the final two seconds, it uses an instance of the [SplineDoubleKeyFrame](splinedoublekeyframe.md) class to move the rectangle back to its starting position. Spline key frames like [SplineDoubleKeyFrame](splinedoublekeyframe.md) create a variable transition between values according to the value of the [KeySpline](splinedoublekeyframe_keyspline.md) property. In this example, the rectangle begins by moving slowly and then speeds up exponentially toward the end of the time segment.

[!code-xaml[Doubleanimationusingkeyframes2](../microsoft.ui.xaml.media.animation/code/doubleanimationusingkeyframes2/csharp/Page.xaml#SnippetDoubleanimationusingkeyframes2_cs)]

[!code-vb[Doubleanimationusingkeyframes2](../microsoft.ui.xaml.media.animation/code/doubleanimationusingkeyframes2/vbnet/Page.xaml.vb#SnippetDoubleanimationusingkeyframes2)]

[!code-csharp[SnippetDoubleanimationusingkeyframes2](../microsoft.ui.xaml.media.animation/code/doubleanimationusingkeyframes2/csharp/Page.xaml.cs#SnippetDoubleanimationusingkeyframes2)]

## -see-also
[Storyboarded animations](/windows/apps/design/motion/storyboarded-animations)
