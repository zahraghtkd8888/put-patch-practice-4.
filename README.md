# put-patch-p

fetch("https://api.github.com/repos/USERNAME/put-patch-practice", {
  method: "PATCH",
  headers: {
    "Accept": "application/vnd.github+json",
    "Authorization": "Bearer YOUR_TOKEN",
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    description: "Updated using PATCH"
  })
})
.then(async response => {
  console.log("HTTP Status:", response.status);
  console.log(await response.json());
});
