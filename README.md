# editor

a rich text editor for javascript

## todo

- [x] bug! (create bold, make substring italic, remove bold on substring)
- [x] splitNodeAtChild
- [x] styleToElement
- [x] elementHasStyle
- [x] removeStyleFromElement
- [x] solve bug with empty style elems
- [x] handle BR as content tag
- [x] issue with strikethrough and underline together not working on spans
- [x] clicking to create a new style elem
- [x] empty style elem
- [x] bug with styling completely empty editor/element
- [x] when making newline, retain styling options
- [x] when clicking to create style elem, it doesn't update style (not sure if this is just mobile)
- [x] when clicking to create style elem, properly handle back arrow
- [x] handle br node in style change
- [x] font support (handle font tag)
- [x] clicking to create font tag creates error
- [x] reload in cursor doesn't reload page
- [x] bug with removing/changing styling with styling already applied 
- [x] sanitization (handle spans, invalid elements, and nested styling)
- [x] bug with changeStyle and font tag
- [x] div, brs, ps and lists in pastes
- [x] pasting multiline content into lists
- [x] when pasting list into list, it sometimes places list at the end of the lists
- [x] spaces between pasted nodes
- [x] pasting with empty editor
- [x] update illegal tags (ignore the tags instead of removing them)
- [x] sanitize out stuff like `pre`, `code`, `h1`, etc.
- [x] urgent bug with styling line break (handle BR)
- [x] urgent bug with backspace with cursor
- [x] create new cursor when backspacing out of style node
- [x] issue with whitespace, pasting/dragging
- [x] paste is broken again (pasting span into blockquote)
- [x] bug with styling `br`
- [x] bugs (extraneous divs when removing block styles)
- [x] bug with pasting styled within span
- [x] fix whitespace (handle `pre`)
- [x] history (restore selection and currentCursor)
- [x] history length limit
- [x] drag and drop
- [x] fix metaKey support on webkit
- [x] bug with styling br element
- [x] handle whitespace css
- [x] join multiple blocks (maybe)
- [x] removeBlockStyle is deleting content?!!?! (i might be going bobo) (i was not in fact bobo)
- [x] handle selection
- [x] handle empty editor
- [x] fix pasting (only combine lists on first)
- [x] urgent bug: removing styling on block node containing multiple children
- [x] urgent bug: for some reason not joining certain block nodes (may have to re-write joining code)
- [x] fix pasting (google docs does some weird stuff with B blocks and font-weight: normal ????)
- [x] styling overrides (respect order of dom)
- [x] order of operations
- [x] fix order of block nodes
- [x] fix drag and drop
- [x] joining nodes not working with paste anymore
- [x] remove old child pasted into if it is empty
- [x] fix backspace on cursor
- [x] urgent: styling block empty editor
- [x] urgent: infinite loop with removing styling on block
- [x] applying style should escape out of SOME extraneous nodes
- [x] splitting out of parent nodes when removing block style doesn't work
- [x] paste block nodes (allow certain nodes through, re-apply certain block styles (h1, text align))
- [x] problem with block nodes inside inline nodes
- [x] remove extraneous block nodes
- [x] bug with left click removing stuff
- [x] when pasting, if possible, always join the first node (and the split node, if possible)
- [x] h1-h6
- [x] when pasting, apply inline styles to all content tags, not just text nodes
- [x] remove current selection when pasting
- [x] handle lists (joining lists doesn't work)
- [x] when pasting, place the paste content AFTER the start node, not before!!
- [x] removing nested styles doesn't work (blockquote in blockquote)
- [x] redo list styling options
- [x] issue with getBlockNodesInRange: it doesn't stop before the last one
- [x] test more complex list topology
- [x] certain styles should activate if any node inside has that style
- [x] removing block style should join divs (not sure how this issue arose, but its worth looking into) (see `<blockquote>asdasd<strong>asdasd</strong><div>asdasd</div></blockquote>`)
- [x] paste, drag should have takeSnapshotOnNextChange
- [x] saveHistory happens multiple times on block removal
- [x] list joining broken
- [x] removing styles on nested nodes not working
- [x] does removing multiple at a time work?
- [x] bug with pasting nodes (seperating it for some reason)
- [x] cursor not working within a href
- [x] pasting text align isn't working!
- [x] urgent bug: removing second bq on `<blockquote>asdasdasd</blockquote><blockquote><br></blockquote>` doesn't work
- [x] improper style value when removing style on cursor
- [x] issue when block styling BR (`abc<div><br></div>`)
- [x] join adjacent list nodes when applying style
- [x] getTextNodesInRange doesn't stop before the last one
- [x] more styling options
- [x] todo: if nothing selected, go to the beginning of the editor
- [x] urgent bug: issue with getTextNodesInRange extending beyond selection (possible issue with range)
- [x] blockIndent is indenting outside of editor
- [x] todo: bug with this situation: `<ol><li><ol><li><ol><li>asdasd</li></ol></li></ol></li><li><ol><li><div>asd</div></li></ol></li><li><div>as</div></li><li><ol><li><div>a</div></li></ol></li></ol>` (not joining. consider joining every time we have a group of consecutive siblings. offload the joining of consecutive siblings to a separate function and join every time in there)
- [x] sometimes when pressing ctrl-z it produces the letter a ?
- [x] indenting does not select
- [x] retain selection when leaving editor
- [x] paste simple indenting
- [x] paste links? does it work
- [ ] block styling options
- [x] sanitize url for links
- [x] ctrl-click on links
- [x] fix dragging in color picker on mobile
- [x] LI nodes that contain another list should not display marker (perform this change action on block style)
- [x] make modals always show up on screen
- [x] lists
- [x] webkit dragging doesn't work (color picker)
- [x] bug with pasting from google docs (certain color values are throwing it off (background: transparent))
- [x] really slow with large documents (detectStyling, etc.)
- [x] slow with ctrl-a for some reason?
- [x] bug with pasting (not removing newlines between nodes)
- [x] optimize onChangeSelect (possibly) (for mobile users)
- [x] modals on iPad not showing up properly on screen
- [ ] images
- [ ] image copy and paste (copy width/height/data value) (paste data value -> object url, paste width/height)
- [ ] image selection
- [ ] horizontal rule
- [x] when pasting stuff with newlines, replace with spaces!
- [x] link command cannot create cursor (it needs text to be selected)
- [x] new document function
- [x] format indent up
- [x] format indent down
- [ ] disallow pasting HTML option 
- [ ] overhaul UI
- [ ] copy paste buttons
- [ ] accessibility (for, name, aria, etc.) and esc button handling for modals
- [ ] remove all styling from text, remove all color from 
- [ ] change list style (possibly)
- [ ] find and replace
- [ ] more history (calculate)
- [ ] menubar should stay at top of editor
- [ ] format paint (possibly)
- [ ] release 1.0
- [ ] code block (possibly)
- [ ] line spacing (possibly)
- [ ] equations (possibly)
- [ ] table (possibly)
- [ ] special characters
- [x] `sup`
- [x] `pre`
- [x] handle tab button
- [x] a href (add mouse overlay, etc.)
- [x] change previous history's cursor location if hashes match

## future todo

- [x] make new block styling nodes go inside (this can be done during the fixDisallowedChildrenOfNode process, by entering block nodes (this could break joining, however))
- [x] bug: when list styling `<p><p>abc</p></p><p><p>abc</p></p><p><p>abc</p></p>`, where all Ps have margin, uneven list ordering
- [x] possibly join adjacent lists during indent
- [ ] join adjacent lists during outdent
- [ ] consider joining adjacent list nodes during indent, event at different levels. see `<ol><li><ol><li><ol><li>abc</li></ol></li></ol></li><li><ol><li>abc</li></ol></li></ol>`
- [ ] detectStyling for font sizes (em, etc.), superscript/subscript in css
- [ ] remove extraneous style nodes
- [ ] bugs (fix empty styling elements, may be a possibility of text in empty text thing)
- [ ] bugs (when adjusting start container to be relative to inline nodes in getNextTextNodeInRange and applyStyleToBlockNode, it is not considering empty nodes);
- [ ] maybe think about fixing nested divs when pasting (not joining sufficiently)
- [ ] when adjusting range to be relative to inline nodes, it should properly handle empty nodes and properly traverse
  - it should always move in the direction of the endpoint (left for startContainer, right for endContainer)
  - if it hits the end of the editor:
    - if we are trying to adjust ranges for block styling, it should just use the editor as an endpoint
    - otherwise for getTextNodesInRange it should make a new text node
- [ ] issue with getBlockNodesInRange: if the whole last node is included, include it as a whole (possibilities of fixing this: have tne end node always escape?)
- [ ] perhaps remove extraneous divs during paste

## good editors

- TinyMCE
- Quill
- CKEditor
- Lexical
- Froala
- SyncFusion
