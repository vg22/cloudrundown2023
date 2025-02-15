# Changelog

All notable changes to Congo will be documented in this file. Things that need particular attention when upgrading from a prior version are marked ⚠️.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Support for icons in menus including support for links styled as an icon by itself or an icon with text
- Search link can now be fully customised and positioned anywhere in the menu
- Front matter support for specifying article thumbnails, covers and featured image details (including filename pattern, alt text and caption)
- Support for SVG assets as article thumbnails, covers and featured images
- Front matter keywords support on a per article basis
- Indonesian translation ([#398](https://github.com/jpanther/congo/pull/398))
- Mastodon sharing links ([#405](https://github.com/jpanther/congo/pull/405))
- `homepage.recentLimit` parameter to adjust the maximum number of recent items listed on the homepage ([#411](https://github.com/jpanther/congo/pull/411))

### Changed

- Images smaller than the article width are no longer resized to fill the content area and will now simply align centre ([#394](https://github.com/jpanther/congo/pull/394))
- Upgrade to KaTeX v0.16.4 ([#414](https://github.com/jpanther/congo/pull/414))
- Upgrade to Mermaid v9.3.0 ([#419](https://github.com/jpanther/congo/pull/419))
- Upgrade to Chart.js v4.1.2 ([#420](https://github.com/jpanther/congo/pull/420), [#434](https://github.com/jpanther/congo/pull/434))
- Upgrade to Typography v0.5.9 ([#437](https://github.com/jpanther/congo/pull/437))

### Fixed

- `mainSections` parameter is language dependent and is not referenced from `params.toml` ([#376](https://github.com/jpanther/congo/pull/376))
- Code highlight background cut off in Google Chrome when overflowing content area ([#383](https://github.com/jpanther/congo/pull/383))
- Social icons shift position during CSS transition when hovered in Safari ([#396](https://github.com/jpanther/congo/pull/396))
- Hamburger navigation menu is misaligned in mobile browsers ([#399](https://github.com/jpanther/congo/pull/399))
- Error when attempting to resize SVG assets in page bundles ([#427](https://github.com/jpanther/congo/pull/427))
- Appearance switcher missing `aria-label` ([#438](https://github.com/jpanther/congo/pull/438))
- Article links missing `alt` text and `aria-label` ([#439](https://github.com/jpanther/congo/pull/439))
- Figure shortcode would not apply `class` or `href` attribtues in some cases
- Charts displaying with incorrect theme colours

## [2.4.2] - 2022-11-22

### Added

- Dutch translation ([#371](https://github.com/jpanther/congo/pull/371))
- HTML `theme-color` meta tag to adjust browser colours according to the active Congo colour scheme ([#379](https://github.com/jpanther/congo/pull/379))

### Changed

- Extended head and footer partials are no longer cached during builds
- Upgrade to Chart.js v4.0.1 ([#373](https://github.com/jpanther/congo/pull/373))

### Fixed

- Code highlight background cut off when overflowing content area ([#374](https://github.com/jpanther/congo/issues/374))
- 'Description' HTML meta tag not set from article description ([#378](https://github.com/jpanther/congo/issues/378))

## [2.4.1] - 2022-11-14

### Changed

- Upgrade to Tailwind v3.2.4 ([#368](https://github.com/jpanther/congo/pull/368))

### Fixed

- List page doesn't render nested list pages ([#365](https://github.com/jpanther/congo/issues/365))
- Pagination is duplicated on term pages ([#366](https://github.com/jpanther/congo/issues/366))
- Link to last pagination page sometimes displays twice
- Recent articles would sometimes display less than five articles

## [2.4.0] - 2022-11-10

### Added

- Support for article thumbnails, covers and featured images
- Hybrid header layout that switches between the hamburger and basic menus at appropriate viewport sizes
- Traditional Chinese (Taiwan) translation ([#262](https://github.com/jpanther/congo/pull/262))
- New `list.paginationWidth` parameter to specify how many pagination links are generated before they are truncated
- Site title display can be toggled on or off independently, allowing for it to be displayed alongside the site logo or removed entirely
- Tailwind plugin for Prettier to standardise the order of CSS classes ([#268](https://github.com/jpanther/congo/pull/268))
- External links in article content will now open in a new browser tab ([#312](https://github.com/jpanther/congo/pull/312))
- Independent control over the display of taxonomy listings on article and list pages ([#326](https://github.com/jpanther/congo/pull/326))
- Button shortcode now supports an optional `download` parameter to instruct browsers to directly download resources rather than navigate to a URL ([#349](https://github.com/jpanther/congo/pull/349))
- Minor style and layout improvements

### Changed

- ⚠️ The `logo` parameter has moved under the `header` group and is now set using `header.logo`
- ⚠️ Simplified Chinese (China) language code has changed from `zh` to `zh-cn`
- Site logo is now in its own `logo.html` partial to allow it to be easily overridden ([#322](https://github.com/jpanther/congo/pull/322))
- Upgrade to Chart.js v3.9.1 ([#261](https://github.com/jpanther/congo/pull/261))
- Upgrade to Tailwind v3.2.2 ([#265](https://github.com/jpanther/congo/pull/265), [#333](https://github.com/jpanther/congo/pull/333), [#352](https://github.com/jpanther/congo/pull/352))
- Upgrade to Mermaid v9.2.2 ([#272](https://github.com/jpanther/congo/pull/272), [#279](https://github.com/jpanther/congo/pull/279), [#296](https://github.com/jpanther/congo/pull/296), [#339](https://github.com/jpanther/congo/pull/339), [#360](https://github.com/jpanther/congo/pull/360))
- Upgrade to KaTeX v0.16.3 ([#284](https://github.com/jpanther/congo/pull/284), [#334](https://github.com/jpanther/congo/pull/334))
- Upgrade to Typography v0.5.8 ([#287](https://github.com/jpanther/congo/pull/287), [#292](https://github.com/jpanther/congo/pull/292), [#353](https://github.com/jpanther/congo/pull/353))

### Fixed

- Appearance switcher title doesn't update when switching appearance ([#235](https://github.com/jpanther/congo/issues/235))
- Article updated date logic doesn't consider formatted date values ([#259](https://github.com/jpanther/congo/issues/259))
- Error calling Paginate when attempting to generate a site with no taxonomies ([#289](https://github.com/jpanther/congo/issues/289))
- Multilingual links are spaced incorrectly when using Hugo minify ([#298](https://github.com/jpanther/congo/issues/298))
- Pagination links overflow the page area on large datasets ([#299](https://github.com/jpanther/congo/issues/299))
- Embedded content disappears when displayed at certain viewport sizes ([#302](https://github.com/jpanther/congo/issues/302), [#335](https://github.com/jpanther/congo/issues/335))
- Order of articles on list pages would not follow Hugo conventions when grouped by year ([#313](https://github.com/jpanther/congo/issues/313))
- Button shortcode overlaps table of contents when at the top of the article content ([#337](https://github.com/jpanther/congo/issues/337))
- Providing a `colorScheme` value containing uppercase characters breaks some deployments ([#347](https://github.com/jpanther/congo/issues/347))

## [2.3.1] - 2022-07-30

### Added

- Japanese translation ([#234](https://github.com/jpanther/congo/pull/234))

### Changed

- Upgrade to Mermaid v9.1.3 ([#233](https://github.com/jpanther/congo/pull/233))
- Upgrade to Tailwind v3.1.6 ([#245](https://github.com/jpanther/congo/pull/245))
- Upgrade to Typography v0.5.4 ([#246](https://github.com/jpanther/congo/pull/246))
- Upgrade to Chart.js v3.8.2 ([#247](https://github.com/jpanther/congo/pull/247))

### Fixed

- Main content misaligned when hamburger menu is opened at large viewport sizes

## [2.3.0] - 2022-06-27

### Added

- Header layouts for selecting a preferred header style
- Hamburger menu header layout with popover main menu ([#167](https://github.com/jpanther/congo/discussions/167), [#88](https://github.com/jpanther/congo/discussions/88), [#43](https://github.com/jpanther/congo/discussions/43), [#29](https://github.com/jpanther/congo/discussions/29))
- Front matter support for showing or hiding comments on a per article basis ([#207](https://github.com/jpanther/congo/discussions/207))
- `showCopyright` and `showThemeAttribution` parameters that allow more control over how the site footer is displayed ([#192](https://github.com/jpanther/congo/discussions/192))
- `bars` SVG icon

### Changed

- ⚠️ Footer configuration parameters are now in their own `footer` sub-group
- Search will now return results for all page types, including lists and taxonomies
- Comments partials are now better considered within the page layout
- Reduced whitespace at the top of the main content block ([#226](https://github.com/jpanther/congo/discussions/226))
- Upgrade to Tailwind v3.1.4 ([#225](https://github.com/jpanther/congo/pull/225))

### Fixed

- Hugo v0.101.0 breaks the link to the homepage ([#230](https://github.com/jpanther/congo/issues/230))
- Search link does not appear in header if main menu has no items to display
- Search only returns results in the primary language when multiple languages are available ([#229](https://github.com/jpanther/congo/issues/229))
- Arrow on external article links not aligned correctly when title wraps onto multiple lines
- Arrow on external article links points the wrong direction for RTL languages
- Scroll to top misaligned with the footer at small viewport heights
- Link to homepage would be incorrect in some deployments if `baseURL` contained sub-directories in the path

## [2.2.3] - 2022-06-22

### Changed

- Profile image alt text now uses author name when available

### Fixed

- Search not working when `baseURL` does not end with a forward slash ([#224](https://github.com/jpanther/congo/pull/224))
- Author `headline` parameter not correctly displaying Markdown or Emoji content

## [2.2.2] - 2022-06-16

### Added

- Breadcrumb display can now be can now be specificed in front matter for articles and list pages
- Italian translation ([#209](https://github.com/jpanther/congo/pull/209))

### Changed

- Upgrade to Chart.js v3.8.0 ([#204](https://github.com/jpanther/congo/pull/204))
- Upgrade to KaTeX v0.16.0 ([#208](https://github.com/jpanther/congo/pull/208))
- Upgrade to Mermaid v9.1.2 ([#214](https://github.com/jpanther/congo/pull/214))

## [2.2.1] - 2022-05-25

### Changed

- Upgrade to Mermaid v9.1.1 ([#194](https://github.com/jpanther/congo/pull/194))
- Upgrade to Fuse.js v6.6.2 ([#195](https://github.com/jpanther/congo/pull/195))
- Upgrade KaTeX to v0.15.6 ([#202](https://github.com/jpanther/congo/pull/202))

### Fixed

- Main content area doesn't grow to window height ([#201](https://github.com/jpanther/congo/issues/201))

## [2.2.0] - 2022-05-09

### Added

- Finnish translation ([#185](https://github.com/jpanther/congo/pull/185))

### Changed

- Updated French translation ([#178](https://github.com/jpanther/congo/pull/178))
- Analytics partial now checks `hugo.IsProduction` instead of `.Site.IsServer` before including scripts ([#179](https://github.com/jpanther/congo/issues/179))
- Upgrade to Tailwind v3.0.24 ([#176](https://github.com/jpanther/congo/pull/176))
- Upgrade to Mermaid v9.0.1 ([#183](https://github.com/jpanther/congo/pull/183))
- Upgrade to Fuse.js v6.6.1 ([#189](https://github.com/jpanther/congo/pull/189))

### Fixed

- Code blocks are rendered incorrectly in RTL languages ([#164](https://github.com/jpanther/congo/issues/164))
- Scroll to top link overlaps footer menu on mobile devices when there are several links ([#172](https://github.com/jpanther/congo/issues/172))

### Removed

- `hugo.Generator` from HTML `<head>` so that the [default Hugo generator behaviour](https://gohugo.io/getting-started/configuration/#disablehugogeneratorinject) works as expected ([#179](https://github.com/jpanther/congo/issues/179))

## [2.1.3] - 2022-04-12

### Added

- Hungarian translation ([#170](https://github.com/jpanther/congo/pull/170))

### Fixed

- Scroll to top link overlaps footer menu on mobile devices ([#172](https://github.com/jpanther/congo/issues/172))

## [2.1.2] - 2022-04-08

### Added

- Romanian translation ([#168](https://github.com/jpanther/congo/pull/168))

### Changed

- Upgrade to Mermaid v9.0.0

## [2.1.1] - 2022-04-03

### Added

- Print styles to hide unnecessary elements when printing ([#155](https://github.com/jpanther/congo/pull/155))
- Hebrew translation ([#163](https://github.com/jpanther/congo/pull/163))

### Fixed

- Footer menu displays incorrectly in RTL languages ([#165](https://github.com/jpanther/congo/pull/165))

## [2.1.0] - 2022-03-14

### Added

- Simple page layout for creating full-width content ([#139](https://github.com/jpanther/congo/issues/139))
- Portuguese (Portugal) translation ([#144](https://github.com/jpanther/congo/pull/144))

### Changed

- Upgrade SVG icons to FontAwesome 6:
  - New icons for Hashnode, bug, check, comment, light bulb, list, pencil, skull, tag, and information. ([#136](https://github.com/jpanther/congo/discussions/136))
  - ⚠️ The `exclamation-triangle` icon has been renamed `triangle-exclamation`
  - ⚠️ The `times` icon has been renamed `xmark`
  - ⚠️ The `stackoverflow` icon has been renamed `stack-overflow`
- Upgrade KaTeX to v0.15.3
- Markdown images and `figure` shortcode now search the `assets/` directory if an image cannot be found in page bundle ([#126](https://github.com/jpanther/congo/issues/126))
- Markdown images and `figure` shortcode now fallback to static assets if an image is not provided as a Hugo resource ([#126](https://github.com/jpanther/congo/issues/126))
- Taxonomy term listings now honour the `groupByYear` parameter ([#145](https://github.com/jpanther/congo/pull/145))
- The `alert` shortcode now allows its icon to be specified as a parameter

### Fixed

- Dark appearance shown even when default appearance set to light and auto switching is disabled ([#149](https://github.com/jpanther/congo/issues/149))

## [2.0.5] - 2022-02-20

### Added

- Bengali translation ([#115](https://github.com/jpanther/congo/pull/115))

### Changed

- Upgrade to Tailwind v3.0.23 and Typography v0.5.2
- Upgrade to Mermaid v8.14.0
- Upgrade to Chart.js v3.7.1

### Fixed

- Updated date is displayed even when it is the same as published date
- Structured data on homepage unparsable by Google ([#113](https://github.com/jpanther/congo/issues/113))
- Underline styles not displaying correctly in some browsers ([#125](https://github.com/jpanther/congo/issues/125))

## [2.0.4] - 2022-02-09

### Changed

- Updated German translation ([#110](https://github.com/jpanther/congo/pull/110))
- Upgrade to Tailwind v3.0.19

### Fixed

- Main content area not growing to fill screen vertically
- Search results not cleared when search is dismissed ([#109](https://github.com/jpanther/congo/pull/109))
- Emoji strings not displaying in search results

## [2.0.3] - 2022-02-07

### Changed

- Updated Turkish translation ([#105](https://github.com/jpanther/congo/pull/105))
- Updated Spanish translation ([#106](https://github.com/jpanther/congo/pull/106))

### Fixed

- Markdown images and `figure` shortcode fail to load resource when providing an external URL source
- HTML `figcaption` tags are output for Markdown images even when a caption is not provided
- Light appearance briefly appears on page load before switching to dark appearance ([#102](https://github.com/jpanther/congo/issues/102))

## [2.0.2] - 2022-02-05

### Changed

- Updated French translation ([#100](https://github.com/jpanther/congo/pull/100))

### Fixed

- User's appearance preference is lost on page load when default appearance is dark ([#102](https://github.com/jpanther/congo/issues/102))
- JavaScript warning when appearance switcher is disabled

## [2.0.1] - 2022-02-03

### Fixed

- Hugo module error when downloading version 2
- Emoji strings not displaying in table of contents

## [2.0.0] - 2022-02-03

### Added

- Multilingual support
- Right-to-left (RTL) language support
- Site search powered by Fuse.js
- Automatic Markdown image resizing and srcset generation
- Performance and Accessibility improvements to achieve perfect Lighthouse scores
- Tables of contents on article pages ([#47](https://github.com/jpanther/congo/discussions/47))
- Code copy buttons in article content
- Taxonomy and term listings now support Markdown content
- Taxonomies on article and list pages
- Article pagination direction can be inverted
- Author `headline` parameter
- Skip to content and Scroll to top links
- Archetype for generating links to external articles

### Changed

- ⚠️ Required Hugo version is now 0.87.0 or later
- ⚠️ Complete rewrite of dark mode to allow more flexibile configuration
- ⚠️ All theme images are now Hugo assets
- ⚠️ Overhauled `figure` shortcode which now resizes images
- Upgrade to Tailwind v3.0.18
- Inline JavaScript moved to external files
- Improved JSON-LD structured data
- Breadcrumbs now fallback to section name when `title` is not provided
- Minor style and layout improvements

## [1.6.4] - 2022-01-24

### Added

- Turkish translation ([#90](https://github.com/jpanther/congo/pull/90))

### Changed

- Article updated date formatting and i18n ([#91](https://github.com/jpanther/congo/pull/91))
- Upgrade to Mermaid v8.13.10

### Fixed

- Article metadata not wrapping at small viewports ([#91](https://github.com/jpanther/congo/pull/91))

## [1.6.3] - 2022-01-19

### Added

- Icon for Stack Overflow ([#82](https://github.com/jpanther/congo/pull/82))

### Changed

- Upgrade to Mermaid v8.13.9
- Upgrade to KaTeX v0.15.2

### Fixed

- Emoji characters in article titles not appearing on list pages and in HTML metadata ([#84](https://github.com/jpanther/congo/pull/84))

## [1.6.2] - 2022-01-07

### Changed

- Upgrade to Chart.js v3.7.0
- Upgrade to Mermaid v8.13.8

### Fixed

- `lead` shortcode not rendering Markdown formatted text ([#73](https://github.com/jpanther/congo/issues/73))
- JSON-LD keywords data not structured correctly ([#74](https://github.com/jpanther/congo/issues/74))

## [1.6.1] - 2021-12-31

### Added

- Icon for Blogger ([#71](https://github.com/jpanther/congo/pull/71))

### Fixed

- Error when building using older Hugo versions ([#65](https://github.com/jpanther/congo/pull/65))
- Error when serving sites using blogdown ([#66](https://github.com/jpanther/congo/pull/66))

## [1.6.0] - 2021-12-21

### Added

- Article word counts ([#57](https://github.com/jpanther/congo/pull/57))
- Last updated dates on articles
- Icons for Amazon, Apple, Flickr, Google, Kickstarter, Microsoft, Patreon, Telegram, Tumblr and WhatsApp

### Changed

- Adjusted contrast of some items to improve accessibility
- Upgrade to Chart.js v3.6.2
- Upgrade to Mermaid v8.13.6

### Fixed

- Missing ARIA descriptions and alt tags on some images and links

## [1.5.3] - 2021-11-18

### Changed

- Updated Chinese translation ([#32](https://github.com/jpanther/congo/pull/32))

### Fixed

- Article pagination uses date of current article ([#32](https://github.com/jpanther/congo/pull/32))

## [1.5.2] - 2021-11-10

### Added

- German translation ([#27](https://github.com/jpanther/congo/pull/27))
- Portuguese (Brazil) translation ([#28](https://github.com/jpanther/congo/pull/28))
- Spanish translation ([#30](https://github.com/jpanther/congo/pull/30))

### Fixed

- Article pagination link spacing ([#26](https://github.com/jpanther/congo/pull/26))
- Minor icon style issues

## [1.5.1] - 2021-11-04

### Fixed

- Hugo failing to build site when deploying as a module

## [1.5.0] - 2021-11-04

### Added

- Chart.js support using `chart` shortcode
- KaTeX support using `katex` shortcode
- Dark mode toggle with new theme parameters for managing light/dark appearance
- French translation ([#18](https://github.com/jpanther/congo/pull/18))
- Author bio in article footer
- Grouping by year can now be specificed in front matter on list pages

### Changed

- Site name, author and menus will now render Markdown and Emoji
- Bundled Mermaid for better vendor dependency management
- Mermaid diagrams are now themed to match the configured colour scheme
- Upgrade to Tailwind v2.2.19

### Fixed

- Site logo image dimensions are unconstrained ([#19](https://github.com/jpanther/congo/issues/19))
- Article summary styled incorrectly in dark mode
- Links containing `code` blocks styled incorrectly

## [1.4.0] - 2021-10-20

### Added

- Footer menu
- Article summary support
- Slate colour scheme ([#9](https://github.com/jpanther/congo/pull/9))
- Icons for ORCID and ResearchGate ([#9](https://github.com/jpanther/congo/pull/9))
- Pinterest sharing links
- Sharing links can now be specified in front matter

### Changed

- Main menu is now optional
- Upgrade to Mermaid v8.13.3
- Upgrade to Tailwind v2.2.17

### Fixed

- Site logo not linked to home page ([#13](https://github.com/jpanther/congo/issues/13))

## [1.3.0] - 2021-09-29

### Added

- Site logo support
- Chinese translation ([#2](https://github.com/jpanther/congo/pull/2))

### Changed

- Upgrade to Tailwind v2.2.16

## [1.2.1] - 2021-08-26

### Added

- New `robots` parameter to add metadata to guide robots on how to handle specific content

### Changed

- URLs are relative by default which allows the theme to be more flexible in different deployment scenarios

### Fixed

- Missing dark style for group subheadings on article listings
- Fathom Analytics script included twice when using custom domain
- Recent heading on homepage profile layout misaligned

## [1.2.0] - 2021-08-22

### Added

- Multiple colour schemes
- Edit links on article pages
- Icons for Foursquare and Pinterest
- Asset fingerprinting and SRI
- CSS minification for custom stylesheets

### Changed

- Static assets are now managed through Hugo Pipelines

### Fixed

- Minor style issue with `button` shortcode
- Hugo Modules would fail when using default theme config file
- Some content not centred correctly on the profile homepage layout
- Some links missing the correct styles when in Firefox
- `externalUrl` front matter not working on some list pages

## [1.1.1] - 2021-08-19

### Fixed

- Hotfix for exampleSite and GitHub configuration

## [1.1.0] - 2021-08-18

### Added

- Breadcrumbs
- i18n support
- Recent articles partial
- CSS transitions
- Hugo module support
- JSON-LD structured metadata

### Changed

- ⚠️ Renamed parameter: `homepage.showList` -> `homepage.showRecent`
- ⚠️ Renamed parameter: `homepage.listSections` -> `mainSections`
- ⚠️ Consolidated author configuration parameters into `config.toml`
- General style tweaks to enhance design consistency

### Fixed

- URLs being incorrect in some cases when the site is deployed in a subfolder

## [1.0.0] - 2021-08-16

### Added

- Built with Tailwind CSS JIT for minified stylesheets without any excess code
- Fully responsive layout
- Dark mode (auto-switching based upon browser)
- Highly customisable configuration
- Multiple homepage layouts
- Flexible with any content types, taxonomies and menus
- Ability to link to posts on third-party websites
- Diagrams and visualisations using Mermaid JS
- SVG icons from FontAwesome 5
- Heading anchors, Buttons, Badges and more
- HTML and Emoji support in articles
- SEO friendly with links for sharing to social media
- RSS feeds
- Fathom Analytics and Google Analytics support
- Favicons support
- Comments support
- Advanced customisation using simple Tailwind colour definitions and styles
- Fully documented

[unreleased]: https://github.com/jpanther/congo/compare/v2.4.2...HEAD
[2.4.2]: https://github.com/jpanther/congo/compare/v2.4.1...v2.4.2
[2.4.1]: https://github.com/jpanther/congo/compare/v2.4.0...v2.4.1
[2.4.0]: https://github.com/jpanther/congo/compare/v2.3.1...v2.4.0
[2.3.1]: https://github.com/jpanther/congo/compare/v2.3.0...v2.3.1
[2.3.0]: https://github.com/jpanther/congo/compare/v2.2.3...v2.3.0
[2.2.3]: https://github.com/jpanther/congo/compare/v2.2.2...v2.2.3
[2.2.2]: https://github.com/jpanther/congo/compare/v2.2.1...v2.2.2
[2.2.1]: https://github.com/jpanther/congo/compare/v2.2.0...v2.2.1
[2.2.0]: https://github.com/jpanther/congo/compare/v2.1.3...v2.2.0
[2.1.3]: https://github.com/jpanther/congo/compare/v2.1.2...v2.1.3
[2.1.2]: https://github.com/jpanther/congo/compare/v2.1.1...v2.1.2
[2.1.1]: https://github.com/jpanther/congo/compare/v2.1.0...v2.1.1
[2.1.0]: https://github.com/jpanther/congo/compare/v2.0.5...v2.1.0
[2.0.5]: https://github.com/jpanther/congo/compare/v2.0.4...v2.0.5
[2.0.4]: https://github.com/jpanther/congo/compare/v2.0.3...v2.0.4
[2.0.3]: https://github.com/jpanther/congo/compare/v2.0.2...v2.0.3
[2.0.2]: https://github.com/jpanther/congo/compare/v2.0.1...v2.0.2
[2.0.1]: https://github.com/jpanther/congo/compare/v2.0.0...v2.0.1
[2.0.0]: https://github.com/jpanther/congo/compare/v1.6.4...v2.0.0
[1.6.4]: https://github.com/jpanther/congo/compare/v1.6.3...v1.6.4
[1.6.3]: https://github.com/jpanther/congo/compare/v1.6.2...v1.6.3
[1.6.2]: https://github.com/jpanther/congo/compare/v1.6.1...v1.6.2
[1.6.1]: https://github.com/jpanther/congo/compare/v1.6.0...v1.6.1
[1.6.0]: https://github.com/jpanther/congo/compare/v1.5.3...v1.6.0
[1.5.3]: https://github.com/jpanther/congo/compare/v1.5.2...v1.5.3
[1.5.2]: https://github.com/jpanther/Congo/compare/v1.5.1...v1.5.2
[1.5.1]: https://github.com/jpanther/Congo/compare/v1.5.0...v1.5.1
[1.5.0]: https://github.com/jpanther/Congo/compare/v1.4.0...v1.5.0
[1.4.0]: https://github.com/jpanther/Congo/compare/v1.3.0...v1.4.0
[1.3.0]: https://github.com/jpanther/Congo/compare/v1.2.1...v1.3.0
[1.2.1]: https://github.com/jpanther/Congo/compare/v1.2.0...v1.2.1
[1.2.0]: https://github.com/jpanther/Congo/compare/v1.1.1...v1.2.0
[1.1.1]: https://github.com/jpanther/congo/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/jpanther/congo/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/jpanther/congo/releases/tag/v1.0.0
