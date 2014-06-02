# WWDC2014
![Screenshot as of April 8th](http://www.iosxtools.com/Resource/WWDC2014_App.png)      [http:/www.iosxtools.com](http:/www.iosxtools.com)

A Cocoa OSX App to help you download WWDC2014 videos

* WWDC2014 videos category browse/search

* Preference:download path setting

* Download video selection,download progress indicator

* Social share:twitter & weibo

## About

We are [iOSTools](http:/www.iosxtools.com),a studio  determined to develop the best iOS/OSX tools for developers!

##Usage
in WWDCBO.m file,use local html path to test,in practice you must modify url as a real remote  wwdc 2014 videos http url.

```
- (void)parseWWDCDownloadLink
{
    dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
        NSURL * url = [NSURL URLWithString:@"https://developer.apple.com/videos/wwdc/2014/"];
        //NSString * string = [[NSString alloc]initWithContentsOfURL:url];
        
        //NSString *webContent = [[NSString alloc] initWithContentsOfURL:url usedEncoding:NULL error:NULL];
        
        
        NSString *path = [[NSBundle mainBundle] pathForResource:@"wwdc" ofType:@"html"];
        
        NSString *webContent = [NSString  stringWithContentsOfFile:path usedEncoding:NULL error:NULL];
        }
      
        
        
    });
    
    //parse finished notify
    
}

```


modify url 

```
- (void)parseWWDCDownloadLink
{
    dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
        //modify it as  real videos url
        NSURL * url = [NSURL URLWithString:@"https://developer.apple.com/videos/wwdc/2014/"];
        
        NSString *webContent = [[NSString alloc] initWithContentsOfURL:url usedEncoding:NULL error:NULL];
        
        
        .....
        }
      
        
        
    });
    
    //parse finished notify
    
}

```



## Screenshots

![Screenshot as of April 8th](http://www.iosxtools.com/WWDC2014/resource/WWDC2014_Main_sh_small.png)

![Screenshot as of April 8th](http://www.iosxtools.com/WWDC2014/resource/WWDC2014_Download_Selection_sh_small.png)

![Screenshot as of April 8th](http://www.iosxtools.com/WWDC2014/resource/WWDC2014_App_sh_small.png)

##Development experience
We use [SQLite+](https://itunes.apple.com/cn/app/sqlite+/id831063466?mt=12) Design database,Generate FMDB-Based Model & DAO class;
[iOSXKit](http://www.iosxkit.com/) A Fast Mac App Development Tool, can quickly generate OSX UI Wapper class.
Only take 4 days complete basic WWDC2014 Demo App.



## Acknowledgment


<p><a href="https://github.com/AFNetworking/AFNetworking">AFNetworking</a></p>
<p><a href="https://github.com/tracy-e/OCGumbo">OCGumbo</a></p>
<p><a href="https://github.com/larcus94/LBProgressBar">LBProgressBar</a></p>
<p><a href="https://github.com/bb9z/RFDownloadManager">RFDownloadManager</a></p>
<p><a href="https://github.com/phranck/CNUserNotification">CNUserNotification</a></p>


## License

Available under MIT license