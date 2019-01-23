
* 1.Run `npm install react-native-ldf-grid --save`
* 2.`import Grid from 'react-native-ldf-grid'`

```.js
 render() {
         return (
             <View style={styles.container}>
                 ...
                 <Grid
                    style = {styles.grid}
                    column = {4}
                    data = {this.girdItems}
                    renderItem = {(item, index) => (
                        <HomeGridItem
                            key = {index}
                            item = {item}
                            onPress={() => {}}
                        />
                    )}
                 />
             </View>
         );
 }

```

### Basic usage

```js
render() {
        return (
            <View style={styles.container}>
                <Grid
                   style = {styles.grid}
                   column = {4}
                   data = {this.girdItems}
                   rowSeparatorLineRender = {(index) => (<Line key = {index} />)}
                   columnSeparatorLineRender = {(index) => (
                        <Line key = {index} style = {styles.columnline}/>
                   )}
                   renderItem = {(item, index) => (
                       <HomeGridItem
                           key = {index}
                           item = {item}
                           onPress={() => {}}
                       />
                   )}
                />
            </View>
        );
    }
```

Then you can use it like this:
>1.grid item reload：

```jsx
 this.refs.grid.reloadData(datas);
```

## API

Props              | Type     | Optional | Default     | Description
----------------- | -------- | -------- | ----------- | -----------
style |  ViewPropTypes.style |true | {}  | Custom default grid style
column  | PropTypes.number  | true | 0  |   Set grid column count
renderItem  | PropTypes.func  | true | null  |   Render gird item
rowSeparatorLineRender  | PropTypes.func  | true | null  |   Render grid row separator line
columnSeparatorLineRender  | PropTypes.func  | true | null  |   Render grid column separator line



Method   |  Type     | Optional | Description
----------------- | -------- | -------- | -----------
reloadData(datas)   | function | true | reload grid item render

