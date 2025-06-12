# CSS - Position

![CSS_POSITION](../images/css-position.png)

- Parent Element
- Child Element

# CSS Properties :
| Properties | Valuess                                   |
| ---------- | ----------------------------------------- |
| `postion`  | `static`, `relative`, `fixed`, `absolute` |
| `top`      | `px`, `cm`, `mm`, `in`, `pt` . . . etc    |
| `bottom`   | `px`, `cm`, `mm`, `in`, `pt` . . . etc    |
| `left`     | `px`, `cm`, `mm`, `in`, `pt` . . . etc    |
| `right`    | `px`, `cm`, `mm`, `in`, `pt` . . . etc    |

---

### Usage Examples

##### Parent Element CSS:
```css
.parent-1 {
    position: static;
}

.parent-2 {
    position: relative;
}
```
##### Child Element CSS:
```css
.child-1 {
    position: relative;
    bottom: 20px;
    right: 20px;
    left: 20px;
    top: 20px;
}

.child-1 {
    position: absolute;
    bottom: 20px;
    right: 20px;
    left: 20px;
    top: 20px;
}

.child-2 {
    position: fixed;
    bottom: 20px;
    right: 20px;
    left: 20px;
    top: 20px;
}
```