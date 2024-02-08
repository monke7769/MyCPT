
<form id="imageUploadForm">
        <input type="file" id="imageInput" accept="image/*" />
        <button type="button" onclick="imageupload()">Submit File</button>
</form>

<script>
        function imageupload() {
            const fileInput = document.getElementById('imageInput');
            const file = fileInput.files[0];
            let base64String = ""; // Initialize base64String variable
            if (file) {
                const file = fileInput.files[0];
                console.log(file);
                const reader = new FileReader();
               
                reader.readAsDataURL(file); // reading it in
                reader.onload = () => {
                    console.log("here");
                    base64String = btoa(reader.result); // convergin to base 64
                    
                }
            } 
            
            else {
                console.error('No file selected.');
            }
            // console.log(base64String);

            const url ='http://127.0.0.1:8086/api/users/design';
            const body = {
                name:"Tarun",
                content:"content",
                image:base64String,
                type:"public",

            };
            console.log(body);

            // Change options according to Authentication requirements
            const authOptions = {
                mode: 'cors', // no-cors, *cors, same-origin
                credentials: 'include', // include, same-origin, omit
                headers: {
                    'Content-Type': 'application/json',
                },
                method: 'POST', // Override the method property
                cache: 'no-cache', // Set the cache property
                body: JSON.stringify(body)
            };

            // Fetch JWT
            fetch(url, authOptions)
            .then(response => {
                // handle error response from Web API
                if (!response.ok) {
                    const errorMsg = 'Login error: ' + response.status;
                    console.log(errorMsg);
                    return;
                }
                console.log("uploaded");
                // Success!!!
                // Redirect to the database page
                
            })
            // catch fetch errors (ie ACCESS to server blocked)
            .catch(err => {

                console.error(err);
            });
                // uploading to the database

        }
</script>


