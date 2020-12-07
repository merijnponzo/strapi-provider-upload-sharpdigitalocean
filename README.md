# strapi-provider-upload-sharpdigitalocean

add

```
"thumb": {
      "type": "string",
      "configurable": false,
      "required": true
    },
```

to extensions/upload/models/File.settings.json

add

```
upload: {
    provider: "sharpdigitalocean",
    providerOptions: {
      accessKeyId: "YOUR_ACCESS_KEY_ID",
      secretAccessKey: "YOUR_SECRET_ACCESS_KEY",
      endpoint: "YOUR_SPACE_ENDPOINT eg ny1.digitaloceanspaces.com",
      optimize: {
        size: 1000,
        thumbnail_size: 500,
      },
      settings: {
        awsUploadFolder: "CUSTOM_FOLDER_NAME_IN_YOUR_BUCKET",
      },
      params: {
        Bucket: "YOUR_SPACE_BUCKET_NAME",
      },
    },
  },

```

to config/ENV/plugins.js
