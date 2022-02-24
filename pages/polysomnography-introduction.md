# Polysomnography introduction

Data collection for PSG was standardized among various manufactured instruments by use of standardized collection and display montages. Each unit used for collection was certified before use to maximize signal quality integrity throughout the EDF conversion and import into Compumedics Profusion software used for scoring.

Notes:

- [Montage and Sampling Rate Information on MrOS Sleep Visit 1](:pages_path:/equipment-mros1.md)
- [Montage and Sampling Rate Information on MrOS Sleep Visit 2](:pages_path:/equipment-mros2.md)

## Signal and annotation files

[Raw polysomnography data](:files_path:/polysomnography) are available for 2,907 subjects at MrOS Sleep Visit 1 and 1,026 subjects at MrOS Sleep Visit 2. Each recording has a signal file (.EDF) and two versions of the event scoring and epoch staging annotations (.XML).

1. **[EDF](:files_path:/polysomnography/edfs)** - Signal files in the [European Data Format](http://www.edfplus.info/) exported from Compumedics Profusion.
2. **[XML (Profusion)](:files_path:/polysomnography/annotations-events-profusion)** - Annotation files exported from Compumedics Profusion. ([Learn more...](https://github.com/nsrr/edf-editor-translator/wiki/Compumedics-Annotation-Format))
3. **[XML (NSRR)](:files_path:/polysomnography/annotations-events-nsrr)** - Annotation files processed in the [EDF Editor and Translator](https://github.com/nsrr/edf-editor-translator) tool.

NSRR XML files can be overlaid onto EDF signal files using the [EDF Viewer tool](https://github.com/nsrr/edf-viewer). For more information about the XML translation (mapping) process, review the files available on the [EDF Editor and Translator Releases page](https://github.com/nsrr/edf-editor-translator/releases).

## Hypopnea event tags

Hypopnea events are represented by two different tags in the XML annotation files. Events with the `Hypopnea` tag are hypopneas with a reduction in airflow between 30% and 50% from baseline levels. Events with the `Unsure` tag are hypopneas with a reduction in airflow greater than 50% from baseline levels.

If interested in all hypopneas that have a 30% or more reduction in airflow, both event types should be included. If interested in events with greater reduction in airflow (>50%), use those that were labeled with the `Unsure` tag.

The `Unsure` tag **does not represent uncertainty about the event**, but rather was the only custom tag available in the original polysomnography scoring program.

Additional criteria can be applied to limit events based on associated desaturation and/or arousal.

## Known issues

- `visit1`
  - Subject aa2180 does not have XML annotation files. Scoring and staging data could not be reliably exported. The EDF is intact.
  - Many subjects (aa0236, aa0425, aa0461, aa1477, aa2159, aa2339, aa2608, aa3354, aa3386, aa4712, aa4858, aa4860) do not have scoring annotations in the XML annotation files. The staging information appears correct, though other scoring data were lost due to past file corruption.
  - Raw data and annotations for four subjects (aa1103, aa1578, aa2660, aa5781) are not available due to prior data loss.

## History / changelog

*December 2018*
- `visit1`
  - aa2180 XML annotation files removed (unreliable data)
  - aa2618, aa2931 XML annotation files re-exported and replaced (fix issues with past file corruption)

*February 2017*
- `visit2`
  - aa0889, aa5061 replaced (lights setting issue, fixed with re-exporting)
  - aa2618, aa2649, aa3601, aa3624, aa3780, aa5006 replaced (linked references, fixed with re-exporting)

*December 2016*
- Change EDF recording dates from "00.00.00" (invalid) to "01.01.85" (valid de-identified date)

*August 2015*
- Polysomnography data uploaded to sleepdata.org after exports from Compumedics Profusion

## Questions?

Please reach out to us at support@sleepdata.org or in the [Forum](https://sleepdata.org/forum) if you have questions.
