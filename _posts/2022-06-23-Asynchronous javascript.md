---
Layout:
Title: "Asynchronous javascript"
Date: 2022-06-17
Categories:
---

# Introduction

Today i have learned about Asynchronous Programming javascript
Asynchronous programming is a form of parallel programming that allows a unit of work to run separately from the primary application thread. When the work is complete, it notifies the main thread (as well as whether the work was completed or failed). There are numerous benefits to using it, such as improved application performance and enhanced responsiveness.
# body

 like all things in programming, it’s not something that you should use in every instance; in fact, there are some situations in which you should avoid it. Asynchronous programming has actually been around for a long time, but in recent years, it’s become more widely used. 

 some examples of asynchronous programming :

 <//setTimeout

 setTimeout(() => {

 console.log('waited 1 second')
 
 },1000); 

//nested setTimeouts

 setTimeout(() => { 
     console.log('waited 3 second') 
     setTimeout(() => {     
     console.log('waited 2 second')    
     setTimeout(() => {         
     console.log('waited 1 second')    
    },1000); 
  },1000);
 },1000);
 
//button event handler in browser javascript
const btn = A;
btn.addEventListener('click', () => {
     this is one of the common method
 })



//error first callback
fs.readFile('./text.txt', {encoding:'utf-8'}, (err, data) => {
if(err){
    console.log('Error');
    console.log(err)
}else {
    console.log('GOT DATA')
    console.log(data)
}
})

//**************promises************** 

//Create a promise

const myPromise = new Promise((resolve, reject)  => {
     const rand = Math.floor(Math.random() * 2);
     if(rand === 0){
        resolve();
     }else{
        reject();
     }
});

myPromise
 .then(() => console.log('Success'))
.catch(() =>console.log('Something went wrong'));

//fs readFile with promises

fs.promises
    .readFile('./text.txt', {encoding: 'utf-8'})
    .then((data) => console.log(data))
    .catch((err) => console.error(err));

//fetch with promises

fetch('https://twitch.tv/jamesqquick')
 .then((res) => res.json())
 .then((data) => console.log(data))
 .catch((err) => console.error(err));

 //***************Async/Await*****************

 //load file with async/await

 const loadFile = async () => {

    try{
        const data = await fs.promises.readFile('./text.txt', {
            encoding: 'utf-8',

        });
    } catch(error) {
        console.error(error)
    }


 };

 loadFile();

 //fetch a link with async/await without error handling

 const fetchList = async (id) => {
     
     try{
     const res = await fetch(`https://twitch.tv/jamesqquick/${id}`);
     const data = await res.json; 
    console.log(data)
     }catch (error){
        console.error(err);

     }
 };
 fetchList(2);>

# conclusion
The asynchronous nature of JavaScript to understanding the language. You'll find the use of callbacks, promises, and async/await in code that you write every day as a JavaScript developer.