# Untitled

```text
import React from "react";

class portfolio extends React.Component {

    constructor(props){
        super(props);
        console.log("cunstructr()");
    }
 
        state = {
            count:0,  
          };

       add = () => { 
           console.log("add");
           //this.state.count += 1;
        //    this.setState({count:1});
        // this.setState({count: this.state.count +1});
        this.setState((current)=> ({
            count: current.count + 1,
        }));
    };
    minus = () => {
        console.log("minus");
        this.setState((current)=> ({
            count: current.count - 1,
        }));
};


componentDidMount(){
    console.log("componentDidMount");
}

componentDidUpdate(){
    console.log("componentDidUpdate");
}
componentWillUnmount(){
    console.log("componentWillUnmount")
}


    render(){
        return(
            <div>
                <h1>Class{this.state.count}  </h1>
                <button onClick={this.add}>add</button>
                <button onClick={this.minus}>minus</button>
            </div>
        )
    }
}

export default portfolio;
```

