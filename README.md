# CBCT dental segmentation demo

Browser viewer over precomputed segmentation results on public CBCT volumes.
Built by [Silurus Software](https://www.silurus-software.com/) as a technology
demonstration. Not a medical device.

Live: https://silurussoftware.github.io/cbct-demo/

## What it shows

Three dental CBCT volumes. Two of them also carry the manual expert annotation
published with the dataset, so the model output can be compared against a human
reference in the same viewer.

- **DentalSegmentator**, five structures (upper skull or maxilla, mandible,
  upper teeth, lower teeth, mandibular canal).
- **Per-tooth, two stage**, up to 32 individually numbered teeth. Stage one
  locates the arches on the whole volume, stage two runs the per-tooth model on
  the cropped region only, which cuts memory use from roughly 26 GB to a few GB.
- **Manual reference**, the annotation made by the dataset authors.

Every structure can be shown, hidden and recoloured. Slice views and a WebGL
volume render of the same data.

Neither model was trained on any of the volumes shown here.

## Credits and licences

- CBCT volumes: public [3D Slicer sample data](https://github.com/Slicer/SlicerDataStore)
  and the [DentVoxel dataset](https://doi.org/10.6084/m9.figshare.31239889), CC BY 4.0.
- [DentalSegmentator](https://github.com/gaudot/SlicerDentalSegmentator), CC BY 4.0.
- [ToothSeg](https://github.com/MIC-DKFZ/ToothSeg), CC BY 4.0, trained on the
  ToothFairy2 dataset.
- Viewer: [Niivue](https://github.com/niivue/niivue).
