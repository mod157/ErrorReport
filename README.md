#
***DELETE_FAILED_INTERNAL_ERROR
Error while Installing APKs***
```
 File > Settings > Build, Execution, Deployment > Instant Run > Uncheck : Enable Instant Run
```

#Autogeneration Error : Cannot mark directory
```
 Press F4 into Project Structure, Check SDKs on left
 Click Modules ---> Source Tab, check gen and src as sources
```
#java.lang.IllegalStateException: Object is no longer managed by Realm. Has it been deleted?
```
삭제 후에 뷰에서 삭제도 같이 처리해줘야함.
 notifyItemRemoved(position);
```

#java.lang.RuntimeException: java.lang.RuntimeException: Exception occured on reading file /storage/emulated/0/camtest/SS.jpg
```
Permission 처리 필요( read, write storge)

<provider
            android:name="android.support.v4.content.FileProvider"
            android:authorities="com.your.package.fileProvider"
            android:grantUriPermissions="true"
            android:exported="false">
            <meta-data
                android:name="android.support.FILE_PROVIDER_PATHS"
                android:resource="@xml/file_paths" />
        </provider>

        <?xml version="1.0" encoding="utf-8"?>
<paths>
    <external-path path="Android/data/com.your.package/" name="files_root" />
    <external-path path="." name="external_storage_root" />
</paths>
```
#IndexOutOfBoundsException
