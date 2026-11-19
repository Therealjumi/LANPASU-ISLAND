LANPASU — PHASE F FULL CUSTOMIZATION ASSET PARTS v001
Built 2026-11-19 • Safe foundation: working Chin Test v006
============================================================

PURPOSE
-------
This is a NEW, standalone, automatic-loading Phase F character customization
package. It does NOT depend on the old GitHub ChinTest_EC.part01–part05 files,
the old F_EC_RealCharacter parts, three individually hosted hair GLBs, or
F_Preview_All32.glb.gz. It does NOT alter the main game or approved Chin Test.

WHAT'S INSIDE
-------------
* LANPASU_F_FullCustomization_Viewer.html — independent Phase F creator,
  63 appearance genes (61 established genes + Chin Length + Chin Shape),
  three existing gender foundations, MBTI/alignment, color, hair selector,
  movement selector, local profile save/export.
* LANPASU_F_FullCustomization_Core.html — real original E-C skinned rig with
  approved v006 chin deformation, body/face morph runtime, starter garments,
  skin/eye/brow/hair pigment controls and hairstyle fit.
* LANPASU_F_FullCustomization_Manifest.json — address map for independent
  compressed GLB records inside the new part files.
* LANPASU_F_FullCustomization.part001–part037 — 37 numbered NEW parts,
  12 MiB maximum each. Total compressed content ~442.3 MiB.
* LANPASU_F_FullCustomization_QA.json — verified part checksums, original
  GLB header checks, count of 37 hairstyles and all 32 animations.

HOW IT LOADS
------------
The model and animation library are automatically fetched from the numbered
parts when the creator opens. The first hairstyle loads automatically from
these parts; changing hairstyle fetches just that style's compressed range.
You do NOT have to choose GLB files one by one or manually pick old GitHub
assets. Internet is needed for GitHub Pages and the existing Three.js CDN.

37 original hairstyle identities from the E-B catalog are bundled. Hair_005
uses the recovered newer original '1C Long Voluminous Straight v009' because
the catalog's older v005 was not present in available source files.

GITHUB INSTALL — NO REPLACEMENTS OF APPROVED FILES
--------------------------------------------------
1. Download the ZIP provided by ChatGPT and unzip it using Files on your iPhone.
2. Open github.com/Therealjumi/LANPASU-ISLAND on branch main.
3. Open Add file → Upload files. Upload ALL files from the ZIP into the
   REPOSITORY ROOT (the folder already containing index.html).
4. You may upload in several batches; keep the EXACT file names. There are
   37 .part files, two .html files, one .json manifest, and a README/QA JSON.
   DO NOT upload the ZIP itself. Each individual part is under 25 MB.
5. Commit each upload batch. Verify all part001–part037 are present.
6. Visit:
   https://therealjumi.github.io/LANPASU-ISLAND/LANPASU_F_FullCustomization_Viewer.html

DO NOT delete or overwrite these working originals:
* index.html
* LANPASU_Phase_F_Character_Creator_Interface.html
* LANPASU_F_RealModel_Core.html
* LANPASU_F_ChinTest_Core.html
* LANPASU_F_ChinTest_Viewer.html
* LANPASU_F_ChinTest_EC.part01 through .part05
* Any of your original animations, body models, or hairstyles.

WHAT IS READY AND WHAT ISN'T
----------------------------
READY IN THIS PACK (structural):
* Real approved chin v006 deformation with 50/50 original neutral values,
  female / neutral-intersex / male existing foundations; 117-bone E-C rig.
* 63 slider/data entries, starter garment set fitted to foundation.
* All 32 original movement animations, 8 styles x Idle/Walk/Run/Jump.
* All 37 hair GLBs packaged with lazy loading. 24 are Teen+ entries;
  13 are Baby/Toddler/Child assets kept for future age integration.
* New self-contained part files and loader, no dependence on prior model
  or hairstyle part filenames.

NOT COMPLETED BY THIS PACKAGE:
* Age 0–100 body modeling/skin integration. Although age is saved, the
  rendered E-C character remains adult as before. Child/toddler/baby hair
  will only be age-correct after the future E.1 character-model integration.
* Full clothing wardrobe beyond the existing E-C starter garments.
* Automated transfer of finished custom characters into the game,
  persistent in-game player save, NPC creation/genetic inheritance.
* Live Safari visual verification of the entire new package or all 37
  hairstyles. Dense original hair GLBs can be large and may stress iPhone RAM.

TEST IN ORDER
-------------
A. Open the new FullCustomization_Viewer.html and wait for character/model
   ready, not merely the character illustration.
B. Set Chin Length=50 and Chin Shape=50, then test both extremes and check
   the mouth seam and neck protection on all three foundations.
C. Test Hair_001, Hair_005 (v009), a long coily style (e.g. Hair_019),
   and a dense 4C style only if Safari memory allows.
D. Switch Idle, Walk, Run, Jump through a few of the eight movement styles.
E. Verify changing hair, face, body and color does not reset unrelated genes.

PACK DETAILS
------------
The .part files are consecutive slices of a contiguous binary container of
39 independently gzip-compressed glTF GLB records. Entries may span part
boundaries. The JSON manifest maps exact compressed offsets and checksums.
The browser decompresses the requested record only, not the entire 442 MiB
asset container. Do not rename or combine parts by hand.

No existing repository files were changed during construction of this ZIP.
