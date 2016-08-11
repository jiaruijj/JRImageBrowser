# JRImageBrowser
图片浏览器   自定义动画  小图看大图 

    初始化
     FNFullImageViewController *fullVc = [[FNFullImageViewController alloc]initWithFullScreenImageArray:self.photoArray currentIndex:0];
 
 
 
    Push动画设置 self.navigationTransitioningStyle  或者 实现[self animationWithType:]
    [fullVc push];
    初始化动画
 
    Present动画设置 ,默认为放大缩小,设置之后用设置的动画
    fullVc.animation = animation;
    [fullVc show];
 
    自定义动画请继承FNBaseAnimatedTransitioning 重写 根据operation 和 present 设置模态动画还是push动画
    - (void)animateTransition:(id<UIViewControllerContextTransitioning>)transitionContext
