# GSoC 2025: InVesalius Project - Hrishav Deka

## Proposed Goals

- Implement automated testing for InVesalius.
- Ensure stability for core logic, image processing, and GUI.
- Improve contributor onboarding via CI/CD integration.

## What Was Done

Over the course of the project, I contributed **9 Pull Requests** (6 merged, 3 open) and added **70+ automated test cases** across multiple modules.  
My main work involved building a strong **pytest-based testing suite** for InVesalius, covering segmentation, mask operations, mesh generation, DICOM loading, GUI interactions, and utility functions.  
Additionally, I fixed code issues such as improper exception handling and incorrect format specifiers.

### Below are the detailed PRs with their contributions:

- **[PR #1022](https://github.com/invesalius/invesalius3/pull/1022)** – Added tests for adding, removing, and changing masks [Merged]

  - Includes 1 commit +64 lines.
  - Added test cases for creating a mask, removing a mask, and changing mask name.

- **[PR #1019](https://github.com/invesalius/invesalius3/pull/1019)** – Extended segmentation tests with Watershed [Merged]

  - Includes 2 commit +153 lines.
  - Added tests for watershed segmentation.
  - Included: `test_do_watershed()`, `test_edit_mask_pixel_orientations()`, `test_edit_mask_pixel_boundaries()`, `test_edit_mask_pixel_operation_values()`.

- **[PR #1009](https://github.com/invesalius/invesalius3/pull/1009)** – Added test for segmentation tools [Merged]

  - Includes 2 commit +161 lines.
  - Tested Region Growing, Fill Holes, and Mask Density measurement.
  - Created 2D/3D test cases using NumPy arrays.
  - Verified thresholding and density measurements.

- **[PR #1002](https://github.com/invesalius/invesalius3/pull/1002)** – Added unit tests for bone thresholding, mesh generation, STL export, and DICOM loading [Merged]

  - Includes 6 commit +632 lines.
  - `test_mesh_generation.py`: validated mesh creation, cleaning, smoothing, and up/downsampling.
  - `test_bone_thresholding.py`: tested bone segmentation on mock images.
  - `test_stl_export.py`: verified STL export/import preserves mesh geometry.
  - `test_dicom_loading.py`: tested DICOM loading, grouping, and metadata extraction.

- **[PR #947](https://github.com/invesalius/invesalius3/pull/947)** – Added pytest for `import_bitmap_panel.py` GUI components [Open]

  - Includes 4 commit +199 lines.
  - Simulated bitmap import panel operations.
  - Verified correct integration with backend and UI behavior.

- **[PR #926](https://github.com/invesalius/invesalius3/pull/926)** – Added tests for `utils.py`, `control.py`, `navigation.py`, and `data.markers.marker` [Open]

  - Includes 4 commit +909 lines.
  - Added the following test files to the Tests directory:
    - test_control.py: Unit tests for the control module.
    - test_utils.py: Unit tests for the utils module in InVesalius.
    - test_navigation.py: Unit tests for navigation module
    - test_data_marker.py: Unit test for data.markers.marker module.

- **[PR #923](https://github.com/invesalius/invesalius3/pull/923)** – Proper exception handling in `TwoWayDictionary` class [Merged]

  - Includes 3 commit +5 -4 lines.
  - Removed redundant `TypeError` handling; handled only `KeyError`.
  - Added direct key existence checks to avoid unnecessary exception handling.

- **[PR #916](https://github.com/invesalius/invesalius3/pull/916)** – Fixed incorrect format specifier in `strptime()` [Merged]
  - Includes 1 commit +5 -5 lines.
  - Corrected formatting errors that caused failures in date/time parsing.

- **[PR #907](https://github.com/invesalius/invesalius3/pull/907)** – Added pytest unit tests for `session.py`, `pubsub.py`, and `tracker.py` [Merged]
  - Includes 7 commits and +420 lines
  - Validated session handling, event-driven communication, and tracking functionality.
  - Added the following test files to the Tests directory:
    - test_session.py: Session module tests.
    - test_publisher.py: Pubsub (publisher) module tests.
    - test_tracker.py: Tracker module tests.

## What's Left

- Finalize tests for remaining core components.
