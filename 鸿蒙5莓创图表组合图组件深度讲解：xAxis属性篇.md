### Hello and welcome back to our special session on HarmonyOS 5 Meichuang chart components! In this episode, we'll explore the detailed usage of the `xAxis` property in combined chart components. The `xAxis` is a crucial configuration object for controlling the display and styling of the X-axis, and mastering its properties is essential for customizing charts.  


## 1. `type`  
**Function**: Specifies the type of the X-axis.  
**Type**: String  
**Default**: `'data'`  
**Options**: `'data'` (category axis), `'value'` (value axis)  
**Scenario**: Use `'data'` for categorical axes and `'value'` for numerical axes.  
**Code Example**:  
```json
xAxis: {
  type: 'data', // Set as category axis
  data: ['January', 'February', 'March']
}
```  


## 2. `name`  
**Function**: Sets the name of the X-axis.  
**Type**: String  
**Default**: `''` (empty string)  
**Scenario**: Add descriptive text to the X-axis.  
**Code Example**:  
```json
xAxis: {
  name: 'Month', // Display X-axis name
  nameGap: 15
}
```  


## 3. `show`  
**Function**: Controls whether the X-axis is displayed.  
**Type**: Boolean  
**Default**: `true`  
**Scenario**: Hide the X-axis by setting to `false`.  
**Code Example**:  
```json
xAxis: {
  show: false // Hide X-axis
}
```  


## 4. `position`  
**Function**: Sets the position of the X-axis.  
**Type**: String  
**Default**: `'bottom'`  
**Options**: `'bottom'` (bottom), `'top'` (top)  
**Scenario**: Display the X-axis at the top of the chart.  
**Code Example**:  
```json
xAxis: {
  position: 'top' // X-axis at the top
}
```  


## 5. `nameGap`  
**Function**: Sets the distance between the axis name and the axis line.  
**Type**: Number  
**Default**: `15`  
**Scenario**: Adjust the spacing between the axis name and the axis line.  
**Code Example**:  
```json
xAxis: {
  name: 'Month',
  nameGap: 20 // Increase distance between name and axis line
}
```  


## 6. `nameLocation`  
**Function**: Sets the position of the axis name.  
**Type**: String  
**Default**: `'end'`  
**Options**: `'start'` (start), `'center'` (center), `'end'` (end)  
**Scenario**: Control the alignment of the axis name on the axis line.  
**Code Example**:  
```json
xAxis: {
  name: 'Month',
  nameLocation: 'center' // Name centered
}
```  


## 7. `nameTextStyle`  
**Function**: Sets the text style of the axis name.  

### 7.1 `color`  
**Function**: Sets the text color of the name.  
**Type**: String  
**Default**: `'#999'`  
**Code Example**:  
```json
nameTextStyle: {
  color: '#333' // Dark text
}
```  

### 7.2 `fontSize`  
**Function**: Sets the text size of the name.  
**Type**: Number  
**Default**: `22`  
**Code Example**:  
```json
nameTextStyle: {
  fontSize: 18 // Smaller font size
}
```  

### 7.3 `fontWeight`  
**Function**: Sets the font weight of the name.  
**Type**: String  
**Default**: `'normal'`  
**Code Example**:  
```json
nameTextStyle: {
  fontWeight: 'bold' // Bold text
}
```  

### 7.4 `fontFamily`  
**Function**: Sets the font family of the name.  
**Type**: String  
**Default**: `'sans-serif'`  
**Code Example**:  
```json
nameTextStyle: {
  fontFamily: 'Microsoft YaHei' // Specify font
}
```  

**Complete Example**:  
```json
xAxis: {
  name: 'Month',
  nameTextStyle: {
    color: '#1890FF',
    fontSize: 16,
    fontWeight: 'bold',
    fontFamily: 'Arial'
  }
}
```  


## 8. `min`  
**Function**: Sets the minimum value of the axis.  
**Type**: String|Number  
**Default**: `null`  
**Scenario**: Force specify the axis range.  
**Code Example**:  
```json
xAxis: {
  type: 'value',
  min: 0 // Minimum starts at 0
}
```  


## 9. `max`  
**Function**: Sets the maximum value of the axis.  
**Type**: String|Number  
**Default**: `null`  
**Scenario**: Force specify the axis range.  
**Code Example**:  
```json
xAxis: {
  type: 'value',
  max: 100 // Maximum up to 100
}
```  


## 10. `interval`  
**Function**: Forces the axis division interval.  
**Type**: Number  
**Default**: `null`  
**Scenario**: Fix the axis tick interval.  
**Code Example**:  
```json
xAxis: {
  type: 'value',
  interval: 20 // One tick every 20 units
}
```  


## 11. `minInterval`  
**Function**: Sets the minimum division interval.  
**Type**: Number  
**Default**: `null`  
**Scenario**: Prevent automatically calculated intervals from being too small.  
**Code Example**:  
```json
xAxis: {
  type: 'value',
  minInterval: 1 // Minimum interval is 1
}
```  


## 12. `maxInterval`  
**Function**: Sets the maximum division interval.  
**Type**: Number  
**Default**: `null`  
**Scenario**: Prevent automatically calculated intervals from being too large.  
**Code Example**:  
```json
xAxis: {
  type: 'value',
  maxInterval: 100 // Maximum interval is 100
}
```  


## 13. `boundaryGap`  
**Function**: Controls whether to leave space at the axis ends.  
**Type**: Boolean  
**Default**: `null`  
**Scenario**: Set to `false` to have the chart紧贴 (close to) the axis edges.  
**Code Example**:  
```json
xAxis: {
  boundaryGap: false // No space at ends
}
```  


## 14. `splitNumber`  
**Function**: Sets the number of axis divisions.  
**Type**: Number  
**Default**: `5`  
**Scenario**: Control the number of axis ticks.  
**Code Example**:  
```json
xAxis: {
  splitNumber: 4 // Divided into 4 segments
}
```  


## 15. `axisLine`  
**Function**: Sets the style of the axis line.  

### 15.1 `show`  
**Function**: Whether to show the axis line.  
**Type**: Boolean  
**Default**: `true`  
**Code Example**:  
```json
axisLine: {
  show: false // Hide axis line
}
```  

### 15.2 `lineStyle`  
**Function**: Sets the axis line style.  

#### 15.2.1 `color`  
**Function**: Sets the axis line color.  
**Type**: String  
**Default**: `'#DDE2EB'`  
**Code Example**:  
```json
lineStyle: {
  color: '#1890FF' // Blue axis line
}
```  

#### 15.2.2 `width`  
**Function**: Sets the axis line width.  
**Type**: Number  
**Default**: `1`  
**Code Example**:  
```json
lineStyle: {
  width: 2 // Thickened axis line
}
```  

#### 15.2.3 `lineDash`  
**Function**: Sets the axis line dashed style.  
**Type**: Array  
**Default**: `null`  
**Code Example**:  
```json
lineStyle: {
  lineDash: [5, 5] // Dashed style
}
```  

**Complete Example**:  
```json
xAxis: {
  axisLine: {
    show: true,
    lineStyle: {
      color: '#666',
      width: 2,
      lineDash: [5, 3]
    }
  }
}
```  


## 16. `axisTick`  
**Function**: Sets the style of the axis ticks.  

### 16.1 `show`  
**Function**: Whether to show the ticks.  
**Type**: Boolean  
**Default**: `true`  
**Code Example**:  
```json
axisTick: {
  show: false // Hide ticks
}
```  

### 16.2 `lineStyle`  
**Function**: Sets the tick line style.  
**Type**: Object  
**Default**: `{color: '#DDE2EB', width: 1, lineDash: null}`  
**Code Example**:  
```json
axisTick: {
  lineStyle: {
    color: '#FF0000',
    width: 2
  }
}
```  

### 16.3 `interval`  
**Function**: Sets the interval between ticks and labels.  
**Type**: Number  
**Default**: `4`  
**Code Example**:  
```json
axisTick: {
  interval: 8 // Increase interval
}
```  

### 16.4 `length`  
**Function**: Sets the tick line length.  
**Type**: Number  
**Default**: `5`  
**Code Example**:  
```json
axisTick: {
  length: 10 // Lengthen ticks
}
```  

**Complete Example**:  
```json
xAxis: {
  axisTick: {
    show: true,
    lineStyle: {
      color: '#333',
      width: 1
    },
    interval: 6,
    length: 8
  }
}
```  


## 17. `axisLabel`  
**Function**: Sets the style of the axis labels.  

### 17.1 `show`  
**Function**: Whether to show the labels.  
**Type**: Boolean  
**Default**: `true`  
**Code Example**:  
```json
axisLabel: {
  show: false // Hide labels
}
```  

### 17.2 `formatter`  
**Function**: Formats the label content.  
**Type**: String|Function  
**Default**: `null`  
**Code Example**:  
```json
// String formatting
axisLabel: {
  formatter: '{value}月'
}

// Function formatting
axisLabel: {
  formatter: (value) => `${value}月份`
}
```  

### 17.3 `color`  
**Function**: Sets the label text color.  
**Type**: String  
**Default**: `'#999999'`  
**Code Example**:  
```json
axisLabel: {
  color: '#333' // Dark labels
}
```  

### 17.4 `fontSize`  
**Function**: Sets the label text size.  
**Type**: Number  
**Default**: `22`  
**Code Example**:  
```json
axisLabel: {
  fontSize: 16 // Smaller font size
}
```  

### 17.5 `fontWeight`  
**Function**: Sets the label text weight.  
**Type**: Number  
**Default**: `400`  
**Code Example**:  
```json
axisLabel: {
  fontWeight: 600 // Bold
}
```  

### 17.6 `fontFamily`  
**Function**: Sets the label text font.  
**Type**: String  
**Default**: `'sans-serif'`  
**Code Example**:  
```json
axisLabel: {
  fontFamily: 'Microsoft YaHei'
}
```  

### 17.7 `rotate`  
**Function**: Sets the label rotation angle.  
**Type**: Number  
**Default**: `0`  
**Code Example**:  
```json
axisLabel: {
  rotate: 45 // 45-degree tilt
}
```  

### 17.8 `interval`  
**Function**: Sets the label display interval.  
**Type**: String|Number  
**Default**: `null`  
**Code Example**:  
```json
axisLabel: {
  interval: 2 // Show one label every 2 items
}
```  

### 17.9 `width`  
**Function**: Sets the label text width.  
**Type**: Number|null  
**Default**: `null`  
**Code Example**:  
```json
axisLabel: {
  width: 60 // Fixed width
}
```  

### 17.10 `overflow`  
**Function**: Sets the handling for text overflow.  
**Type**: String  
**Default**: `'none'`  
**Options**: `'none'` (none), `'truncate'` (truncate), `'breakAll'` (wrap)  
**Code Example**:  
```json
axisLabel: {
  overflow: 'truncate' // Truncate overflow
}
```  

### 17.11 `margin`  
**Function**: Sets the distance between labels and tick lines.  
**Type**: Number  
**Default**: `5`  
**Code Example**:  
```json
axisLabel: {
  margin: 10 // Increase distance
}
```  

### 17.12 `shadowColor`  
**Function**: Sets the text shadow color.  
**Type**: String  
**Default**: `'rgba(0, 0, 0, 0)'`  
**Code Example**:  
```json
axisLabel: {
  shadowColor: 'rgba(0, 0, 0, 0.5)'
}
```  

### 17.13 `shadowBlur`  
**Function**: Sets the shadow blur size.  
**Type**: Number  
**Default**: `0`  
**Code Example**:  
```json
axisLabel: {
  shadowBlur: 5
}
```  

### 17.14 `shadowOffsetX`  
**Function**: Sets the shadow X-axis offset.  
**Type**: Number  
**Default**: `0`  
**Code Example**:  
```json
axisLabel: {
  shadowOffsetX: 2
}
```  

### 17.15 `shadowOffsetY`  
**Function**: Sets the shadow Y-axis offset.  
**Type**: Number  
**Default**: `0`  
**Code Example**:  
```json
axisLabel: {
  shadowOffsetY: 2
}
```  

**Complete Example**:  
```json
xAxis: {
  axisLabel: {
    show: true,
    formatter: '{value}月',
    color: '#666',
    fontSize: 14,
    fontWeight: 500,
    fontFamily: 'Arial',
    rotate: 30,
    interval: 1,
    width: 80,
    overflow: 'truncate',
    margin: 8,
    shadowColor: 'rgba(0, 0, 0, 0.2)',
    shadowBlur: 3,
    shadowOffsetX: 1,
    shadowOffsetY: 1
  }
}
```  


## 18. `splitLine`  
**Function**: Sets the style of the axis split lines.  

### 18.1 `show`  
**Function**: Whether to show split lines.  
**Type**: Boolean  
**Default**: `false`  
**Code Example**:  
```json
splitLine: {
  show: true // Show split lines
}
```  

### 18.2 `lineStyle`  
**Function**: Sets the split line style.  

#### 18.2.1 `color`  
**Function**: Sets the split line color.  
**Type**: String  
**Default**: `'#DDE2EB'`  
**Code Example**:  
```json
lineStyle: {
  color: '#EEE' // Light gray
}
```  

#### 18.2.2 `width`  
**Function**: Sets the split line width.  
**Type**: Number  
**Default**: `1`  
**Code Example**:  
```json
lineStyle: {
  width: 1
}
```  

#### 18.2.3 `lineDash`  
**Function**: Sets the split line dashed style.  
**Type**: Array  
**Default**: `null`  
**Code Example**:  
```json
lineStyle: {
  lineDash: [3, 3] // Dashed
}
```  

**Complete Example**:  
```json
xAxis: {
  splitLine: {
    show: true,
    lineStyle: {
      color: '#F0F0F0',
      width: 1,
      lineDash: [3, 3]
    }
  }
}
```  


## 19. `data`  
**Function**: Sets the data items of the X-axis.  
**Type**: Array  
**Default**: `[]`  
**Scenario**: Use when the X-axis is a category axis.  
**Code Example**:  
```json
xAxis: {
  data: ['January', 'February', 'March', 'April', 'May']
}
```  


## 20. `rLevel`  
**Function**: Sets the rendering level of the X-axis.  
**Type**: Number  
**Default**: `-20`  
**Scenario**: Adjust the stacking order of the X-axis with other elements.  
**Code Example**:  
```json
xAxis: {
  rLevel: -10 // Increase level
}
```  


## 21. `animationCurve`  
**Function**: Sets the X-axis animation easing.  
**Type**: String  
**Default**:
