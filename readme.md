# Revuect

A ultra-framework, the features of which encompass both Vue and React.

## Sample

```js
import Revuect from "revuect";
import RevuectDOM from "react-dom";

function FunctionalApp() {
    const [xd, setXd] = useState("xd"); // stateful hooks.

    return (
        <h1>Hello! {xd}</h1>
    )
}

const ObjectalApp = new Revuect({
    // follow the design pattern:
    // data is a function of state
    data() {
        return {
            xd: "xd"
        };
    }

    template: `<h1>{{ xd }}</h1>`, // string-interpolation, the future of webdev
});

// Mounting a Functional Component
RevuectDOM.render(<FunctionalApp />, document.querySelector("main"));

// Mounting a Objectal App
ObjectalApp.$mount("main");