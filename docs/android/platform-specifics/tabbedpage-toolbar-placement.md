---
title: "TabbedPage toolbar placement on Android"
description: "This article explains how to consume the .NET MAUI Android platform-specific that sets the placement of the toolbar on a TabbedPage."
ms.date: 04/05/2022
---

# TabbedPage toolbar placement on Android

These .NET Multi-platform App UI (.NET MAUI) Android platform-specifics are used to set the placement of the toolbar on a `TabbedPage`. They are consumed in XAML by setting the `TabbedPage.ToolbarPlacement` attached property to a value of the `ToolbarPlacement` enumeration:

```xaml
<TabbedPage ...
            xmlns:android="clr-namespace:Microsoft.Maui.Controls.PlatformConfiguration.AndroidSpecific;assembly=Microsoft.Maui.Controls"
            android:TabbedPage.ToolbarPlacement="Bottom">
    ...
</TabbedPage>
```

[!INCLUDE [docs under construction](~/includes/preview-note.md)]

Alternatively, they can be consumed from C# using the fluent API:

```csharp
using Microsoft.Maui.Controls.PlatformConfiguration.AndroidSpecific;
...

On<Microsoft.Maui.Controls.PlatformConfiguration.Android>().SetToolbarPlacement(ToolbarPlacement.Bottom);
```

The `TabbedPage.On<Microsoft.Maui.Controls.PlatformConfiguration.Android>` method specifies that this platform-specific will only run on Android. The `TabbedPage.SetToolbarPlacement` method, in the `Microsoft.Maui.Controls.PlatformConfiguration.AndroidSpecific` namespace, is used to set the toolbar placement on a `TabbedPage`, with the `ToolbarPlacement` enumeration providing the following values:

- `Default` – indicates that the toolbar is placed at the default location on the page. This is the top of the page on phones, and the bottom of the page on other device idioms.
- `Top` – indicates that the toolbar is placed at the top of the page.
- `Bottom` – indicates that the toolbar is placed at the bottom of the page.

> [!NOTE]
> The `GetToolbarPlacement` method can be used to retrieve the placement of the `TabbedPage` toolbar.

The result is that the toolbar placement can be set on a `TabbedPage`:

:::image type="content" source="media/tabbedpage-toolbar-placement/tabbedpage-toolbar-placement.png" alt-text="TabbedPage toolbar configuration.":::
