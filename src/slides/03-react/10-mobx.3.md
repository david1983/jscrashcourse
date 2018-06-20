### mobx - core concepts

3. modify the state

```javascript
//state.js
import {observable} from 'mobx';

class AppState{

    constructor(){
        setInterval(this.increment, 1000)
    }
    @action resetTimer(){
        this.timer = 0
    }
    @action increment(){        
        this.timer++        
    }
    @observable timer = 0
}

export default new AppState()
```


