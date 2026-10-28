# Planetary Flyover Concept

## Scope

Terra-Prospect analyzes calibrated remote-sensing observations from a flyover of a planetary body.
The body, spacecraft, instrument suite, and sensor combination are inputs rather than fixed product
assumptions.

The system produces separate evidence products for:

1. habitability and biosignature potential;
2. valuable resource potential; and
3. landing suitability for declared mission constraints.

It must also be able to conclude that the available observations are insufficient for one or more
goals.

## Processing boundary

```text
planetary archive / mission product / local calibrated asset
                              │
                    mission-instrument adapter
                              │
             calibration, geometry, quality, provenance
                              │
                 co-registered planetary data cube
                              │
              physics-anchored modality plugins
                              │
              goal-specific probabilistic evidence
                              │
      uncertainty / cost / redundancy-aware combination analysis
                              │
        maps + confidence + provenance + recommendation or abstention
```

Adapters are responsible for preserving the meaning of their source products, including body,
platform, instrument, observation time, calibration level, units, spectral or radar configuration,
viewing and illumination geometry, pixel footprint, coordinate reference, quality masks, and source
digest.

Modality plugins declare their prerequisites and validity envelope. A hyperspectral plugin, radar
plugin, or thermal plugin is not assumed to inform every goal. Each emits only scientifically
supported, goal-specific evidence with explicit uncertainty and provenance.

## Combination principle

Every available sensor is not automatically fused. A combination should be preferred when it adds
useful coverage or reduces decision-relevant uncertainty without merely repeating a shared signal or
systematic error. Selection therefore considers:

- expected information contribution;
- valid spatial coverage;
- measurement and model uncertainty;
- shared provenance or correlated systematics;
- processing and operational cost;
- the scientific relevance of the evidence to the selected goal.

A single sensor remains a valid case. Unknown areas remain unknown.

## Interoperability direction

The intended public-data path uses planetary archive metadata such as
[NASA PDS4](https://pds.nasa.gov/datastandards/about/), planetary image processing compatible with
[USGS ISIS](https://astrogeology.usgs.gov/docs/getting-started/using-isis-first-steps/about-isis/),
STAC-like asset discovery, and chunked multidimensional storage such as
[OGC Zarr](https://www.ogc.org/standards/zarr-storage-specification/). These are integration
directions, not claims that planetary calibration or geometry can be reduced to a generic Earth
observation catalog.

## Scientific limits

- Orbital observations can prioritize candidate habitability or biosignature evidence but generally
  cannot prove life exists.
- A spectral or geophysical anomaly is not automatically an accessible or economically valuable
  resource.
- A landing score depends on vehicle constraints, resolution, geodetic accuracy, illumination, and
  hazard validation; it is not flight certification.
- Cross-body generalization must be demonstrated rather than assumed.
