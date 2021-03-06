---
layout: home

title: Box Layout
order: 1

redirect_from:
  - /layout/

---

As discussed in [Container and Layouts](/basics/container.html) elements
within a container can be arranged using a layout. This section explores
the builtin layouts and how to use them.

The most commonly used layout is `layout.BoxLayout` and it has two variants,
horizontal and vertical. A box layout arranges all elements in a single
row or column with optional spaces to assist alignment.

A horizontal box layout, created with `layout.NewHBoxLayout()` creates
an arrangement of items in a single row. Every item in the box will
have it's width set to it's `MinSize().Width` and the height will be
equal for all items, the largest of all the `MinSize().Height` values.
The layout can be used in a container or you can use the box widget
`widget.NewHBox()`.

A vertical box layout is similar but it arranges items in a column.
Each item will have it's height set to minimum and all the widths will
be equal, set to the largest of the minimum widths.

To create an expanding space between elements (so that some are left
aligned and the others right alighed, for example) add a `layout.NewSpacer()`
as one of the items. A spacer will expand to fill all available space.
Adding a spacer at the beginning of a vertical box layout will cause
all items to be bottom aligned. You can add one to the beginning and
end of a horizontal arrangement to create a center alignment.