# LEDScreenShader

The shader of a realistic LED panels.

Built-in shaders are included, but I'm currently focused on development with the Shader Graph.

<img width="467" alt="Screen Shot 2022-02-12 at 1 08 58" src="https://user-images.githubusercontent.com/113725/153626690-deef6682-13d5-4086-8b39-dec24587deeb.png">

* Grid parameters are currently disabled due to quality issue.
* Includes detailed LED panel textures.


## Samples
detailed version

<img src="https://github.com/llcheesell/LEDScreenShader/blob/main/Docs/de99bb559a84878e447cbc1e7014cee4.gif">
simple version

<img width="577" alt="Screen Shot 2022-02-10 at 13 57 37" src="https://user-images.githubusercontent.com/113725/153345784-378ab0e4-3e55-4e2c-8149-d437d9c11def.png">

<img width="640" alt="Screen Shot 2022-02-10 at 13 59" src="https://user-images.githubusercontent.com/113725/153346605-d261c567-1d2c-4da7-9944-623f21abde96.png">

Distant Fader
<img src="https://github.com/llcheesell/LEDScreenShader/blob/main/Docs/DistantFader2.gif">

## Install
Please import via UPM (Unity Package Manager).

Package Manager > Add Package from Git URL > paste below and import.
```
https://github.com/llcheesell/LEDScreenShader.git?path=/Assets/LEDScreenShader#v0.0.4
```

or you can import unitypackage manually.

Please check [Release v0.0.4](https://github.com/llcheesell/LEDScreenShader/releases/tag/v0.0.4) page.

## Usage

* InputVideo<br>
Apply the texture you want to project to the panel. You can put a video via RenderTexture.<br>
パネルに投影するテクスチャを適用します。

* LED Texture<br>
Set the LED texture. This texture will be multiplied by the InputVideo.<br>
The package include several LED Texture.<br>
LEDのテクスチャを適用します。このパッケージにはいくつかのサンプルが含まれています。

* BaseTexture/NormalTexture/AlphaMap/MaskMap<br>
This is the base material setting for the panel.
Metalic and Smoothness will be multiplied to MaskMap.<br>
パネルのベースマテリアルを設定します。

* Tiling/Offset<br>
Sets the number of tiles and offset of the LED panel.<br>
LEDテクスチャのタイリングを設定します。

* DistantFadeStart/End<br>
Fades the LED texture according to the distance from the camera. This prevents moiré effects.<br>
カメラからの距離に従ってLEDテクスチャを無効化します。これによってモアレ効果を防ぐことができます。

* DistantFadeBrightness<br>
This value allows you to adjust the brightness change caused by the fading of the LED texture.<br>
DistantFadeによって明るさの変化が生じたときに、HDRカラーで明るさを調整することが出来ます。



## Note
Optimized for Linear Color Space. It could be used in Gamma Color Space but the bright area tend to be clamped.<br>
リニアカラースペースでの使用を推奨。

<img src="https://github.com/llcheesell/LEDScreenShader/blob/main/Docs/linear.png">

The combination use of Bloom Post Processing is recommended.<br>
Bloomポストエフェクトの併用を推奨。

## Roadmap
* Moire prevention processing according to the distance from the camera (completed in v0.0.4)
* Higher quality pixel textures ana materials (completed in v0.0.2)


## Preview Release
Preview Release is available at preview branch
```
https://github.com/llcheesell/LEDScreenShader.git?path=/Assets/LEDScreenShader#preview
```