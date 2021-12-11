# Azure Storage Blob Upload from a Node.js Web Application:

#### NodeJS Installation:

```nodejs
# Using Ubuntu
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs
```
This sample demonstrates how to use the Azure Storage SDK in the context of an Express application to upload images into Azure Blob Storage.

**Clone the repository to your machine:**
```bash
git clone https://github.com/Azure-Samples/storage-blob-upload-from-webapp-node.git
```
**Change into the storage-blob-upload-from-webapp-node folder:**
```bash
cd storage-blob-upload-from-webapp-node
```
**Install dependencies via npm:**
```bash
npm install
```
# Adding a connection string
1. Navigate to the Azure Portal and copy the connection string from your storage account (under Settings > Access keys) in to the `.env.example` file. Once you have pasted your connection string in to the file, rename the file from `.env.example` to `.env`.

2. Go to storage account > Container > Create a new container `i)thumbnails` `ii)images`
 
### Running the sample
Start the server in virtual machine:
```bash
npm start 
```
Navigate to http://localhost:3000 or (puplic IP):3000 and upload an image to blob storage.

# Output:
![image](https://user-images.githubusercontent.com/71425992/145670542-fe92e832-b960-4365-b518-52726b45da17.png)

![image](https://user-images.githubusercontent.com/71425992/145670532-c142714f-005e-4b15-adfb-192d272b9078.png)
