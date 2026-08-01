# Tracking by Trial and Error 

PDFtrack is for multi-camera tracking what SORT is for single-camera tracking: fast, simple, elegant.

Instead of associating detections across cameras, PDFtrack reconstructs the scene directly. For each frame, it samples candidate 3D positions around each tracked person, projects them into every camera as bounding boxes, and picks the configuration that best matches the observed detections. Tracks are managed SORT-style: unmatched detections spawn new tracks, modelled as 3D cylinders; unmatched tracks age out.

No re-ID, no learned associations — pure geometry.

96.6 3D MOTA, 93.0 3D IDF1 and 62.4 HOTA on [MMPTrack dataset](https://arxiv.org/abs/2111.15157), real-time on consumer hardware.


📄 **[Read the full paper (PDF)](paper.pdf)**

The core idea:

<p align="center">
  <a href="paper.pdf">
    <img src="teaser.png" width="800">
  </a>
</p>

