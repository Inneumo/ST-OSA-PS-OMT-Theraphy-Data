# Human-readable data dictionary

This dictionary is organized around the **English encoded dataset**:
[therapy_data_encoded_en.csv](../data/processed/therapy_data_encoded_en.csv).
English normalized names and labels are the primary reference for analysis.
Spanish source names and labels are included as additional traceability fields.

The dataset contains 126 records and 38 variables. The machine-readable sources
are [therapy_data_dictionary_en.json](../data/processed/therapy_data_dictionary_en.json)
and [therapy_data_dictionary.json](../data/processed/therapy_data_dictionary.json).

## Encoding conventions

- Numeric fields remain numeric.
- Binary fields use `0 = NO` and `1 = YES` in the English dictionary.
- Other categorical fields use compact integer codes beginning at `0` within
  each column.
- `NA` means the source cell was empty; it is not a measured zero.
- Decode codes with the `value_mappings` object in the English JSON dictionary.
- `source_name_es` and `spanish_labels` below preserve the original Spanish
  terminology for cross-referencing the source CSV.

## Field reference

### 1. `treatment_level_1`

- **English meaning:** Treatment or therapy scheme assigned at level 1.
- **Type:** Categorical code.
- **English codebook:** `0 = TMO LEVEL 1`; `1 = TMO LEVEL 1 CBT`; `NA = missing`.
- **Spanish source field:** `ESQUEMA NIVEL 1`.
- **Spanish labels:** `0 = TMO NIVEL 1`; `1 = TMO NIVEL 1 TCC`.
- **Note:** The source dictionary does not define the clinical expansion of
  `TCC`.

### 2. `age`

- **English meaning:** Participant age.
- **Type:** Number; values are recorded as whole years in the supplied data.
- **Spanish source field:** `EDAD`.
- **Missing value:** `NA`.

### 3. `sex`

- **English meaning:** Sex category recorded in the source.
- **Type:** Categorical code.
- **English codebook:** `0 = MALE`; `1 = FEMALE`; `NA = missing`.
- **Spanish source field:** `SEXO`.
- **Spanish labels:** `0 = MASCULINO`; `1 = FEMENINO`.
- **Note:** This source field should not be interpreted as a complete measure of
  gender identity.

### 4. `bmi`

- **English meaning:** Body mass index.
- **Type:** Number; conventionally expressed in kg/m².
- **Spanish source field:** `IMC`.
- **Missing value:** `NA`.

### 5. `baseline_epworth`

- **English meaning:** Baseline Epworth Sleepiness Scale score.
- **Type:** Number; score points.
- **Spanish source field:** `EPWORTH BASAL`.
- **Missing value:** `NA`.

### 6. `followup_epworth`

- **English meaning:** Epworth Sleepiness Scale score recorded at the end or
  follow-up assessment.
- **Type:** Number; score points.
- **Spanish source field:** `EPWORTH SALIDA`.
- **Missing value:** `NA`.

### 7. `overall_score`

- **English meaning:** General or overall assessment score.
- **Type:** Number; unit and valid range are not specified in the source.
- **Spanish source field:** `PuntGeneral`.
- **Missing value:** `NA`.

### 8. `baseline_symptoms`

- **English meaning:** Baseline symptom recorded for the participant.
- **Type:** Categorical code.
- **English codebook:** `0 = Bruxism`; `1 = Chronic fatigue`; `2 = Morning
  headache`; `3 = Waking up gasping`; `4 = Difficulty falling asleep`; `5 =
  Difficulty maintaining sleep`; `6 = Sudden movements`; `7 = Nocturia`; `8 =
  Snoring`; `9 = Excessive daytime sleepiness`; `NA = missing`.
- **Spanish source field:** `SINTOMAS BASALES`.
- **Spanish labels:** `Bruxismo`; `Cansancio crónico`; `Cefalea matutina`;
  `Despertarse con ahogo`; `Dificultad para conciliar el sueño`; `Dificultad
  para mantener el sueño`; `Movimientos bruscos`; `Nicturia`; `Ronquido`;
  `Somnolencia diurna excesiva`.

### 9. `primary_symptom`

- **English meaning:** Primary symptom recorded for the participant.
- **Type:** Categorical code.
- **English codebook:** `0 = Chronic fatigue`; `1 = Morning headache`; `2 =
  Waking up gasping`; `3 = Difficulty falling asleep`; `4 = Difficulty
  maintaining sleep`; `5 = Snoring`; `6 = Excessive daytime sleepiness`; `7 =
  Unrefreshing sleep`; `8 = Xerostomia`; `NA = missing`.
- **Spanish source field:** `SINTOMA PRINCIPAL`.
- **Spanish labels:** `Cansancio crónico`; `Cefalea matutina`; `Despertarse con
  ahogo`; `Dificultad para conciliar el sueño`; `Dificultad para mantener el
  sueño`; `Ronquido`; `Somnolencia diurna excesiva`; `Sueño no reparador`;
  `Xerostomía`.

### 10. `sleep_exam_type`

- **English meaning:** Type of sleep examination.
- **Type:** Categorical code.
- **English codebook:** `0 = PLG`; `1 = PSG`; `NA = missing`.
- **Spanish source field:** `TIPO EXAMEN DE SUEÑO`.
- **Note:** The source supplies these abbreviations but does not define them
  further.

### 11. `baseline_ahi`

- **English meaning:** Baseline apnea–hypopnea index (AHI).
- **Type:** Number; clinically expressed as events per hour.
- **Spanish source field:** `IAH BASAL`.
- **Missing value:** `NA`.

### 12. `snoring_index_per_hour`

- **English meaning:** Baseline snoring index.
- **Type:** Number; the source `/h` indicates a per-hour measure.
- **Spanish source field:** `INDICE DE RONQUIDO/h`.
- **Missing value:** `NA`.

### 13. `spo2`

- **English meaning:** Oxygen saturation measurement.
- **Type:** Number; stored as a fraction (for example, `0.94` represents 94%).
- **Spanish source field:** `% SpO2`.
- **Missing value:** `NA`.

### 14. `minimum_o2`

- **English meaning:** Minimum oxygen measurement recorded during assessment.
- **Type:** Number; stored as a fraction in the supplied data.
- **Spanish source field:** `MÍNIMAS DE O2`.
- **Note:** The source does not specify whether this represents saturation,
  duration, or another derived quantity.

### 15. `t90`

- **English meaning:** T90 measurement recorded during sleep assessment.
- **Type:** Number; unit is not specified in the source.
- **Spanish source field:** `T 90`.
- **Missing value:** `NA`.

### 16. `prior_upper_airway_surgery`

- **English meaning:** Whether prior upper-airway surgery was recorded.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `ANTC QX EN VAS`.
- **Spanish labels:** `0 = NO`; `1 = SI`.
- **Note:** The source does not define the surgical-history time window.

### 17. `surgery_type`

- **English meaning:** Prior surgery or surgical combination recorded.
- **Type:** Categorical code.
- **English codebook:** `0 = Tonsillectomy`; `1 = Tonsillectomy, Septoplasty`;
  `2 = Tonsillectomy, Septoplasty, Turbinoplasty`; `3 = Tonsillectomy,
  Turbinoplasty`; `4 = None`; `5 = Paranasal sinuses`; `6 = Septoplasty`; `7 =
  Septoplasty, Turbinoplasty`; `8 = Turbinoplasty`; `NA = missing`.
- **Spanish source field:** `CUAL (ES)`.
- **Spanish labels:** `Amigdalectomía`; `Amigdalectomía, Septoplastia`;
  `Amigdalectomía, Septoplastia, Turbinoplastia`; `Amigdalectomía,
  Turbinoplastia`; `Ninguna`; `Senos paranales`; `Septoplastia`;
  `Septoplastia, Turbinoplastia`; `Turbinoplastia`.

### 18. `upper_airway_obstruction`

- **English meaning:** Upper-airway obstruction indicator.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `OVAS`.
- **Note:** The source dictionary does not expand the `OVAS` abbreviation.

### 19. `retracted_tongue`

- **English meaning:** Whether a retracted tongue was recorded.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `LENG RETRAÍDA`.

### 20. `elongated_uvula`

- **English meaning:** Observation of an elongated uvula.
- **Type:** Categorical code.
- **English codebook:** `0 = NO`; `1 = Not visualized`; `2 = YES`; `NA =
  missing`.
- **Spanish source field:** `UVULA ALARGADA`.
- **Spanish labels:** `0 = NO`; `1 = No se visualiza`; `2 = SI`.

### 21. `lowered_soft_palate`

- **English meaning:** Observation of a lowered or descended soft palate.
- **Type:** Categorical code.
- **English codebook:** `0 = NO`; `1 = Not visualized`; `2 = YES`; `NA =
  missing`.
- **Spanish source field:** `VELO DESCENDIDO`.
- **Spanish labels:** `0 = NO`; `1 = No se visualiza`; `2 = SI`.

### 22. `erythematous_pillars`

- **English meaning:** Observation of erythematous pillars.
- **Type:** Categorical code.
- **English codebook:** `0 = NO`; `1 = Not visualized`; `2 = YES`; `NA =
  missing`.
- **Spanish source field:** `PILARES ERITEMATOSOS`.
- **Spanish labels:** `0 = NO`; `1 = No se visualiza`; `2 = SI`.

### 23. `yawn_soft_palate_movement`

- **English meaning:** Soft-palate movement observed during the yawn maneuver.
- **Type:** Categorical code.
- **English codebook:** `0 = Reduced soft-palate elevation`; `1 = Complete
  soft-palate elevation`; `2 = No soft-palate elevation`; `3 = Not visualized
  due to high tongue dorsum`; `NA = missing`.
- **Spanish source field:** `MAN BOSTEZO - VELO`.
- **Spanish labels:** `Asciende el velo reducido`; `Asciende el velo totalmente`;
  `No asciende el velo`; `No se visualiza por dorso lingual alto`.

### 24. `yawn_uvula_movement`

- **English meaning:** Uvula movement observed during the yawn maneuver.
- **Type:** Categorical code.
- **English codebook:** `0 = Reduced uvula contraction`; `1 = Complete uvula
  contraction`; `2 = No uvula contraction`; `3 = Not observed due to high tongue
  dorsum`; `NA = missing`.
- **Spanish source field:** `MAN BOSTEZO - ÚVULA`.
- **Spanish labels:** `Contrae la úvula reducido`; `Contrae la úvula totalmente`;
  `No contrae la úvula`; `No se observa por dorso lingual alto`.

### 25. `phonation_soft_palate_movement`

- **English meaning:** Soft-palate movement observed during phonation.
- **Type:** Categorical code.
- **English codebook:** `0 = Reduced soft-palate elevation`; `1 = Complete
  soft-palate elevation`; `2 = No soft-palate elevation`; `3 = Not visualized
  due to high tongue dorsum`; `NA = missing`.
- **Spanish source field:** `MAN. FONEMA - VELO`.
- **Spanish labels:** `Asciende el velo reducido`; `Asciende el velo totalmente`;
  `No asciende el velo`; `No se visualiza por dorso lingual alto`.

### 26. `phonation_uvula_movement`

- **English meaning:** Uvula movement observed during phonation.
- **Type:** Categorical code.
- **English codebook:** `0 = Reduced uvula contraction`; `1 = Complete uvula
  contraction`; `2 = No uvula contraction`; `3 = Not visualized due to high
  tongue dorsum`; `NA = missing`.
- **Spanish source field:** `MAN FONEMA - ÚVULA`.
- **Spanish labels:** `Contrae la úvula reducido`; `Contrae la úvula totalmente`;
  `No contrae la úvula`; `No se visualiza por dorso lingual alto`.

### 27. `chewing_sign`

- **English meaning:** Sign associated with chewing.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `SIG. MASTICACIÓN`.
- **Spanish labels:** `0 = NO`; `1 = SI`.

### 28. `swallowing_sign`

- **English meaning:** Sign associated with swallowing.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `SIG DE DEGLUCIÓN`.
- **Spanish labels:** `0 = NO`; `1 = SI`.

### 29. `cardiovascular_comorbidity`

- **English meaning:** Cardiovascular comorbidity indicator.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `CO_Cardiovasculares`.

### 30. `endocrine_metabolic_comorbidity`

- **English meaning:** Endocrine or metabolic comorbidity indicator.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `CO_Endocrino_metabólicas`.

### 31. `psychiatric_comorbidity`

- **English meaning:** Psychiatric comorbidity indicator.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `CO_Psiquiátricas`.

### 32. `pulmonary_comorbidity`

- **English meaning:** Pulmonary comorbidity indicator.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `CO_Pulmonares`.

### 33. `deviated_midline`

- **English meaning:** Indicator that the midline was recorded as deviated.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `Línea_media_desviada`.

### 34. `edge_to_edge_bite`

- **English meaning:** Indicator of an edge-to-edge bite.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `Mordida_borde_a_borde`.

### 35. `anterior_open_bite`

- **English meaning:** Indicator of an anterior open bite.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `Mordida_abierta_anterior`.

### 36. `crossbite`

- **English meaning:** Indicator of a crossbite.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `Mordida_cruzada`.

### 37. `class_ii_malocclusion`

- **English meaning:** Indicator of Class II malocclusion.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `Maloclusión_clase_II`.

### 38. `class_iii_malocclusion`

- **English meaning:** Indicator of Class III malocclusion.
- **Type:** Boolean.
- **English codebook:** `0 = NO`; `1 = YES`; `NA = missing`.
- **Spanish source field:** `Maloclusión_clase_III`.

## Related files

- [English encoded CSV](../data/processed/therapy_data_encoded_en.csv)
- [English machine-readable dictionary](../data/processed/therapy_data_dictionary_en.json)
- [Spanish encoded CSV](../data/processed/therapy_data_encoded.csv)
- [Spanish machine-readable dictionary](../data/processed/therapy_data_dictionary.json)
