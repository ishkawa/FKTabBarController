FKTabBarController
==================
FKTabBarController is intended to change the tabbar and items instead of UITabBarController

![FKTabBarController screenshot](https://raw.github.com/chion/FKTabBarController/master/Demo/screenshot.png "Screenshot")

### Example Usage

```objective-c
FKTabBarController *tabBarController = [[FKTabBarController alloc]initWithNibName:nil bundle:nil];
NSMutableArray *viewControllers = @[].mutableCopy;
NSMutableArray *items = @[].mutableCopy;
for (int i=0; i<4; i++) {
    UINavigationController *nc = [[UINavigationController alloc] initWithRootViewController:[[DemoViewController alloc]initWithNibName:nil bundle:nil]];
    [viewControllers addObject:nc];
    UIImage *icon = [UIImage imageWithColor:[UIColor clearColor]];
    [items addObject:[[FKTabBarItem alloc] initWithIcon:icon
                                          selectedColor:[UIColor blackColor]
                                        unselectedColor:[UIColor grayColor]]];
}
tabBarController.viewController = viewController;
tabBarController.tabBar.items = items;
```

### License

FKTabBarController is available under the MIT license.
