# colorator
extract colors from image in various ways, (angular-services)

example usage

```javascript
sortColors() {
    this.generatedColors = this.colorAverager.getSortedBySuperLab(
      this.generatedColors,
      '#ffffff'
    );
  }
  
averageHueSaturationPalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageHueSaturationColors(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode
    );
    this.sortColors();
    this.ioService.setColorsObservable(
      'Hue Saturation, Colorator',
      this.generatedColors
    );
  }

  averageSuperLabSaturationPalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageColorsBySuperLabSaturation(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode,
      '#ffffff'
    );
    this.sortColors();
    this.ioService.setColorsObservable('Lab Saturation', this.generatedColors);
  }

  averageSuperLabHuePalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageColorsBySuperLabHue(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode,
      '#ffffff'
    );
    this.sortColors();
    this.ioService.setColorsObservable('Lab Hue', this.generatedColors);
  }

  averageSuperLabLightnessPalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageColorsBySuperLabLightness(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode,
      '#ffffff'
    );
    this.sortColors();
    this.ioService.setColorsObservable('Lab Lightness', this.generatedColors);
  }

  averageSuperLabLabPalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageColorsBySuperLabLab(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode,
      '#ffffff'
    );
    this.sortColors();
    this.ioService.setColorsObservable('Lab Lab', this.generatedColors);
  }

  averageHueLightnessPalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageHueLightnessColors(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode
    );
    this.sortColors();
    this.ioService.setColorsObservable(
      'Hue Lightness, Light',
      this.generatedColors
    );
  }

  averageHueHuePalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageHueHueColors(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode
    );
    this.sortColors();
    this.ioService.setColorsObservable(
      'Hue Hue, Average',
      this.generatedColors
    );
  }

  averageLightnessSaturationPalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageLightnessSaturationColors(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode
    );
    this.sortColors();
    this.ioService.setColorsObservable(
      'Lightness Saturation, Warm',
      this.generatedColors
    );
  }

  averageLightnessHuePalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageLightnessHueColors(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode
    );
    this.sortColors();
    this.ioService.setColorsObservable('Lightness Hue', this.generatedColors);
  }

  averageLightnessLightnessPalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageLightnessLightnessColors(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode
    );
    this.sortColors();
    this.ioService.setColorsObservable(
      'Lightness Lightness, Cold',
      this.generatedColors
    );
  }

  averageSaturationLightnessPalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageSaturationLightnessColors(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode
    );
    this.sortColors();
    this.ioService.setColorsObservable(
      'Saturation Lightness, Pastel',
      this.generatedColors
    );
  }

  averageSaturationHuePalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageSaturationHueColors(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode
    );
    this.sortColors();
    this.ioService.setColorsObservable('Saturation Hue', this.generatedColors);
  }

  averageSaturationSaturationPalette() {
    const cols = this.imageProcessor.getColorsFromCanvas(
      this.canvas,
      this.averagingPrecision
    );
    this.generatedColors = this.colorAverager.getAverageSaturationSaturationColors(
      cols,
      this.colorAmount,
      0,
      3,
      this.colorMode
    );
    this.sortColors();
    this.ioService.setColorsObservable(
      'Saturation Saturation',
      this.generatedColors
    );
  }
```
