## Jest - NodeJS

```javascript
const person = {
    name: "davide",
    surname: "andreazzini"
    fullname: ()=>`${this.name} ${this.surname}`
}

describe("person ", () => {
	it("should have a name and a surname", () => {
        expect(person).toHaveProperty("name")
        expect(person).toHaveProperty("surname")
    })
    //    
})

```