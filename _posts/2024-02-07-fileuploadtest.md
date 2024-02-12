
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
                    // console.log("here234");
                    // console.log(reader.result);
                    base64String = btoa(reader.result); // convergin to base 64
                    // console.log(base64String);
                    const url = 'http://127.0.0.1:8086/api/users/images';
                    const body = {
                        
                        Image: base64String
                    };
                    console.log(body);
                    const AuthOptions = {
                                mode: 'cors', // no-cors, *cors, same-origin
                                credentials: 'include', // include, same-origin, omit
                                headers: {
                                    'Content-Type': 'application/json',
                                },
                                method: 'POST', // Override the method property
                                cache: 'no-cache', // Set the cache property
                                body: JSON.stringify(body)
                            };
                        // fetch the API
                        fetch(url, AuthOptions)
                        // response is a RESTful "promise" on any successful fetch
                        .then(response => {
                            // check for response errors and display
                            if (response.status !== 200) {
                                window.location.href = "http://127.0.0.1:4200/student/2024/01/31/403error.html";
                            }
                            // valid response will contain JSON data
                            response.json().then(data => {
                            // insert whatever code you want here
                            window.location.href="http://127.0.0.1:4200/student/2024/01/30/DataTable.html"; // reload pge
                            })
                        })
                        // catch fetch errors (ie ACCESS to server blocked)
                        .catch(err => {
                        console.log(err)
                        });
                                    
                    }
            } 
            
            else {
                console.error('No file selected.');
            }
            

            
                // uploading to the database

        }
</script>


