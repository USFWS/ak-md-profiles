# Alaska Region mdEditor profiles

The [mdEditor](mdEditor) is designed to support creating metadata for a wide variety of data types. As a result, an edit session will likely display much more information than is required for the data that you are describing. Applying a profile allows a user to hide menus and data entry fields that may not be required for a given use case.

The mdEditor defaults to the "Full Profile" when a metadata record is first created, displaying all available menus and data entry fields.

When editing a record, a [Profile Selection](https://guide.mdeditor.org/tutorial/editor-window-parts/primary-navigation.html#profile) field is displayed on the mdEditor [Primary Navigation Bar](https://guide.mdeditor.org/tutorial/editor-window-parts/primary-navigation.html). A selected profile will remain associated with metadata record unless changed during a subsequent edit session.

For more information see the mdEditor [Core Profile Definitions](https://adiwg.github.io/mdProfiles/) page.

See the [List of Alaska Profiles](./ak-profile-list) for the current profile URL's.

# Contents
<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Alaska Region mdEditor profiles](#alaska-region-mdeditor-profiles)
- [Contents](#contents)
- [Custom profile](#custom-profile)
	- [What is a profile definition](#what-is-a-profile-definition)
	- [What is a validation schema](#what-is-a-validation-schema)
- [Creating profile definitions and schemas](#creating-profile-definitions-and-schemas)
- [Adding a custom profile to mdEditor](#adding-a-custom-profile-to-mdeditor)
	- [Add profile definition](#add-profile-definition)
	- [Add profile for use by mdEditor](#add-profile-for-use-by-mdeditor)
	- [Add Validation Schema:](#add-validation-schema)
- [Updating a profile](#updating-a-profile)
- [Curently available Alaska Region profile definitions](#curently-available-alaska-region-profile-definitions)
	- [Alaska Region basic project definition (alpha version)](#alaska-region-basic-project-definition-alpha-version)
	- [Alaska Region basic product definition (alpha version)](#alaska-region-basic-product-definition-alpha-version)
- [References and resources](#references-and-resources)

<!-- /TOC -->

# Custom profile
A mdEditor profile is a template that can be used to limit the metadata fields that are displayed during an edit session and define the fields that are required to be completed within a metadata record. A mdEditor custom profile consists of a "profile definition" and an associated "validation schema". Multiple validation schemas may be associated with a single profile definition. Each unique combination of a definition and schema is a distinct mdEditor profile.

## What is a profile definition
A profile definition is file used to configure the menus and fields that are displayed while editing a mdEditor metadata record.

## What is a validation schema
A validation schema is a file or set of files that specify the metadata fields that must contain data for a record to be considered valid. The validation schema controls when an error message is displayed by the editor.

# Creating profile definitions and schemas
A discussion of creating profiles and schemas is beyond the scope of this documentation. Contact your Data Manager or Data Steward for assistance.

# Adding a custom profile to mdEditor
Before a custom profile can be created for use in the mdEditor, the profile definition and validation schema must be accessible as URLs.
Note: if you are using GitHub to host profile definition files, make sure that you provide users with the url to the "raw" version of the file.

## Add profile definition
  1. Go to Settings/Profiles/Manage Definitions.
  2. Select "Add Definition".
  3. Select "Imported" tab.
  4. Enter URL to profile definition.
  5. Enter an optional alias (the alias replaces the definition title).
  6. Select "Save definition". You should receive a notification that the profile has been downloaded and profile information will be displayed on the tab.

## Add profile for use by mdEditor
  1. Go to Settings/Profiles.
  1. Select "Add Profile".
  1. Enter a "Title" (displayed in profile selection field).
	1. Select a "Profile Definition" from dropdown list (either the definition title or the alias entered in the previous step will be displayed).
	1. And optional description (displayed when cursor hovers over "?" in the profile selection field).
  1. Identify a schema from the "Selected Schema" list and select "Add" (NOTE: Skip this step for testing. You will see a "No schemas have been assigned" warning, just ignore that for now!).
  1. Select "Save Profile".

Notes:
Changes made to a existing profile may not be reflected until the editor is reloaded.

## Add Validation Schema:
  1. Goto Settings/Profiles/Validation.
  1. Select "Add Schema".
  1. Enter URL to the schema root.
  1. Enter a Title and Description.
  1. Select the record "Type" to which the schema applies.
  1. Select "Save Schema". You should receive a notification that the profile has been downloaded.

# Updating a profile
  1. Goto Settings/Profiles/Manage Definitions
  2. Select "Check for Updates"
  3. A blue information icon next to a profile definition indicates that an update is available
  4. Select the definition "Edit" button. (The currently installed version will be displayed along with the updated version in a blue box)
  5. Select "Update Definition" button to proceed with update.
  6. Refresh browser to activate updated profile.

# Currently available Alaska Region profile definitions

## Alaska Region basic project definition (alpha version)
    File name: ak-proj-a.json
    url: https://raw.githubusercontent.com/USFWS/ak-md-profiles/main/ak-proj-a.json

## Alaska Region basic product definition (alpha version)
    File name: ak-prod-a.json
    url: https://raw.githubusercontent.com/USFWS/ak-md-profiles/main/ak-prod-a.json


# References and resources
[mdEditor](https://www.mdeditor.org/)

[mdEdiorGuide](https://guide.mdeditor.org/)

Core Profile Definitions for the mdEditor
  https://adiwg.github.io/mdProfiles/

Core Schema:
    https://raw.githubusercontent.com/adiwg/mdJson-schemas/master/schema/schema.json

ADIwg mdProfiles:
    https://github.com/adiwg/mdProfiles

mdJson-schemas:
    https://github.com/adiwg/mdJson-schemas
