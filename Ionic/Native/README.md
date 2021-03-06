## Camera

```
ionic cordova plugin add cordova-plugin-camera
npm install @ionic-native/camera
```

```
import { Camera } from '@ionic-native/camera/ngx';

constructor(private camera: Camera) { }
```

+ 获取图片

   ```
   getPicture(options?: CameraOptions): Promise<any>
   ```

   + 配置
   
      ```
      @param {CameraOptions} [options]
      ```
      
       ```
       interface CameraOptions {
          /**
           * 像素范围 0-100. Default is 50
           */

          quality?: number;

          /**
           * DATA_URL : 0,   返回base64
           * FILE_URI : 1,   返回file URI. default
           * NATIVE_URI : 2  返回native URI
           */

          destinationType?: number;
       }
       ```




## Photo Library

```
ionic cordova plugin add cordova-plugin-photo-library
npm install @ionic-native/photo-library
```

```
import { PhotoLibrary } from '@ionic-native/photo-library/ngx';

constructor(private photoLibrary: PhotoLibrary) { }
```

+ 获取权限

   ```
   requestAuthorization(options?: RequestAuthorizationOptions): Promise< void >
   ```

+ 保存图片

   ```
   saveImage(url: string, album: AlbumItem | string, options?: GetThumbnailOptions): Promise< LibraryItem >
   ```
   
   + 路径
   
      ```
      @param url {string} URL of a file, or DataURL.
      ```
   
   + 专辑
   
      ```
      @param album {AlbumItem | string} Name of an album or AlbumItem object.
      ```
      
      ```
      interface AlbumItem {
          /**
           * Local id of the album
           */
          id: string;
          title: string;
      }
      ```
