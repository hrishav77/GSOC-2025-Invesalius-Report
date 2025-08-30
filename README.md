# GSoC 2025: InVesalius Project - Hrishav Deka

## Proposed Goals

- Implement automated testing for InVesalius.
- Ensure stability for core logic, image processing, and GUI.
- Improve contributor onboarding via CI/CD integration.

## What Was Done

Over the course of the project, I contributed **9 Pull Requests** (6 merged, 3 open) and added **70+ automated test cases** across multiple modules.

My main work involved building a strong **pytest-based testing suite** for InVesalius, covering segmentation, mask operations, mesh generation, DICOM loading, GUI interactions, and utility functions.  
Additionally, I fixed code issues such as improper exception handling and incorrect format specifiers.

### Detailed PR Contributions

**[PR #1022](https://github.com/invesalius/invesalius3/pull/1022)** – Added tests for adding, removing, and changing masks [Merged]

- 1 commit, +64 lines
- Test cases for creating, removing, and renaming masks

**[PR #1019](https://github.com/invesalius/invesalius3/pull/1019)** – Extended segmentation tests with Watershed [Merged]

- 2 commits, +153 lines
- Added `test_do_watershed()`, `test_edit_mask_pixel_orientations()`, `test_edit_mask_pixel_boundaries()`, `test_edit_mask_pixel_operation_values()`

**[PR #1009](https://github.com/invesalius/invesalius3/pull/1009)** – Added test for segmentation tools [Merged]

- 2 commits, +161 lines
- Tested Region Growing, Fill Holes, and Mask Density measurement
- Created 2D/3D test cases using NumPy arrays

**[PR #1002](https://github.com/invesalius/invesalius3/pull/1002)** – Added unit tests for bone thresholding, mesh generation, STL export, and DICOM loading [Merged]

- 6 commits, +632 lines
- `test_mesh_generation.py`: validated mesh creation, cleaning, smoothing, up/downsampling
- `test_bone_thresholding.py`: tested bone segmentation
- `test_stl_export.py`: verified STL export/import
- `test_dicom_loading.py`: tested DICOM loading, grouping, metadata extraction

**[PR #947](https://github.com/invesalius/invesalius3/pull/947)** – Added pytest for `import_bitmap_panel.py` GUI components [Open]

- 4 commits, +199 lines
- Simulated bitmap import panel operations
- Verified correct backend/UI integration

**[PR #926](https://github.com/invesalius/invesalius3/pull/926)** – Added tests for `utils.py`, `control.py`, `navigation.py`, `data.markers.marker` [Open]

- 4 commits, +909 lines
- New tests:
  - `test_control.py` – control module
  - `test_utils.py` – utils
  - `test_navigation.py` – navigation
  - `test_data_marker.py` – markers

**[PR #923](https://github.com/invesalius/invesalius3/pull/923)** – Proper exception handling in `TwoWayDictionary` class [Merged]

- 3 commits, +5/-4 lines
- Removed redundant `TypeError` handling, handled only `KeyError`
- Added direct key existence checks

**[PR #916](https://github.com/invesalius/invesalius3/pull/916)** – Fixed incorrect format specifier in `strptime()` [Merged]

- 1 commit, +5/-5 lines
- Corrected formatting errors in date/time parsing

**[PR #907](https://github.com/invesalius/invesalius3/pull/907)** – Added pytest unit tests for `session.py`, `pubsub.py`, and `tracker.py` [Merged]

- 7 commits, +420 lines
- Tests added:
  - `test_session.py` – session handling
  - `test_publisher.py` – pub/sub events
  - `test_tracker.py` – tracker

## Current State

- InVesalius now has a **robust pytest suite** covering core logic and workflows.
- Critical functionality (segmentation, STL export, DICOM loading, session management) is now automatically verified.

## What’s Left


## Code Status

- **Merged upstream:** [#1022](https://github.com/invesalius/invesalius3/pull/1022), [#1019](https://github.com/invesalius/invesalius3/pull/1019), [#1009](https://github.com/invesalius/invesalius3/pull/1009), [#1002](https://github.com/invesalius/invesalius3/pull/1002), [#923](https://github.com/invesalius/invesalius3/pull/923), [#916](https://github.com/invesalius/invesalius3/pull/916), [#907](https://github.com/invesalius/invesalius3/pull/907)
- **Open:** [#947](https://github.com/invesalius/invesalius3/pull/947), [#926](https://github.com/invesalius/invesalius3/pull/926)

---

## Challenges and Learnings

- Initially struggled with **open-source workflows** (PRs, branches, and reviews), but developed confidence after learning from mentors.
- Understanding the **large and complex codebase** was difficult because tests involved several modules, but it substantially enhanced my debugging and reading abilities.
- Key takeaways: 
  - Create effective and maintainable **pytest tests**.
  - Using **wxPython GUI** code for testing.
  - Using mentor feedback to improve contribution structure and code practices.

Overall, this project made InVesalius more stable and maintainable, while giving me valuable real-world experience in open-source testing and collaboration.
