# upload_images_app
android app - upload images to firebase database


to add these methods from https://stackoverflow.com/questions/37367137/unable-to-get-uri-from-storage-reference-on-firebase : 
```
 FirebaseStorage storage = FirebaseStorage.getInstance();
    StorageReference storageRef = storage.getReferenceFromUrl(this.getString(R.string.storage_path));
    Uri uri = storageRef.child("groups/pizza.png").getDownloadUrl().getResult();
    
storageRef.child("groups/pizza.png").getDownloadUrl().addOnSuccessListener(new OnSuccessListener<Uri>() {
    @Override
    public void onSuccess(Uri uri) {
        // TODO: handle uri
    }
}).addOnFailureListener(new OnFailureListener() {
    @Override
    public void onFailure(@NonNull Exception exception) {
        // Handle any errors
    }
});
```
