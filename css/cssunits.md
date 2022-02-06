# Notes from [Kyle](https://youtu.be/-GR52czEd-0?list=TLPQMTIxMjIwMjEdglL3IyoAHg)'s CSS Units vid

### Here we go

---
Been trying to learn this one as well.
---
### Difference between *px* and *%*

*px* are absolute ofc and will stay the same no matter whatever width or height the page has or will have while *%* is relative because it is a percentage of its parent element's properties. This is easy.

### View-width(*vw*) and View-height(*vh*)

*this is the difficult part*

- 1 vw = 1 % of the screen's width so 50vw is half of the screen width and 100vw is the whole screens's width.
>Although being the same unit with having *%*, **%** are relative to their parents while *vw* is relative to the screen/device's width.
- 1 vh = 1 % of the height of the screen. 50vh is half of the screen height and 100vh is the screen's height.

---
### "rem" vs "em"

- both are relative.
- not to anything but the font size of the parent. 
- rem = related to *root* font size, em = related to *parent*'s font size *so 1 rem is always the same everywhere on the page because its relative to the root font size: but 1em is always gonna be different because its based on its parent font. ems will grow bigger and bigger when they get nested more and more.
---
### % on fonts 

- works the same as ems as they both are based on parent's. 
- 1em = 100% and next 1em = 100% gonna be bigger

---
### fr(fractional) unit
- just used in flexbox to set each widths'

# Welp! That is for now bye.
---
# From Kevin Powell.
`px` is not relative.
- Font size? Use `rem`. 
- Setting a width? Use `%` | `max-width`. Or `ch`(width of a character of that font). Might be useful for typography.
- Setting a height? (Rare?) Use a min-height.
- Setting a padding or margin? `em` or `rem`
- Media Queries?: use `em`
- Use `px` only for shadow-offseting or smaller stuff.