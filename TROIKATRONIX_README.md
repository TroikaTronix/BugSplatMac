# BugSplatMac

This is the TroikaTronix version of BugSplat Mac, which is by now some versions behind the master.

The main reason this needed to be modified was to customize the dialog presented to the user. The customized dialog includes the GDPR statement and otherwise makes the crash-reporting experience more friendly.

Most of the user-facing changes are in the XIB file, with a few supporting code and resource changes.

## Notable TroikaTronix Changes

- Customized the crash-report dialog text for Isadora.
- Added GDPR/privacy disclosure text explaining that submitted crash report data and the user's IP address are forwarded to BugSplat.com.
- Changed the cancel button text from `Cancel` to `Don't Send`.
- Changed the name and email fields to make clear that both are optional.
- Reworded the comments prompt to be friendlier and more specific to the crash.
- Added a `commentAndContactEnclView` container view and supporting frame-adjustment code so the comments/contact area resizes correctly when the comments disclosure is shown or hidden.
- Slightly adjusted the details area height.
- Reworked the XIB layout to make the crash-report dialog taller and to better organize the introduction, comments, optional contact information, GDPR text, details, and action buttons.
- Changed the BugSplat logo asset from a preserved-vector SVG to 1x and 2x PNG image resources.
- Lowered the macOS deployment target from 10.13 to 10.12.
- Adjusted Xcode code-signing settings.
- Deleted user-specific Xcode workspace, scheme, breakpoint, and interface-state files.
- Updated `.gitignore` to exclude Xcode `xcuserdata` and `xcuserdatad` files going forward.

## Notes

This fork exists only to support TroikaTronix's customized BugSplat crash-reporting dialog. The repository should be considered a vendor fork rather than the upstream source of truth.
