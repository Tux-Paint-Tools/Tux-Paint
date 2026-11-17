# Tux Paint A Playful Canvas for Young Artists

Explore tux paint tools through short drawing activities that leave room for a child's own choices.
Tux Paint combines brushes, shapes, stamps, text, and visual effects with a simple interface and a helpful penguin mascot.

## Turn a few marks into a picture

Begin with a small subject, such as a garden, a friendly creature, or a view from a window.
The goal is to connect each tool with an idea the child wants to express.

- Use Paint for a winding path, clouds, or an invented creature.
- Add Lines for a fence, a roof edge, or a geometric pattern.
- Combine Shapes into a house, vehicle, or abstract arrangement.
- Try one Magic effect and observe which part of the picture changes.
- Use Undo to compare an experiment with the previous version.

Introduce a second tool after the child can recognize the result of the first.
Leave time to describe the picture instead of turning every activity into a sequence to copy.
The tux paint software interface keeps the drawing area alongside tool and option selectors.

[![Create in Tux Paint](https://img.shields.io/badge/Create%20in-Tux%20Paint-DB2777?style=flat&labelColor=831843)](https://tux-paint-tools.github.io/Tux-Paint/)

## Give stamps a role in the story

A tux paint drawing can combine original marks with reusable pictures.
Place one stamp, then ask what belongs around it: a habitat, a road, a weather pattern, or another character.

The stamp collection is distributed separately from the main application.
Choose a small collection that fits the activity and review its contents before the session.
Scaling and placement turn the same image into different parts of a composition.

### Define a custom symbol's behavior

For tux paint stamps, an image can have a matching plain-text data file with the .dat extension.
For an original letter-shaped PNG stamp, these options allow color selection while preventing flipping and mirroring:

```text
colorable
nomirror
noflip
```

Use the same basename for the image and data file, such as letter-a.png and letter-a.dat.
The [extension guide](https://tuxpaint.org/docs/en/html/EXTENDING.html) documents the image, description, and option files.
Colorable stamps use the image's transparency to define a solid shape in the selected color.
Restart Tux Paint after changing custom content so it can discover the new files.

![A child-created garden combining freehand paths with carefully placed animal stamps](FOTO)

## Adjust the session to the room and input device

A shared activity may need a quiet window on a projector rather than a full-screen session with sounds.
On a Linux system with Tux Paint available in the command path, this launches a quiet window at the requested size:

```bash
tuxpaint --windowed --1024x768 --nosound
```

The [options documentation](https://tuxpaint.org/docs/en/html/OPTIONS.html) describes these launch settings and their configuration equivalents.
The command changes this launch's options; it does not edit the saved configuration.
Check that the drawing area and controls remain comfortable to use on the actual display.

### Keep repeated classroom choices in configuration

A plain-text configuration can make routine choices consistent across sessions.
For example, these entries disable printing, remove the shape-rotation step, and request larger buttons:

```ini
noprint=yes
simpleshapes=yes
buttonsize=64
```

Add the entries to the platform's Tux Paint configuration file, rather than a drawing or stamp file.
The available button size depends on how much space the chosen window provides.
Keep only the restrictions that support the activity; revisit them as the user's confidence grows.
Command-line options can override configuration settings.

## Match a gesture to the intended mark

Show how a tool responds before asking for a finished picture.
A useful demonstration changes one thing at a time: the tool, the color, or the selected shape.

| Tool | Typical interaction | Picture element | Activity idea |
| --- | --- | --- | --- |
| Paint | Drag across the canvas | A freehand stroke | Draw paths with different brush sizes |
| Lines | Drag between endpoints | A straight segment | Construct a fence or star pattern |
| Shapes | Drag to set size | A geometric shape | Combine shapes into an imaginary vehicle |
| Stamp | Position and place an image | A reusable object | Build a scene around one character |
| Magic | Use the selected effect's interaction | An effect or special mark | Compare a small area before and after |

Magic tools have different behaviors, so the selected tool's instructions matter.
Try an effect on a small area before using it across a picture.
Undo provides a way to compare outcomes without requiring a perfect first attempt.

![A colorful scene built from simple geometry with one demonstrated Magic effect](FOTO)

## Keep a picture available for the next activity

Use Save before ending a session and Open to return to a thumbnail of earlier work.
Ask the child to recognize the picture and describe what they want to add.
For a shared computer, agree how different users' work will be kept distinct.

Printing can be part of a supervised activity when it is enabled.
A paper copy and a saved drawing serve different purposes, so retain the saved work for later changes.
The [official documentation](https://tuxpaint.org/docs/en/html/README.html) explains the drawing tools and picture controls.

## Pinta reference files supplied with this collection

### Desktop integration and packaging

The Pinta manual page is [pinta.1](xdg/pinta.1).
[com.github.PintaProject.Pinta.desktop.in](xdg/com.github.PintaProject.Pinta.desktop.in) defines desktop launch metadata.
[com.github.PintaProject.Pinta.metainfo.xml.in](xdg/com.github.PintaProject.Pinta.metainfo.xml.in) provides application metadata.
[Makefile.am](xdg/Makefile.am) installs these desktop resources.
The Snap recipe is [snapcraft.yaml](snap/snapcraft.yaml), with its launcher in [pinta.desktop](snap/gui/pinta.desktop).

### Interface components

[AddinManagerDialog.cs](Pinta.Gui.Addins/AddinManagerDialog.cs) implements the Pinta add-in manager window.
[InstallDialog.cs](Pinta.Gui.Addins/InstallDialog.cs) handles add-in installation interactions.
[AddinListView.cs](Pinta.Gui.Addins/AddinListView.cs) displays add-in entries.
[AddinInfoView.cs](Pinta.Gui.Addins/AddinInfoView.cs) presents details for a selected entry.
[StatusProgressBar.cs](Pinta.Gui.Addins/StatusProgressBar.cs) reports progress, warnings, and errors.
[SettingNames.cs](Pinta.Docking/SettingNames.cs) defines keys for dock layout settings.
[readme.txt](Pinta.Docking/readme.txt) explains the docking library's origins.

### Build and dependency context

[Directory.Build.props](Directory.Build.props) contains shared .NET build properties.
[Directory.Packages.props](Directory.Packages.props) centralizes package versions.
[ReferenceGirCoreGtk40.props](properties/ReferenceGirCoreGtk40.props) references the GTK bindings.
[ReferenceGirCoreAdw1.props](properties/ReferenceGirCoreAdw1.props) references the Adwaita bindings.
[ReferenceGirCorePangoCairo10.props](properties/ReferenceGirCorePangoCairo10.props) references the PangoCairo bindings.
[configure.ac](configure.ac) defines Autoconf configuration checks.
[CHANGELOG.md](CHANGELOG.md) records Pinta development changes.

The uploaded files are a partial Pinta snapshot; Tux Paint application sources and stamp collections are absent.
These Pinta references describe a separate image editor and do not define Tux Paint tools or build requirements.
Tux Paint's own application and content repositories are listed on its [official Git page](https://tuxpaint.org/download/source/git/).

## Related Search Terms

tux paint tools, tux paint, tux paint software, tux paint drawing, tux paint stamps, drawing, painting, art, education, kids, brushes, stamps, raster-graphics, accessibility, open-source
