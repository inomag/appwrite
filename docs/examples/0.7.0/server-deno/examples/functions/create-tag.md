import * as sdk from "https://deno.land/x/appwrite/mod.ts";

// Init SDK
let client = new sdk.Client();

let functions = new sdk.Functions(client);

client
    .setProject('5df5acd0d48c2') // Your project ID
    .setKey('919c2d18fb5d4...a2ae413da83346ad2') // Your secret API key
;


let promise = functions.createTag('[FUNCTION_ID]', '[COMMAND]', new File([fileBlob], 'file.png'));

promise.then(function (response) {
    console.log(response);
}, function (error) {
    console.log(error);
});