
# Useful-Javascript-Tricks
This repository is can contains some useful JavaScript methods and tricks. 

### To hide query parmas in next js
```
 router.push({ pathname: `/your-path-name`, query: { key: value } }, `/your-path-name`)
```

### To block invalid charectors on keydown
```
const blockInvalidChar = e => ['e', 'E', '+', '-', '.'].includes(e.key) && e.preventDefault()
```

### Get year dropdown value from specific year to current year
```
//pass the minimum year that you want like 2000 
const getYears =(minYear)=>{
let currentYear = new Date().getFullYear()
    const yearOptions = []
    let earliestYear = minYear
    while (currentYear >= earliestYear) {
      yearOptions?.push({
        label: currentYear,
        value: currentYear
      })
      currentYear -= 1
    }
    return yearOptions
}
```
### On Enter prevent any action
```
function onKeyDown(keyEvent) {
    if ((keyEvent.charCode || keyEvent.keyCode) === 13) {
      keyEvent.preventDefault()
    }
  }
```
