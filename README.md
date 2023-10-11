# Color from Asset in Package crashes Preview in Package


## Scenario

A Swift Package (Package A) has a dependency to Package B.
Package B contains a Color Asset and exposes it to Package A.
Package A contains a Preview using the Color Asset from Package B.


## Issue

The Preview in Package A crashes.

Using the Color Asset in a project instead of a package does not crash the preview.


## Example Code

A Package with an Asset is available at: https://github.com/simonnickel/FB-PackageWithColorAsset.git

The example is a Package using FB-PackageWithColorAsset and a Preview using the color from the package.

Opening the preview crashes.


## Crash   

== PREVIEW UPDATE ERROR:

	CrashReportError: Fatal Error in resource_bundle_accessor.swift
	
	XCPreviewAgent crashed due to fatalError in resource_bundle_accessor.swift at line 44.
	
	unable to find bundle named FBPackageWithColorAsset_FBPackageWithColorAsset
	
Full crashlog can be found in Report.txt


## Workaround

There seems to be some kind of workaround: https://developer.apple.com/forums/thread/664295


## Tested on

 - Xcode Version 15.0 (15A240d)
