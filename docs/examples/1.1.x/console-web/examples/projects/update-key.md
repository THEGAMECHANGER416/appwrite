import { Client, Projects } from "packageName";

const client = new Client();

const projects = new Projects(client);

client
    .setEndpoint('https://[HOSTNAME_OR_IP]/v1') // Your API Endpoint
    .setProject('5df5acd0d48c2') // Your project ID
;

const promise = projects.updateKey('[PROJECT_ID]', '[KEY_ID]', '[NAME]', []);

promise.then(function (response) {
    console.log(response); // Success
}, function (error) {
    console.log(error); // Failure
});