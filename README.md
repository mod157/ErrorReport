#[Android]
***DELETE_FAILED_INTERNAL_ERROR
Error while Installing APKs***
```
 File > Settings > Build, Execution, Deployment > Instant Run > Uncheck : Enable Instant Run
```

#[Android] Autogeneration Error : Cannot mark directory
```
 Press F4 into Project Structure, Check SDKs on left
 Click Modules ---> Source Tab, check gen and src as sources
```
#[Android] java.lang.IllegalStateException: Object is no longer managed by Realm. Has it been deleted?
```
삭제 후에 뷰에서 삭제도 같이 처리해줘야함.
 notifyItemRemoved(position);
```

#[Android] java.lang.RuntimeException: java.lang.RuntimeException: Exception occured on reading file /storage/emulated/0/camtest/SS.jpg
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
#[Android] IndexOutOfBoundsException

#[Android] Error:Execution failed for task ':app:processDebugResources'.
#com.android.ide.common.process.ProcessException: Failed to execute aapt
```
compat을 build시 삭제하면 발생, 찾지 못했기에 발생한다.
```

#[Android] IllegalThreadStateException: Thread already started
```
쓰레드가 사용중이라 발생하는 현상, 레디 체크 후 시작
if(!thread.isAlive()){
thread.start();
}


```

#java.lang.RuntimeException: Unable to instantiate application
```
폴더 중에 한글이 있는지 확인
https://translate.googleusercontent.com/translate_c?depth=1&hl=ko&prev=search&rurl=translate.google.co.kr&sl=en&sp=nmt4&u=https://stackoverflow.com/questions/32171968/your-project-path-contains-non-ascii-characters-android-studio&usg=ALkJrhihaiVypjtcoSEzqS_h8SREMOtdMw

```




#[Unity3D] unity system.io.ports not found
 ```
  Edit>ProjectSettings>Player>ApiCompatibilityLevel 에서 .NET 2.0으로 변환(Sub X)
 ```
#[Unity3D] CommandInvokationFailure: Unable to list target platforms. Please make sure the android sdk path is correct.
```
tools 버전이 업그레이드 되면서 Unity가 빠진듯 함.
다운그레이 하면 잘됨.
http://answers.unity3d.com/questions/1320150/unable-to-list-target-platform.html
```
#[Unity3D] gradle build failed see the console for details
#[Unity3D] CommandInvokationFailure: Gradle build failed.
```
java9을 8으로 다운그레이 해결
```

#[Unity3D] MissingComponentException: There is no 'Renderer' attached to the "VideoController" game object, but a script is trying to access it.

#CS0103: The name ## does not exist in the current context
```
존재하지 않는 Context가 존재, 사용 되어지는 부분에서 삭제
```

#[Unity3D] is an incorrect path for a scene file. BuildPlayer expects paths relative to the project folder.
```

Scene path를 찾지 못해서 발생
Build에서 Scene을 다시 추가해주면 해결
```

#[Unity3D] CheckConsistency: GameObject does not reference component MonoBehaviour. Fixing.
```
신 전환 후 발생하지 않음
```
#[Unity3D] Shadow map cache entry with NULL shadowmap?
```
Screen Space Shadows in Custom
Edit > ProjectSettings >  graphics > Built-in Shader Settings > Screen Space Shadows > Built-in shader
```

#[Unity3D] Non-convex MeshCollider with non-kinematic Rigidbody is no longer supported in Unity 5.
```
remove Rigidbody
```

#[Unity3D] Screenspace cascaded shadow map support is disabled in graphics settings
```
Edit > ProjectSettings >  graphics > Built-in Shader Settings > Screen Space Shadows > Built-in shader
```
#[Oculus Go] Oculus go Ocullus update Require
```
1. 오큘러스 고 페어링 초기화
2. 스마트폰 Oculus 어플 재셜치
3. 페어링 초기화
```
