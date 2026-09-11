# CBCT dental segmentation demo

Browser viewer over precomputed segmentation results on public CBCT volumes.
Built by [Silurus Software](https://www.silurus-software.com/) as a technology
demonstration. Not a medical device.

Live: https://silurussoftware.github.io/cbct-demo/

## What it shows

Two dental CBCT volumes, each segmented by two pretrained models:

- **DentalSegmentator**, five structures (upper skull, mandible, upper teeth,
  lower teeth, mandibular canal).
- **Per-tooth, two stage**, up to 32 individually numbered teeth. Stage one
  locates the arches on the whole volume, stage two runs the per-tooth model on
  the cropped region only, which cuts memory use from roughly 26 GB to a few GB.

Every structure can be shown, hidden and recoloured. Slice views and a WebGL
volume render of the same data.

## Credits and licences

- CBCT volumes: public [3D Slicer sample data](https://github.com/Slicer/SlicerDataStore).
- [DentalSegmentator](https://github.com/gaudot/SlicerDentalSegmentator), CC BY 4.0.
- [ToothSeg](https://github.com/MIC-DKFZ/ToothSeg), CC BY 4.0, trained on the
  ToothFairy2 dataset.
- Viewer: [Niivue](https://github.com/niivue/niivue).
