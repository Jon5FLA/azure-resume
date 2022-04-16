# azure-resume
My azure supported resume, following [ACG Project Video.](https://www.youtube.com/watch?v=ieYrBWmkfno)

## First steps

- Frontend floder contains the website.
- main.js contains visitor counter code.

```js
window.addEventListener("DOMContentLoaded", (event) =>{
    getVisitCount()
})

const functionApi = '';

const getVisitCount = () => {
    let count = 30;
    fetch(functionApi).then(Response => {
        return Response.json()
    }).then(Response =>{
        console.log("Website called function API.");
        count = Response.count;
        document.getElementById("counter").innerText = count;
    }).catch(function(error){
        console.log(error);
    });
    return count;
```

