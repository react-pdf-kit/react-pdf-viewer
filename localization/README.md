# Localization

React PDF Kit supports multiple languages through JSON locale files. This folder contains translation files that customize all user-facing text in the PDF viewer. For the full list of localization keys exposed by the `Localization` interface, see the [React PDF Kit interfaces documentation](https://docs.react-pdf-kit.dev/interfaces#localization).

## Available Locales

| File | Language |
| --- | --- |
| `en_US.json` | English (United States) |
| `de_DE.json` | German (Germany) |
| `it_IT.json` | Italian (Italy) |
| `pt_PT.json` | Portuguese (Portugal) |
| `th_TH.json` | Thai (Thailand) |
| `zh_CN.json` | Chinese (Simplified) |

## Adding a New Locale

1. Copy `en_US.json` and rename it using the format `{language}_{COUNTRY}.json` (e.g., `ja_JP.json` for Japanese, `fr_FR.json` for French).
2. Translate all 79 values in the file. **Do not rename any keys** -- only change the values.
3. Pass your locale file to the `localization` prop on `RPConfig`:

```jsx
import jaJP from './localization/ja_JP.json'

<RPConfig localization={jaJP}>
  {/* ... */}
</RPConfig>
```

## Translation Keys Reference

Each locale file is a flat JSON object. Below is a breakdown of every key grouped by feature area.

### Search

| Key | Description |
| --- | --- |
| `searchButtonTooltip` | Tooltip for the search button |
| `searchInputPlaceholder` | Placeholder text inside the search input |
| `searchInputTooltip` | Tooltip for the search input |
| `searchPrevTooltip` | Tooltip for the "previous match" button |
| `searchNextTooltip` | Tooltip for the "next match" button |
| `searchCloseButtonTooltip` | Tooltip for the close search button |
| `searchMatchCaseLabel` | Label for the "Match Case" toggle |
| `searchMatchCaseTooltip` | Tooltip for the "Match Case" toggle |
| `searchWholeWordsLabel` | Label for the "Whole Words" toggle |
| `searchWholeWordsTooltip` | Tooltip for the "Whole Words" toggle |

### Navigation

| Key | Description |
| --- | --- |
| `previousPageTooltip` | Tooltip for going to the previous page |
| `currentPageTooltip` | Tooltip for the current page indicator |
| `nextPageTooltip` | Tooltip for going to the next page |
| `firstPageLabel` | Label for the "First page" action |
| `firstPageTooltip` | Tooltip for the "First page" action |
| `lastPageLabel` | Label for the "Last page" action |
| `lastPageTooltip` | Tooltip for the "Last page" action |

### Zoom

| Key | Description |
| --- | --- |
| `zoomOutTooltip` | Tooltip for the zoom out button |
| `zoomInTooltip` | Tooltip for the zoom in button |
| `zoomSelectTooltip` | Tooltip for the zoom level dropdown |
| `zoomActualSize` | Label for the "Actual size" zoom option |
| `zoomPageFit` | Label for the "Page fit" zoom option |
| `zoomPageWidth` | Label for the "Page width" zoom option |

### Theme

| Key | Description |
| --- | --- |
| `themeEnableDarkTooltip` | Tooltip for enabling dark theme |
| `themeEnableLightTooltip` | Tooltip for enabling light theme |

### File Operations

| Key | Description |
| --- | --- |
| `openLocalFileLabel` | Label for the "Open local file" action |
| `openLocalFileTooltip` | Tooltip for the "Open local file" action |
| `downloadFileLabel` | Label for the "Download file" action |
| `downloadFileTooltip` | Tooltip for the "Download file" action |
| `printLabel` | Label for the print action |
| `printTooltip` | Tooltip for the print action |
| `printLoadingMessage` | Message shown while preparing the document for print |
| `printCancelLabel` | Label for the cancel button during print preparation |

### View Controls

| Key | Description |
| --- | --- |
| `fullScreenLabel` | Label for the full screen action |
| `fullScreenTooltip` | Tooltip for the full screen action |
| `moreOptionTooltip` | Tooltip for the "More options" menu |
| `rotateClockwiseLabel` | Label for the rotate clockwise action |
| `rotateClockwiseTooltip` | Tooltip for the rotate clockwise action |
| `rotateCounterclockwiseLabel` | Label for the rotate counterclockwise action |
| `rotateCounterclockwiseTooltip` | Tooltip for the rotate counterclockwise action |
| `textSelectionLabel` | Label for the text selection tool |
| `textSelectionTooltip` | Tooltip for the text selection tool |
| `handToolLabel` | Label for the hand tool |
| `handToolTooltip` | Tooltip for the hand tool |
| `documentPropertiesLabel` | Label for the document properties action |
| `documentPropertiesTooltip` | Tooltip for the document properties action |

### Scroll Modes

| Key | Description |
| --- | --- |
| `pageScrollingLabel` | Label for page scrolling mode |
| `pageScrollingTooltip` | Tooltip for page scrolling mode |
| `verticalScrollingLabel` | Label for vertical scrolling mode |
| `verticalScrollingTooltip` | Tooltip for vertical scrolling mode |
| `horizontalLabel` | Label for horizontal scrolling mode |
| `horizontalTooltip` | Tooltip for horizontal scrolling mode |
| `wrappedScrollingLabel` | Label for wrapped scrolling mode |
| `wrappedScrollingTooltip` | Tooltip for wrapped scrolling mode |

### Page View Modes

| Key | Description |
| --- | --- |
| `singlePageLabel` | Label for single page view |
| `singlePageTooltip` | Tooltip for single page view |
| `dualPageLabel` | Label for dual page view |
| `dualPageTooltip` | Tooltip for dual page view |
| `dualPageWithCoverLabel` | Label for dual page view with a cover page |
| `dualPageWithCoverTooltip` | Tooltip for dual page view with a cover page |

### Document Properties

| Key | Description |
| --- | --- |
| `propertiesFilenameLabel` | Label for the file name property |
| `propertiesFileSizeLabel` | Label for the file size property |
| `propertiesTitleLabel` | Label for the title property |
| `propertiesAuthorLabel` | Label for the author property |
| `propertiesSubjectLabel` | Label for the subject property |
| `propertiesKeywordLabel` | Label for the keywords property |
| `propertiesCreatorLabel` | Label for the creator property |
| `propertiesCreateOnLabel` | Label for the creation date property |
| `propertiesModifiedOnLabel` | Label for the modified date property |
| `propertiesPDFProducerLabel` | Label for the PDF producer property |
| `propertiesPDFVersionLabel` | Label for the PDF version property |
| `propertiesPageCountLabel` | Label for the page count property |

### Thumbnails

| Key | Description |
| --- | --- |
| `thumbnailTooltip` | Tooltip for the thumbnail panel |

### Password Protected Documents

| Key | Description |
| --- | --- |
| `passwordModalTitle` | Title of the password prompt modal |
| `passwordModalMessage` | Message displayed in the password prompt |
| `passwordPlaceholder` | Placeholder text in the password input |
| `passwordConfirmLabel` | Label for the submit button |
| `passwordError` | Error message shown for incorrect password |

### Drag and Drop

| Key | Description |
| --- | --- |
| `dragDropFileMessage` | Message shown in the drag-and-drop zone |

## Contributing a New Locale

Created a locale file for a language we don't support yet? We'd love to include it! Please open a pull request with your new `{language}_{COUNTRY}.json` file added to this folder. Make sure all 79 keys are translated and the file is valid JSON before submitting.

## Tips

- Use `en_US.json` as the reference -- it always contains the complete set of keys.
- Every key must be present in your locale file. Missing keys will fall back to the default English text.
- Key names follow the pattern `{feature}{Element}{Type}` (e.g., `searchInputPlaceholder`, `zoomOutTooltip`).
