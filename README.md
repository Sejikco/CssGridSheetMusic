# CSS Grid Sheet Music

## Goal

Create a responsive sheet music page using CSS grid layout.

## Examples

Beethoven’s Ode to Joy - [View Example](https://sejikco.github.io/CssGridSheetMusic/beethoven-ode-to-joy.html)

## Overview

Bars are placed in rows of sheet music, up to a maximum of four bars per row depending on the device screen width. Each row of sheet music is preceded by a clef and a key signature, and also a time signature in the first row. Bar lines separate each bar and a bold double bar line concludes a section of bars.

Musical notes are positioned horizontally within a bar such that the distance between notes is relative to the duration. The vertical position reflects the pitch of the musical note.

## Implementation

The responsive sheet music page consists of two CSS grid layouts - one for positioning the bars within the rows of sheet music, and one for positioning musical notes within the bars.

For browsers that do not support CSS grid layouts or grid auto-placement, e.g. Microsoft Edge and Internet Explorer, a float-based layout system is used with fixed-width bars and musical notes with pre-defined widths and margins.

SVGs are used to ensure that musical symbols can be scaled responsively when the zoom level or font size is adjusted. Due to rendering issues in Google Chrome and Microsoft Edge when using SVGs in HTML image elements, HTML division elements with background SVGs and ARIA labels are used instead.

Conditional stylesheets are used for Internet Explorer 9, which does not support CSS transforms, and Internet Explorer 8, which does not support SVGs and CSS background image properties.

