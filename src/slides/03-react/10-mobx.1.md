### mobx - core concepts

1. define a state and make it observable

```javascript
//state.js
import {observable} from 'mobx';

class AppState{

    constructor(){
        setinterval(this.increment, 1000)
    }
    @action resetTimer(){
        this.timer = 0
    }
    @action increment(){        
        this.timer++        
    }
    @observable timer = 0
}
```


