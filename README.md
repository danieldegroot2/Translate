FAH Translation Draft

# Folding@home Translation Text Repository

Thank you for helping us reach even more people around the world by adapting the
experience to their native language.

**IMPORTANT UPDATE: We have switched away from YAML format to PO format. Please
read the updates.**

**Before you start translating, please read this README to learn how we
collaborate and how to find out what is already done and what is left to do. **

**Please check out the "Coordination" section, and the
[coordination threads](https://github.com/FoldingCommunity/Translate/labels/coordination-thread)
to find out how your language team is coordinating with each other. Please
submit pull requests to your language team's repository first. Your language
team coordinator will collate all the translation changes, and submit a pull
request to this repository.**

## What has changed?
After the discussion within the translation plugin development team, we have
decided to move from the custom YAML format to the more standardised
[gettext](https://en.wikipedia.org/wiki/Gettext) Portable Object (PO) format.
We have decided to embedding formatting (*not layout*) within the PO files. This
allows each PO file to follow the paragraph structure of the original webpage,
while enabling more flexibility the translated text within each paragraph.

We believe that the format change is necessary for the long term maintainability
of the project. We apologise for the extra work that you have to do. It is
important to note that in software development, sometimes there are occasional
requirements changes that require code refactoring and rewrite. This happens
more often at the beginning of the project. We believe that there will not be
major format changes down the line.

The old YAML-based files are archived in the
[old-yaml branch](https://github.com/FoldingCommunity/Translate/tree/old-yaml).

## How do we translate?
Please copy the files from [Localization/en-US](Localization/en-US) to your
local language folder, e.g. [Localization/zh-CN](Localization/zh-CN), update
the metadata field.  For each file, translate each ``msgid`` to ``msgstr``.

We are certain Markdown for formatting the strings to be translated and the
translated string. We have made the decision to support the following Markdown
syntaxes:

 - Links: e.g. ``[Example](http://example.net/)``
 - Bold text: e.g. ``**Example**``
 - Italic: e.g. ``*example*``

For more information on Markdown, feel free to have a look at
[Github's official guide](https://guides.github.com/features/mastering-markdown/),
 however, we are only supporting the formatting syntaxes statated above.

You can use a text editor, such as [Notepad++](https://notepad-plus-plus.org/)
or [Atom](https://atom.io/). Please **Set your encoding to UTF-8, this is
important!**. Alternatively you can use tools such as
[Poedit](https://poedit.net/) or
[Lokalize](https://kde.org/applications/en/office/org.kde.lokalize). We do not
mind the extra metadata these tools add.

### PO file mandatory metadata
At the top of each PO file, it is mandatory to have the following metadata
fields:

 1. ``Schema-Version`` - The schema version of this PO file, e.g. ``1.2``.
 In future, we may have minor update to the format of the PO files.
 2. ``URL`` - The URL of the webpage that generated the PO file.
 3. ``Source-Language`` - The original language of the webpage, it should be
 ``en-US`. However, as FAH project grows, we may start seeing webpages that were
 written in language that was not English.
 4. ``Source-Version`` - The version code for the source PO file,
  e.g. ``1.2``.
 5. ``Source-Last-Modified`` - The last modification date for the source PO
 file, this must be  in the format of **YYYYMMDD**, e.g. ``20200704``.
 6. ``Target-Language`` - The target language for this PO file, e.g. ``zh-CN``.
 7. ``Target-Version`` - The version code for the target PO file,
 e.g. ``1.2``.
 8. ``Target-Last_Modified`` - The last modification date for this PO file, this
 must be in the format of **YYYYMMDD**, ``20200704``.

Please note that:

 - For dates, ``YYYY`` is the 4-digit year, ``MM`` is the 2-digit month,
 and ``DD`` is the 2-digit day.
 - The ``Source-Version`` should follow the format of ``x.y``, where ``x`` and
 ``y`` are both integers. Increase in ``x`` indicates a major structure
 change, e.g. adding or removing a paragraph. Increase in ``y`` indicates a
  minor change, e.g. a spelling mistake. Note that ``x`` and ``y`` can have
  multiple digits, e.g. ``1.12``. ``y`` should start at 0.
 - The ``Target-Version`` should also follow the format of ``x.y.z``. ``x` and
 ``y`` should follow the ``x`` and ``y`` in ``Original-Version``. ``z`` should
 start at 0. It should be incremented before pushing the updated PO file to the
 main repository. ``z`` should be reset to 0, if a new ``Source-Version`` is
 released.

The metadata block at the top of the file should look like this:

    # Schema-Version: 1.0
    # URL: https://foldingathome.org/diseases/
    # Source-Language: en-US
    # Source-Version: 1.0
    # Source-Last-Modified: 20200705
    # Target-Language: zh-CN
    # Target-Version: 1.0.0
    # Target-Last_Modified: 20200706

## How do I add a PO file?
For now, if you want to add a PO file, please use
[PO file generator](http://wpdev.tshw.de/po-converter.php) created by
[Till Helge](https://github.com/Tar-Minyatur).

This is an alpha version, so you have to manually do these:

 - strip the menu
 - escape the double quotes
 - add the metadata block.

We plan to release a proper tool in a later date to generate PO file properly.

If you do want to add a PO file or modify an existing PO file, please use a **separate** pull request than the normal translation work. This is to maintain
a clean workflow.

### Translation style guide
Please also check out the [Wiki](https://github.com/FoldingCommunity/Translate/wiki)
for the translation style guide. Please feel free to contribute to the Wiki.

We will be adding more examples as translation progress.

## Coordination
There are languages with multiple translators, please organise a team amongst
yourself. Please feel free to use the Folding@home Dev Discord server, or other
communication methods your translation team is comfortable with.

We recommend one member of your language team to fork this repository, and give
write access to all translators within your team, so every member of your team
can commit directly to the forked repository. We would like members within a
language team to discuss and review the translation. Once your team has agreed
upon a final version of the translation, please create a pull request for
this repository.

**Every language team will come up with their own ways of working and also might
be defining guidelines to follow. Check with them to find out what they already
did and where help is needed.**

You can check out the [Wiki](https://github.com/FoldingCommunity/Translate) for
some general guidelines and we would highly recommend joining the development
Discord server to easily coordinate with the other translators (and to avoid
working on the same things).

## What if I need help?
Please feel free to open an Github issue, and tag
[fangfufu](https://github.com/fangfufu/),
[ReadyPlayerEmma](https://github.com/ReadyPlayerEmma)
and/or
[Antonthynell](https://github.com/Antonthynell). Alternatively, you could
post a message in the main transation channel on Folding@home Dev Discord
server and tag one of us.
