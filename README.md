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

The DegaFiles upload is complete. All 112,649 data files were uploaded in 145
batches, each containing at most 1,000 files or 128 MiB, and the final Git tree
was checked against the local inventory. Representative raw-file downloads were
also checked by SHA-256.

View the dataset with Celldega:

```python
import celldega as dega

landscape = dega.viz.Landscape(
    technology="Xenium",
    base_url="https://raw.githubusercontent.com/broadinstitute/Celldega_Atera_v1_WTA_Kidney_non_diseased_FFPE/main",
    max_tiles_to_view=25,
)
landscape
```

## Annotated counts for linked Clustergrams

The full [annotated count AnnData is available on Hugging Face](https://huggingface.co/datasets/broadinstitute/Celldega_Supporting_Data/blob/main/Atera_v1_WTA_Kidney_non_diseased_FFPE.h5ad).
It contains 399,120 cells and 18,049 gene-expression features, raw counts,
the default Leiden labels, Azimuth broad/coarse/fine annotations and scores,
and the original UMAP. The compressed file is 1,401,432,095 bytes.

SHA-256: `3002804d996888d071787f26a54a2dfd1eec70554c745908e207e933d4c6611d`.
