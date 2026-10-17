# Atera v1 WTA Kidney non-diseased FFPE — DegaFiles

Celldega visualization files generated from the Atera output bundle using the
`atera_preprocess` branch, with `tile_size=250` and all morphology channels.

- 399,120 cells; 24,674 features, including controls; 28 Leiden clusters.
- 1,083,911,533 transcripts with stored QV ≥ 20.
- DAPI, boundary, RNA, and protein image pyramids.
- Approximately 9.68 GiB of visualization data.

The transcript count was checked against the stored Zarr quality scores. The
input `experiment.spatial` summary reports 1,083,799,964 high-quality transcripts;
the DegaFiles preserve the records passing the stored QV threshold.

After all upload batches finish, view the dataset with Celldega:

```python
import celldega as dega

landscape = dega.viz.Landscape(
    technology="Xenium",
    base_url="https://raw.githubusercontent.com/broadinstitute/Celldega_Atera_v1_WTA_Kidney_non_diseased_FFPE/main",
    max_tiles_to_view=25,
)
landscape
```

The data are committed in small batches. A partially uploaded repository may not
yet contain every tile required by the viewer.
