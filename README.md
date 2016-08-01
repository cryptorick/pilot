# pilot: Picolisp organization tool
This tool helps you organize your picolisp downloads and installations.  It's fairly easy to do this manually (i.e., without the `pilot` script); however, I keep forgeting where all the bits are, and so I found myself reluctant to (read, just lazy enough not to) update my picolisp install without having a convenience script like this to do it.  Lazy people unite!

# To get started
1. Clone this repo. (Or, simply download the `pilot` script -- it's a monolith.)
2. Put the `pilot` script somewhere on your `$PATH`.  (This is not necessary, but convenient.)
3. Set up a config file in `~/.pilotrc`.  See the file `pilotrc.sample` in this repo for a model/sample.  In short, there are only two items (variables) that need to be set in the config file. The `pilot` script will nag you about them; so you can't miss them. :)
4. You should be ready to go at this point.  Enter `pilot fetch` as your first step.  When it's done, it will tell you what to do next.

# Usages

- `pilot fetch`    downloads the latest distro to `${DISTRODIR}`.
- `pilot get`      is a synonym for `pilot fetch`.
- `pilot extract`  extracts the latest distro (found in `${DISTRODIR}`) into `${BUILDDIR}`.
- `pilot build`    starts the 64-bit (asm) build in the latest picolisp dir in `${BUILDDIR}`.
- `pilot install`  installs the latest build from `${BUILDDIR}` into `${PREFIX}`.
- `pilot update`   is equivalent to `pilot fetch && pilot extract && pilot build && pilot install`.
- `pilot relink`   relinks the pil script to a previously installed version of picolisp.
