
<form id="imageUploadForm">
        <input type="file" id="imageInput" accept="image/*" />
        <button type="button" onclick="imageupload()">Submit File</button>
</form>

<script>
        function imageupload() {
            const fileInput = document.getElementById('imageInput');
            const file = fileInput.files[0];

            if (file) {
                const file = fileInput.files[0];
                console.log(file);
                const reader = new FileReader();
               let base64String = ""; // Initialize base64String variable
                reader.readAsDataURL(file); // reading it in
                reader.onload = () => {
                    console.log("here");
                    base64String = btoa(reader.result); // convergin to base 64
                    console.log(base64String);
                }
            } 
            
            else {
                console.error('No file selected.');
            }
        }
</script>


