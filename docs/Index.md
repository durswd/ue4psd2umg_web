
# PSD2UMG

PSD2UMG is a plug-in thatimports a PSD file into UnrealEngine4 and converts the PSD file into Widget Blueprints.

![Top](img/Title.png)

## Supports

PSD2UMG converts a layer in a PSD into an object in an Widget Blueprint.

- Image
- Button
- ProgressBar
- Canvas Panel
- Text(Beta)

PSD2UMG assign anchors automatically.

PSD2UMG supports reimport. An appearance of Widget Blueprints can be changed with reimport.

## How to use

### Preparation

#### You prepare a PSD file which is converted into an Widget Blueprint.

Layer styles and shape layer are not supported.

8bitRGB format is only supported.

You need to fix it.

[SampleFile(.psdumg)](https://github.com/durswd/ue4psd2umg_web/releases/download/Samples/SamplePSD.psdumg)

[SampleFile(.psd)](https://github.com/durswd/ue4psd2umg_web/releases/download/Samples/SamplePSD.psd)

![PSD](img/psd.png)

#### Exstention is changed .psd into .psdumg

Because .psd is imported with default function of UE4 as a single image.

![psdumg](img/psdumg.png)

### Import

#### You drag and drop the .psdumg file in contents.

![umg_contents](img/umg_contents.png)

#### An widget blueprint is generated on a directory where you drag and drop it.

You can use thie widget blueprint.

![wb](img/wb_contents.png)

![wb](img/wb_ss.png)

## Elements

### Image

An image layer in PSD is converted Image in UMG.

![wb](img/Desc_Image.png)

### Button

You need to an image layer's name in PSD.

A layer whose name is Sample@Button is converted a button whose name is Sample.

This function has options.

A PSD file has three layers as follows.

- SampleB@Button[Normal]
- SampleB@Button[Hovered]
- SampleB@Button[Pressed]

A button is generated and assigned images as follows.

Normal image is assigned SampleB@Button[Normal].

Hovered image is assigned SampleB@Button[Hovered].

Pressed image is assigned SampleB@Button[Pressed].

A layer is converted whose size are same each other automatically.

![wb](img/Desc_Button.png)

### ProgressBar

You need to an image layer's name in PSD.

A layer whose name is Sample@ProgressBar is converted a progress bar whose name is Sample.

This function has options.

A PSD file has three layers as follows.

- SamplePB@ProgressBar[Background]
- SamplePB@ProgressBar[Fill]
- SamplePB@ProgressBar[Marquee]

A progress bar is generated and assigned images as follows.

Background image is assigned SamplePB@ProgressBar[Background].

Fill image is assigned SamplePB@ProgressBar[Fill].

Marquee image is assigned SamplePB@ProgressBar[Marquee].

![wb](img/Desc_ProgressBar.png)

A layer is converted so that the layer's size are same each other automatically.
 
### CanvasGroup

A group in PSD is converted into CanvasGroup in Widget Blueprint.

The layer's size are defined automatically so that all elements in the group is included in canvas group.

![wb](img/Desc_Group.png)

### Text(Beta)

A text layer in PSD file is converted into Text.

Position and character string is valid.
Other parameters are not supported. (I have a plan to support it.)

![wb](img/Desc_Text.png)

## Reimport

PSD2UMG supports reimport.

When you reimport .psdumg, an object(Image, Button, etc) whose name is same to imported layer's name are changed only apperance such as a position, image and so on. Other parameters are maintained.

In addition, an object(Image, Button, etc) whose name does not exists in imported layer is not changed.

## License

This plugin is depends on

```

// psd.c
//
// Copyright (c) 2014 hkrn
// Released under the MIT license
// https ://opensource.org/licenses/mit-license.php

```