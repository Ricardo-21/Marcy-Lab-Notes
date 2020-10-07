# Flex box

__display: flex;__

* justify-content <- moves 'boxes' by the (main/horizontal) axis (_Aligns flex items along the main axis_)
  * commands to use on the property |  __flex-start (default)__ | __flex-end__ | __center__  |  __space-between__ | __space-around__|
* align-items <- moves 'boxes' by the y axis (_Aligns flex items along the cross axis_)
  * commands to use on the property | __flex-start__ | __flex-end__ | __center__ | __baseline__ | __stretch (default)__ | 
* flex-direction <- moves 'boxes' bases on cols and rows (_Defines the direction of the main axis_)
  * commands to use | __row (default)__ | __row-reverse__ | __column__ | __column-reverse__ |
* order <- You can move the items order (must be selected) (_Specifies the order of the flex item_)
  * ex. (order: 2) this would move item to second position (_< integer > (... -1, 0 (default), 1, ...)_)
* align-self <- aligns an item, overrides align-items (_Aligns a flex item along the cross axis, overriding the align-items value_)
  * commands to use | __flex-start__ | __flex-end__ | __center__ | __baselines__ | __stretch__ |
* flex-wrap <- works similar to box-inline and box (_Specifies whether flex items are forced on a single line or can be wrapped on multiple lines_)
  * commands to use | __nowrap (default)__ | __wrap__ | __wrap-reverse__ | 
* flex-flow <- (_Shorthand property for flex-direction and flex-wrap_)
  * commmands to use | __ < flex-direction > < flex-wrap > __ |
* align-content <- (_Aligns a flex container's lines within the flex container when there is extra space on the cross-axis_)
  * commands to use | __flex-start__ | __flex-end__ | __center__ | __space-between__ | __space-around__ | __stretch (default)__|
* flex-grow <- similar to order but makes individual items larger
  * ex. (flex-grow: 2;) this would enlarge the individual item
* flex-basis <- Works similar to width
  * (We can use px,%)

  
