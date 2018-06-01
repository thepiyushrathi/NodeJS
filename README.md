# NodeJS
NodeJS material for interview

# REPL
Read Eval Print Loop
* Used to execute ad-hoc javascript statement.REPL provides direct entry to javascript into shell prompt and evaluates the results.

# Types of functions in NodeJs
* Blocking Function
Blocks the execution of next line of code until any I/O event that is being waites occurs.
Blocking functions execute synchronously

var fsObj = require(fs);
var fileData = fsObj.readFileSync('./readme.txt'); //blocks the code execution until entire file get read
console.log(data);
moreWork(); // will work after console.log

* Non-Blocking
Do not wait for I/O event that is being waited for occurance and executes next line of code.
Function executes asynchronously.

var fsObj = require(fs);
fs.readFile('./readme.txt', (err, data) => {
if (err) throw err;
console.log(data);
});
moreWork();// executes before console.log

# Commonly used NodeJS modules/dependencies like for HTTP, Email, Schema, ORM etc.

# What are 'Streams' in NodeJS?
Streams are objects that allows reading of data from source & writing data at the destination as continous process.

Types of streams :
* reading stream
* writing stream
* Both reading & writing
* Duplex - perform computation over the available input.

# What are Exit code in NodeJS
Exit codes are used to end a NodeJS process

* Unused
* Uncaught fatal exception
* fatal error
* Non functional internal exception handler
* Internal exception handler run time failure
* Internal javascript evealuation failure

# What are Globals in NodeJS?
Three keyword are global in NodeJs
* Global
* Process
* Buffer

# handle unhandled exception
process.on('uncaughtException', (err)=>{
console.log("Caught error : " + err);
})

# Does NodeJS support multi-processor platform and takes full advantage of it?
NodeJs is single-threaded 7 runs on single process, However it have core module - Cluster, which enables to run multiple NodeJs worker process which share same port.
