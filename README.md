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
