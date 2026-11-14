LANPASU — MASTER README
Environment Test v007 + Island v011 Stone Arcade / Collision v007 Props
Updated 2026-11-14 (local)

1. WHAT TO KEEP AND USE
The current game code is v007 index.html (replace the hosted v006 file). It contains the player
controller, physics, camera, lighting and ocean. The README is only a
reference; it does not need to be uploaded or selected to play.

Game website: https://therealjumi.github.io/LANPASU-ISLAND/

Select these files in the game's setup screen, in order:
  1. Complete island: Lanpasu_Island_v011_StoneArcade.glb
  2. Collision: Lanpasu_Collision_v007_Props.glb
  3. Routes: Lanpasu_Traversal_v003_routes.json
  4. Ladar: Ladar_Rig_v108_Height_5ft6.glb
  5. Idle: your compatible Ladar Idle GLB
  6. Walk: your compatible Ladar Walk GLB
  7. Run: your compatible Ladar Run GLB
  8. Jump: your compatible Ladar Jump GLB
  9. Water (optional): Lanpasu_Terrain_v004_Water_Placeholders.glb

There are eight required files and one optional water file. Use the actual
movement clips, not copies of the rig. The precise filenames of the four
movement clips can vary. Do not load the separate terrain, traversal and
vegetation layers in addition to the complete island; it already includes
those pieces. The route JSON's older model names are historical metadata;
the game accepts the current replacement files in the selected fields.

ARCHITECTURE ASSETS (development library; not extra game inputs):
  Standard Modern Hut v001 and its collision model.
  Four hut variations and matching collision models.
  District Buildings v001: nine landmark/facility models and collisions.
  Separate Vegetation v003 Sunny: reusable assets and positioned layer.
Keep these originals in Environments / Architecture and Vegetation.
The current complete island and collision GLBs already contain the placed
buildings, all seven market stalls and placed environmental props. Do not load the standalone assets into the game separately.
See Section 11 for the architecture integration release notes.

2. IPHONE / SAFARI SETUP
Open the game website in Safari (not just the Files preview of index.html).
Tap Choose File for each field and browse to your saved models in Files.
Select the eight required files and optional water, then tap Start Test.
Internet is needed to load the Three.js and BVH libraries. The model files
are selected locally, not uploaded to GitHub by this setup. The GitHub
repository and hosted HTML are public. For a future code update, replace the
repository's root index.html; keep Pages set to main / (root). No GitHub
code change is required for the Sunny Island / Solid Collisions update,
the Red Spot Fix, the Stair Flicker Fix, the Architecture update, Markets integration,
Props integration, the Fruit Crate Fix, the Solavren finishing pass, or the Stone Arcade update.
Use Island v011 and the unchanged Collision v007 Props GLB in the current v007 HTML.
For this Step 10 code update, replace the repository root index.html.

3. CONTROLS
Joystick: move relative to the camera; small input = slower movement.
RUN: toggle run/walk. JUMP: jump. Release joystick: return to idle.
Swipe: orbit camera; pinch: zoom; Center: return behind Ladar.
Reset: return to Solavren. Collision: display/hide collision geometry.
Desktop alternatives include WASD/arrows, Shift, Space, Q/E, C and zoom keys.

4. DEVELOPMENT HISTORY (BEGINNING TO CURRENT)
World foundation: seven districts — Solavren (market square), Nayvokel
(sea cave), Coravell (campus), Veluross (beach club), Embravael (volcano),
Marivoh (marina/lighthouse), Ruvelocn (ruins/jungle).
Ladar v108: intended 5 ft 6 in / 1.6764 m; 1 game unit = 1 meter, Y up.
Terrain v001 foundation; v002 color and rock refinements; v003 shape;
v004 color; v005 bright palette. Traversal v003: paths, stairs, bridges,
railings and collision meshes. Spawn: X=0, Y=14.393, Z=25 (Solavren).
Vegetation v001: blue foliage, light tan trunks; v002 bright correction.

Game v001 — Initial HTML, local GLB/JSON loader, basic movement, collision,
camera and lighting. (Summary reconstructed from the original v001 HTML.)
Game v002 — Player controller: analog joystick, camera-relative movement,
acceleration/braking, run toggle, buffered jump, animation crossfades and
speed adjustment. Root translation/scale animation tracks excluded.
Game v003 — Physics: 120 Hz fixed step, capsule contacts, 48 degree slope
limit, 0.23 m step-up, ground snap, fall subdivision and reset. Collision
visualization for debugging.
Game v004 — Camera: swipe orbit, pinch zoom, center behind Ladar, multiple
collision rays. Desktop camera keys added.
Game v005 — Lighting/ocean: bright sky, sun, clouds, ambient/directional
light, animated ocean, shoreline proximity texture, ripples/foam, optional
water surface effects and lightweight character contact shadow.
Asset update (after game v005) — Sunny Island v003 and Solid Collisions
v004. Brighter warm stone and cream sand, blue foliage, light tan wood;
1,541 vegetation placements receive simplified solid proxies; the 239
existing rock collision components are retained. Same HTML and spawn JSON.
Island v004 — Red Spot Fix: nine accidental red pathway junctions
restored to natural beige; intentional volcanic lava colors preserved.
Island v005 — Stair Flicker Fix: redundant overlapping faces removed
across 14 traversal meshes. Visible stair shapes, palette, vegetation,
railings and district layout preserved; collision ramps unchanged.
Architecture v001 — First reusable medium family hut and its separate
collision model created. Standalone originals retained for future editing; see Sections 10 and 11.

5. CURRENT TEST STATUS / KNOWN LIMITATIONS
The Safari setup page has been opened and initial gameplay tested by the
user. Initial feedback: too grey, and vegetation/rocks could be walked
through. Replacement models above address the palette and vegetation
collision geometry. User subsequently described traversal as mostly perfect, with
stair texture flickering. Island v005 addresses overlapping faces; its
Safari behavior has not been independently verified.
Test a tree trunk, large rock and bush, then stairs, bridges and jumps.
Rotate the camera on stairs to check for flickering. If it persists,
inspect depth rendering in the game. The architecture collection is now integrated; it has not yet been
tested in Safari. See Section 11 for the specific test plan.
If rocks remain walk-through, inspect the physics code rather than assuming
the geometry fixes the problem. Proxy shapes are simplified and may need
adjustment. Animation matching and speeds remain provisional. Water is
visual only, no swimming or fluid physics. Full mobile performance and
camera behavior with the new collision file are not yet verified.

6. WORLD DEVELOPMENT CHECKLIST
[x] 01 Island map / seven districts
[x] 02 Universal scale / Ladar v108
[x] 03 Terrain foundation and visual refinements
[x] 04 Traversal and collisions — initial development complete; retest fixes
[x] 05 Native vegetation — models created; sunny palette and proxies added
[~] 06 Modern hut houses and buildings — models placed; gameplay testing pending
[~] 07 Open-air markets and stalls (no shopping malls) — seven models and collisions integrated; Safari testing pending
[x] 08 Environmental props — 50 placements integrated; initial Safari test observed
[~] 09 Assemble Solavren — visual finishing pass integrated; Safari retest pending
[x] 10 Water, sky and lighting — v006 visual polish approved by user
[~] 11 Finalize Ladar, camera and physics — v007 refinement created; Safari testing pending
[~] 12 iPhone testing and optimization — initial test done, fixes pending

7. FILE ORGANIZATION
LANPASU GAME / Game Code: current index.html and this MASTER README.
LANPASU GAME / Environments: Complete Island, Collisions, Traversal, Water,
Vegetation, Architecture, Market & Stalls and Props. Keep Island v011 and Collision v007 in their
respective folders. Standalone house and landmark GLBs stay in Architecture.
Older complete island and collision versions are optional archive backups.
LANPASU GAME / Characters: Ladar rig and four movement animations.
LANPASU GAME / Archive: older code/models/readmes, optional backups only.
You do not need older README files to play, and this master supersedes
prior setup instructions that list the old island or collision models.

8. ORIGINAL V005 RELEASE NOTES — WORLD LIGHTING & OCEAN
Historical release instructions, preserved verbatim. For current asset
filenames and setup, follow Sections 1 and 2 above. The v005 HTML was current at that release; the later Sunny Island / Solid Collisions update replaces two
GLBs only and does not require another HTML update.

LANPASU Environment Test v005 — World Lighting & Ocean

Replace your old index.html with this ZIP's index.html. Host over HTTPS and open in Safari. Select the same eight required files; select the existing water GLB if you want animated waterfall/pool surfaces. The ocean is built in. Internet is required to load the pinned Three.js and BVH modules.

New: bright sky gradient, sun and clouds, warm directional sunlight, cool ambient lighting, animated ocean with baked shoreline proximity, surface ripples and foam, optional animated water surfaces and lightweight character contact shadow. All existing v004 control, collision, camera and animation code retained. No new GLB files.

Water animation is visual only; no swimming, fluid simulation, or splash physics. The shoreline texture is derived from Terrain v005 Bright, so update it if geography changes. This build needs browser and iPhone testing; shadow and shader appearance may vary by GPU.



9. ISLAND FIX RELEASE NOTES — RED SPOTS AND STAIRS
Island v004 RedSpotFix: Lanpasu_Island_v004_RedSpotFix.glb.
Restores nine red pathway junctions to beige. Only vertex colors changed;
intentional lava, geometry, placements and collision data are preserved.
This version is superseded by Island v005.

Island v005 StairFlickerFix: Lanpasu_Island_v005_StairFlickerFix.glb.
Removes redundant overlapping faces in 14 traversal meshes to address
likely Z-fighting. Retains prior color correction and island layout.
Historical: it was used with Lanpasu_Collision_v004_Solid.glb.
Both are superseded by the architecture integration files in Section 1.
Keep the current routes JSON, Ladar files, water GLB and v005 HTML.
No GitHub update needed. Retest stair appearance and movement in Safari.
These notes summarize the development updates; the original fix ZIPs
contain the GLB models only.

10. ORIGINAL MODERN HUT V001 README — ARCHITECTURE
The following is the original README from LANPASU_ModernHut_v001.zip.

LANPASU Modern Hut v001
Standalone reusable family house. Visible GLB and separate collision GLB share the same local origin (ground level), Y-up, front +Z, meters. Body 7.2 x 5.8 m, deck 0.90 m above ground, doorway 1.21 m clear x 2.23 m high. Place both files with identical translation, rotation and scale. Integrate the collision geometry into the island collision system; do not render it in normal gameplay. This model has an unfurnished interior and open doorway; windows are solid blue-tinted panes. Not yet placed on the island or tested in Safari.

Additional organization and development notes:
  Visible model: Lanpasu_ModernHut_v001.glb
  Collision: Lanpasu_ModernHut_Collision_v001.glb
  Save both in LANPASU GAME / Environments / Architecture.
  ADD these files; do not replace current island or collision files.
  Design: light tan timber, layered golden thatch, blue-tinted windows,
  raised veranda, entrance stairs and open doorway. Total height 6.19 m.
  The collision model includes solid walls, windows, floor, roof,
  supports, railings and a smooth stair ramp. Integrate both models at
  matching transforms when placing houses on the island.
  Next: review the standard hut, then create house variations, district
  buildings and their matching collisions before world assembly.


11. ARCHITECTURE INTEGRATION — ISLAND V006 / COLLISION V005
Current release: replace ONLY the Complete Island and Collision GLBs.
Visible: Lanpasu_Island_v006_Architecture.glb
Collision: Lanpasu_Collision_v005_Architecture.glb
Keep the v005 HTML, spawn/routes JSON, Ladar rig and animation files, and
optional water GLB. No GitHub change or new setup fields required.

Development asset collection: five house types (standard family, small,
large family, two-story, round coastal), nine district landmarks/facilities,
and the two separate Sunny vegetation GLBs. Keep standalone source assets
and matching collisions for future placement/editing, not extra game inputs.

Placed 16 instances: nine landmarks and seven residential huts.
Coravell: campus and athletics field.
Marivoh: lighthouse and round coastal hut.
Solavren: community pavilion and four residential huts (standard, small,
large family, two-story). The central market paving and spawn are reserved.
Nayvokel: command base on the lower cave floor.
Veluross: beach lounge and two additional residential huts.
Embravael: laboratory entrance and hot spring shelter.
Ruvelocn: ancient sanctuary.

Original terrain, traversal geometry, sunny colors, stair flicker fix,
water alignment, and world coordinate scale retained. New building sites
use small foundation plinths and short local ramps where appropriate.
140 plant instances and their corresponding solid proxies were removed
from building footprints and entrance approaches; 1,401 remain. Existing
rock, terrain and traversal collisions are preserved. All building visual
and collision placements share the same meter-based transforms.

Lanpasu_Architecture_Placement_v001.json records placement coordinates,
rotation, source assets and planned ground approaches. This is a developer
reference only, not a replacement for the original routes/spawn JSON.
Approach paths are clearance-planned ground routes, not new paved roads.

Validation: both GLBs were reloaded. Original visual mesh/material/buffer
data was preserved. The existing collision buffer was preserved and the
vegetation proxy face indices updated. All 16 locations have planned ground
approaches to existing routes; 2,767 sampled existing route centerline
positions showed no new architecture collision interference in the static
check. This is not a complete runtime traversal or phone performance test.

Safari test: spawn in Solavren; walk to a hut, enter/exit and check walls,
steps, and floors; check the campus entrances/athletics, coastal approaches,
ruins, hot spring shelter and cave base. Confirm the original stairs,
bridges and railings still work. Check frame rate with the larger island.
Lighthouse upper balcony access remains unfinished; school, lab, command
base and lounge interactions and furnished residential interiors are not
implemented. Some approaches are unpaved and may need gameplay adjustments.
Next: complete architecture placement testing, then Step 07 markets/stalls.


12. OPEN-AIR MARKETS & STALLS v001 — DEVELOPMENT ASSETS
Historical standalone release: seven visual/collision GLB pairs. Now placed in Island v007; see Section 13.
Collection: LANPASU_Market_Stalls_v001.zip. Save under Environments /
Market & Stalls. Contains Produce, Clothing, Crafts, Cafe, IslandFood,
Arcade and Tailor models, matching collision files, manifest and previews.
Filenames: Lanpasu_Market_<type>_v001.glb and
Lanpasu_Market_<type>_Collision_v001.glb. Meter scale, Y up, +Z front;
origin at ground center. Apply identical transforms to each visual and
collision pair. Timber frames, pastel fabric canopies and thatch roofs,
open entrances and decorative merchandise. Simplified solid proxies for
structural pieces and larger fixtures. Small goods are decorative.
The standalone release made no changes to the playable island, collision file, route JSON or HTML.
Do not load these standalone files into the current game's setup fields.
Original next step (completed in Section 13): place stalls around Solavren while preserving spawn and walking lanes,
clear conflicting vegetation where necessary, merge visuals and colliders,
and test customer access, collisions and iPhone performance. Shopping,
vendors, minigames and tailoring interactions are not implemented yet.


13. MARKET INTEGRATION — ISLAND V007 / COLLISION V006
Step 07 placement pass. All seven original market models are now placed
in Solavren's reserved central square. West: Produce and Clothing;
north: Tailor and Arcade; south: Crafts, Cafe and IslandFood. All face
the interior pedestrian area. The central gathering space and existing
route network remain open. Each stall has a low foundation and short
front approach ramp; matching collision transforms preserve solid
counters, posts, floors and major equipment.

REPLACE in the game setup:
  Lanpasu_Island_v006_Architecture.glb -> Lanpasu_Island_v007_Markets.glb
  Lanpasu_Collision_v005_Architecture.glb -> Lanpasu_Collision_v006_Markets.glb
Keep the v005 HTML, Traversal v003 routes JSON, Ladar rig and animations,
and optional water GLB. No GitHub changes needed. Archive the old pair
together. Keep all standalone building, plant and stall assets.

ADD for development: Lanpasu_Market_Placement_v001.json in Market & Stalls.
Contains positions, yaw, front approach coordinates and source filenames.
It is not a game input or a replacement for the traversal JSON.

Validation: both new GLBs reloaded successfully. All original visual and
collision data preserved; no new vegetation removals were necessary.
1,401 placed plants and the 16 architectural structures remain. 14,505
sampled existing route centerline positions showed no new market collision
interference in the static capsule-distance check. Stall footprints do not
overlap. Terrain heights sampled for foundation/ramp placement; no change
to the island geography or spawn (0, 14.393, 25).

Safari test: walk from spawn to the market center; approach each stall,
check counters/posts, enter clothing and arcade stalls, walk around the
perimeter and continue along original routes. Check ramp transitions and
frame rate. This is a static geometric check, not a completed phone test.
Vendors, purchases, tailoring, arcade games and other interactions remain
unimplemented. Next: Step 08 Environmental Props, after market review.


ENVIRONMENTAL PROPS v001 — STEP 08
LANPASU — Environmental Props v001

14 reusable prop sets, each with a visible GLB and matching simplified collision GLB. Units: meters; Y up; +Z front (boats +Z bow). Land props origin ground center; boats origin keel center, adjust to waterline when placing. Keep paired visual and collision transforms identical. Assets are standalone, not integrated into Island v007 Markets. Do not select them in place of existing complete island or collision GLBs. Save the collection under Environments / Props. Manifest lists file names, bounds, triangle counts, groups and usage notes. Preview images are optional. Solid supports, furniture and hull proxies are supplied; small decoration, cloth and sails are visual only. Boats are static scenery, not rideable, and lanterns do not cast live light. No sitting, boating or interaction logic yet. Placement, access clearance and Safari testing remain next steps.

Assets: Timber street lantern, District banner, Timber promenade bench, Outdoor cafe table and chairs, Island wayfinding sign, Blue foliage planter, Wooden harbor crate stack, Wooden storage barrel, Dock mooring bollard, Marivoh wooden sailboat, Small fishing skiff, Beach umbrella and two loungers, Hot spring stone lantern, Ruvelocn carved stone marker.
Current playable island, collision, routes, water, character files and HTML remain unchanged.


14. PROPS INTEGRATION — ISLAND V008 / COLLISION V007
Step 08 placement pass: 50 prop instances from all 14 reusable types,
across all seven districts. Solavren 13, Coravell 7, Marivoh 12,
Nayvokel 3, Veluross 7, Embravael 4, Ruvelocn 4. Two sailboats and two
fishing skiffs are static in the harbor; one mooring bollard is on the
shore-side harbor approach, not the narrow boardwalk. Low timber support
pads anchor selected props on uneven terrain. The market center, spawn,
existing paths and planned building/stall approaches were protected.

CURRENT FILES — REPLACE THE PREVIOUS MATCHED PAIR:
  Lanpasu_Island_v007_Markets.glb -> Lanpasu_Island_v008_Props.glb
  Lanpasu_Collision_v006_Markets.glb -> Lanpasu_Collision_v007_Props.glb
Keep v005 index.html, Traversal v003 routes JSON, Ladar v108 rig and
animations, optional water GLB. No new HTML or GitHub upload required.
Keep all reusable props, house, market, district and vegetation assets.
ADD Lanpasu_Props_Placement_v001.json to Environments / Props. This is
development metadata, not a substitute for Routes & Spawn. Keep this
Master README in Game Code; preview PNGs are optional.

VALIDATION: Both GLBs reload successfully. Original GLB binary data and
existing nodes/meshes/accessors/materials remain unchanged; new prop
geometry is appended, with visual materials batched and one additional
collision mesh. 14,505 existing route centerline samples checked with
three capsule-height probes: zero new prop collision hits. Static
terrain/footprint checks performed; no vegetation removed, original
spawn (0, 14.393, 25) and the terrain remain unchanged. The 16 building
placements and seven market stalls remain. This is not a live Safari test.

TEST NEXT: Walk around tables, benches, planters, and lantern poles;
check shoreline, cave, and beachfront. Check frame rate and camera
behavior. Boats are decorative, not rideable, lanterns have no live
lights, and sitting/boating/shop interactions are not implemented.
Signposts remain blank decorative wayfinding signs.
Next: Step 09 — Assemble Solavren, final district detailing and layout.


16. ISLAND v009 — FRUIT CRATE FIX (HISTORICAL)
Source: Island v008 Props. User reported flickering fruit crates in the
Solavren produce stall during Safari testing. Six crates received targeted
geometry corrections at overlapping wood panel joints. No change to the
rest of the island, palette, placements, routes, or Collision v007 Props.
The v010 model is derived from this corrected v009 file, not v008.
The user reported the market was almost perfect aside from this issue;
56 FPS was visible in a single Safari screenshot, not a full performance benchmark.

17. ISLAND v010 — ASSEMBLE SOLAVREN / VISUAL FINISHING PASS
Historical playable visual model (superseded by v011): Lanpasu_Island_v010_Solavren.glb
Current collision model: Lanpasu_Collision_v007_Props.glb (unchanged).
Source: Lanpasu_Island_v009_FruitCrateFix.glb.
The illustrated district map remains the layout reference; the second
image was used for atmosphere only, not a mandate to add modern towers.
- Existing Solavren market-square paving now has embedded warm limestone
  patterning and a 5.1 m circular eight-point compass/flower mosaic at
  X=0, Z=38.8. The original uneven ground is preserved.
- All seven existing vendor sign faces receive descriptive labels with
  their original central emblems retained. No new geometry or colliders.
- Original mesh positions, indices as geometric triangles, all building
  and prop transforms, vegetation, terrain, routes, and the v009 crate
  fix are preserved. Seven sign meshes split their existing front faces
  into a new textured primitive; the plaza uses a new embedded material.
- No extra floor mesh: textures are applied directly to the original
  paving surface, avoiding a new overlapping decal surface.
- Existing landscaping and furniture retained, no new structures,
  buildings, vegetation or stalls placed in this pass.
- Eight embedded PNG textures; all are inside the GLB. No sidecar texture
  files required by the game.

Install: replace the Complete Island GLB with v010. Retain Collision
v007 Props, Traversal v003 routes JSON, Ladar v108, all four animations,
optional water GLB and hosted v005 index.html. No GitHub upload needed.
Keep the separate detail JSON and paving PNG as optional development
assets; neither is a game input. Replace the previous Master README.

Validation: the new GLB was reloaded and an actual mesh preview rendered.
Original node transforms and vertex/geometry binary data are retained;
only the paving material and seven sign-face material assignments change.
Safari rendering of the new textures is not yet tested. Check the mosaic
and stall lettering from Ladar's perspective, walk across the plaza,
rotate the camera near the fruit crates and test all market approaches.
Step 09 is visually assembled; gameplay review remains. Next planned
step: 10, ocean, waterfalls, sky and lighting polish.


18. ISLAND v011 — STONE ARCADE / TECHNOLOGY IMMERSION
Source: Lanpasu_Island_v010_Solavren.glb.
Current playable visual model: Lanpasu_Island_v011_StoneArcade.glb.
Current collision model: Lanpasu_Collision_v007_Props.glb (unchanged).
LANPASU technology rule: Lanpasan wood holds structures together; stone
provides power. Electronics use polished stone screens powered by approved
island energy. The arcade now follows that visual language.
- Only the three arcade cabinets in the existing Solavren stall are edited.
- Blue-grey slate, warm limestone and rose sandstone bodies have embedded
  mineral-grain textures, softly chamfered corners and stone control ledges.
- Existing screen graphics, buttons and joysticks remain, with darker stone
  screen frames and subtle emissive screen materials.
- Original stall structure, sign, mosaic, paving, placements, fruit-crate
  fix, other buildings and world geometry are preserved. All original binary
  data is retained; only the targeted arcade mesh references and new geometry
  and material data change. No new floor, no new collision file.
- Updated reusable asset: Lanpasu_Market_Arcade_v002_Stone.glb. Replace
  the old standalone arcade visual in Market & Stalls / Arcade; retain
  Lanpasu_Market_Arcade_Collision_v001.glb. The revised standalone
  Market_Stalls_manifest_v002.json records this asset revision.
- Install: use v011 in the Complete Island field of the existing v005 game.
  Keep Collision v007 Props, routes, Ladar, animations, water and HTML.
  No additional textures to load, no GitHub change.
- Validation: both revised GLBs reload; the new cabinet surfaces stay inside
  the old cabinet dimensions and the stall placement is unchanged. Rendered
  close-up is an actual mesh preview, not a Safari screenshot. Test screen
  appearance, approach and controls in Safari. Arcade mini-games, live
  touch-input programs and island-energy mechanics remain unimplemented.
- Scope: other electronic devices across LANPASU were not changed.
Step 09 finishing/immersion polish; next planned Step 10 lighting and water.


STEP 10 — GAME CODE v006: TROPICAL VISUAL POLISH
Current installation overrides older v005 code instructions in this history.
Replace the GitHub repository root index.html with the v006 index.html in
LANPASU_Visual_Polish_v006.zip. Keep Pages main / (root), open the existing
HTTPS game in Safari, and reload after deployment. No GLB or route changes.
Select Island v011 StoneArcade, Collision v007 Props, Traversal v003 routes,
Ladar v108 and the same four animation files. Select the existing optional
Water_Placeholders v004 GLB to see waterfalls and hot spring effects.
Visual quality: Sunny enables a local 1024px shadow map, refreshed when
the player crosses a 4 m grid boundary. Lightweight disables the shadow
map but retains lighting, ocean, sky, water flow, mist and contact shadow.
New: reduced exposure/fill, neutral tone mapping, warm directional light,
blue sky gradient with procedural clouds, turquoise shallows, deeper blue
sea, animated shoreline foam, stylized ripple/caustic patterns, flowing
waterfall streaks and lightweight mist/steam. Ocean level and shoreline
texture unchanged. Boats, existing water geometry and all island assets
remain untouched. Water is visual only, not swimming or fluid simulation.
No live lantern lights, day/night cycle, underwater transparency or new
waterfall geometry. Local shadows are static scenery only; Ladar retains
her contact shadow. Mobile shader appearance, shadow artifacts and FPS
require Safari testing. If performance drops, restart in Lightweight.
The previous v005 HTML remains a rollback option.
Step 10: code created; visual review and performance testing pending.
Step 11: existing movement/camera/physics still in place; final validation
pending. Step 12: full-world iPhone testing and optimization pending.


STEP 11 — GAME CODE v007: LADAR MOVEMENT, CAMERA & PHYSICS
Current installation: replace hosted root index.html with v007 from
LANPASU_Movement_Refinement_v007.zip. Keep GitHub Pages main / (root).
Do not upload the models. Open Safari and reload after deployment.
All current GLBs, routes JSON, and v006 rendering code remain unchanged.
Use the exact uploaded Idle.glb, Walk.glb, Run.glb and Jump.glb. Their
source durations are 12 s, 4.2 s, .86 s and 1.25 s; all named animation
targets exist in the v108 rig. No skeleton or GLB was edited.
Movement pace: Measured (default) .48 m/s walk and 1.45 m/s run,
chosen to reduce sliding with short source strides. Travel keeps the
original 1.65 / 4.1 m/s top speeds; foot sliding may still be visible.
Analog input, eased acceleration/braking, speed-based playback,
normalized animation blend weights, walk/run phase continuity and
movement hysteresis. Jump uses authored knee bend (.14 s preparation),
velocity-driven flight pose, and .24 s landing recovery. Duplicate
large vertical pelvis translation is reduced at runtime; the original
clip stays intact. Gravity 14 m/s2, launch 5 m/s, nominal .875 m jump
height on flat ground. Fixed 120 Hz capsule physics retained; ground
snap now checks capsule clearance, and camera follow is softened with
bounded horizontal and vertical lag and existing collision rays.
Validation: uploaded base HTML and five other base assets match previous
versions byte-for-byte. All four animation target name sets match the rig.
JavaScript syntax and synthetic flat-ground state checks passed: jump
prep, flight, land, idle; walk/run/stop and normalized blend weights.
The test uses simplified flat-ground contact, not a browser or WebGL.
Actual stair, doorway, bridge, animation appearance, hair/skirt movement,
camera collision, and iPhone performance still need hands-on testing.
No full foot IK, swimming, interaction system or gameplay activities yet.
Step 11: implementation ready for Safari review. Step 12: full island
playtesting and optimization remain. v006 HTML is the rollback option.


STEP 11 CORRECTION — GAME CODE v008: STAIR & MOVEMENT FIX
Current installation: replace GitHub Pages root index.html with v008
from LANPASU_Stair_Movement_Fix_v008.zip. Keep all existing GLBs and JSON.
The latest v008 instructions supersede the v007 pace and ground snap.
User reported walking/running too slow and stairs no longer climbable.
Default Natural / Travel restores v006 1.65 m/s walking, 4.1 m/s running,
and original acceleration/braking. Relaxed is 1.15 / 3.0 m/s. The original
very slow .48 / 1.45 m/s mode is removed. Animation playback remains
speed-sensitive with capped rate (walk 1.7x, run 1.65x); travel may still
have visible foot sliding because source clips have short strides.
Restore v006 ground snap and floor probe. Preserve original capsule
solver, bounded step lift, slope limit, rail/wall blocking, jump physics,
new jump phase timing, animation blending and v007 camera. Step acceptance
uses a proportional progress tolerance for small joystick increments,
so the .005 m threshold cannot exceed the entire requested displacement.
Validation: JavaScript syntax, synthetic flat-ground movement and jump
state tests, and synthetic step-acceptance tests (small/normal increments,
tall obstacle/wall rejection) pass. These use simplified contacts, not
actual Three.js BVH gameplay; actual stair climbing on the island remains
unverified. We cannot identify the specific stair from the report alone.
Test the same stairs in Natural / Travel, then Relaxed. If still blocked,
try the v006 rollback and report the district/stair and HUD XYZ coordinates.
All island/collision/water/rig/animation models, route JSON and visual
rendering remain unchanged. Step 11 awaiting user retest; Step 12 pending.
