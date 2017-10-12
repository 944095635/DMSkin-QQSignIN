# DMSkin-for-DMSkin-Small

<h3>自用WPF UI无边框方案</h3>
<h4>支持：.NET Framework 3.5 - 4.7</h4>
<h4>支持：Windows XP - Windows 10</h4>
<hr/>
<h1>前言</h1>
<img  src="https://raw.githubusercontent.com/944095635/DMSkin-for-WPF/master/图片/A.png" />
DMSkin.WPF M 是我自己开发WPF用的UI框架，开源到github。（以下简称DFW）。

<h1>核心</h1>
DFW实现了比较完美的无边框窗体方案，并且拖拽全部采用WIN32消息实现。拖拽依靠桌面边缘完美,高DPI支持,窗体不会变形或异常

另外,由于我对MVVM不擅长，所以DEMO并不是采用MVVM框架。


<h1>注意事项</h1>
本源码采用VS2017 个人版 开发,部分C# 6.0+语法 vs2015 vs2013 vs2012 请自行修改源码中不支持的部分。

<h1>版本更新</h1>
<blockquote>
<h3>1.0.0.0 (2017-9-21)</h3>
<p>1.此项目正式上线。</p>
</blockquote>


<h1>相关</h1>

加入讨论

<h3>C#.NET 2000人 QQ群： 76566523</h3>
<h3>DMSkin QQ群： 194684812</h3>

<h2>我的QQ:944095635</h2>
官网：http://www.dmskin.com

<h1>帮助改进</h1>
非常欢迎参与DFW的改进。有钱出钱有力出力，如果你觉得DFW很棒，请支持我。
如果你需要相关的资源或者学习资料也请联系我。
<img style="width:200px;" src="https://github.com/944095635/DMSkin-for-WPF/blob/master/%E5%9B%BE%E7%89%87/JZ.jpg" />

<h1>使用说明</h1>
<pre>
<code>
1.引用DMSkin.WPF.DLL
2.Window继承修改为:MainWindow : DMSkinWindow
3.添加引用:xmlns:DMSkin="clr-namespace:DMSkin.WPF;assembly=DMSkin.WPF"
4.XAML继承修改为: DMSkin:DMSkinWindow x:Class="DMSkin.WPF.Test.MainWindow"
</code>
</pre>


<h1>窗体属性</h1>
<pre>
<code>      
Foreground="White"                    //前景色 
Background="White"                    //背景色 
DMShowMin="True"                      //显示系统按钮-最小化
DMShowMax="True"                      //显示系统按钮-最大化
DMShowClose="True"                    //显示系统按钮-关闭
DMWindowShadowSize="10"               //窗体边框阴影大小
DMWindowShadowColor="#FFC8C8C8"       //窗体边框阴影颜色
DMWindowShadowDragVisibility="False"  //窗体拖动时是否显示阴影层
DMWindowShadowVisibility="False"      //窗体是否有阴影层[关闭阴影层]
DMWindowShadowBackColor="#FF323CAD"   //阴影背景色,选择跟主窗体相近的颜色 拉伸跟拖动 用户体验更好|#FF323CAD 为蓝色
DMSystemButtonSize="50"               //系统按钮大小
DMSystemButtonForeground="#FF666666"  //系统按钮[文字]颜色
DMSystemButtonHoverColor="#33000000"  //系统按钮的鼠标悬浮[背景]色
DMSystemButtonHoverForeground="White" //系统按钮的鼠标悬浮[文字]颜色
DMSystemButtonCloseHoverColor="Red"   //系统【关闭】按钮的鼠标悬浮[背景]色-默认为红色
DMSystemButtonShadowEffect="0"        //系统按钮的阴影大小
ResizeMode="CanResize"                //边框拉伸方案CanResiz和CanResizeWithGrip
Height="700" Width="1000"             //窗体大小
MinHeight="268" MinWidth="360"        //窗体最大以及最小属性
WindowStartupLocation="CenterScreen"  //窗体初始位置
<br/>
<del>DMMetroBorderColor="#FFC8C8C8"  //窗体边框颜色-仅Metro有效   --2.0中移除</del>
<del>DMMetroBorderSize="1"           //边框大小-仅Metro有效   --2.0中移除</del>
<del>DMWindow="Shadow"               //Shadow-阴影模式  Metro-线条扁平化模式   --2.0中移除</del>
</code>
</pre>


<h1>资源引用</h1>
<pre>
<code>
&lt;Application.Resources&gt;
            &lt;ResourceDictionary&gt;
                &lt;ResourceDictionary.MergedDictionaries&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.WPF;Component/Themes/DMSkin.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.WPF;Component/Themes/DMColor.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.WPF;Component/Themes/DMScrollViewer.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.Wpf;component/Themes/DMButton.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.Wpf;component/Themes/DMTabControl.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.Wpf;component/Themes/DMRadioButton.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.Wpf;component/Themes/DMTreeView.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.Wpf;component/Themes/DMDataGrid.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.Wpf;component/Themes/DMListBox.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.Wpf;component/Themes/DMSlider.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.Wpf;component/Themes/DMCheckBox.xaml" /&gt;
                &lt;ResourceDictionary Source="pack://application:,,,/DMSkin.Wpf;component/Themes/DMContextMenu.xaml" /&gt;
                &lt;/ResourceDictionary.MergedDictionaries&gt;
            &lt;/ResourceDictionary&gt;
&lt;/Application.Resources&gt;
</code>
</pre>

<h1>通用模板</h1>
<pre>
<code>
&lt;Grid&gt;
        &lt;Grid Background="White"&gt;
            &lt;Border Grid.Column="0" BorderThickness="0,0,0,2" BorderBrush="{StaticResource LineColor}" VerticalAlignment="Top"&gt;
                &lt;Grid&gt;
                    &lt;TextBlock Foreground="{StaticResource MainColor}" Text="DMSkin"  FontSize="20"
                           HorizontalAlignment="Left" VerticalAlignment="Center" Margin="10,0,0,0"/&gt;
                    &lt;Button  Name="ButtonSkin"
                                ToolTip="主题"
                                Focusable="False"
                                Style="{DynamicResource CaptionButtonStyle}"
                                Padding="0" HorizontalContentAlignment="Center" HorizontalAlignment="Right" Margin="0,0,150,0" Width="50" Height="50" 
                                &gt;
                        &lt;Label Foreground="#FF555555" 
                                       Content="X" FontSize="22" 
                                       HorizontalContentAlignment="Center" FontWeight="Bold"  &gt;&lt;/Label&gt;
                    &lt;/Button&gt;
                &lt;/Grid&gt;
            &lt;/Border&gt;
        &lt;/Grid&gt;
        &lt;ResizeGrip  HorizontalContentAlignment="Stretch" VerticalContentAlignment="Stretch" VerticalAlignment="Bottom" HorizontalAlignment="Right"&gt;&lt;/ResizeGrip&gt;
&lt;/Grid&gt;
</code>
</pre>

<h1>圆角窗体</h1>
<pre>
<code>
&lt;Border Background="White" CornerRadius="5"  BorderThickness="1"&gt;
        &lt;Border.Effect&gt;
            &lt;DropShadowEffect BlurRadius="12" ShadowDepth="0" Color="#88000000"/&gt;
        &lt;/Border.Effect&gt;
        &lt;Grid Margin="0,0,0,0"&gt;
            &lt;Grid Background="Transparent"&gt;
                &lt;Grid.RowDefinitions&gt;
                    &lt;RowDefinition Height="30"&gt;&lt;/RowDefinition&gt;
                    &lt;RowDefinition Height="*"&gt;&lt;/RowDefinition&gt;
                    &lt;RowDefinition Height="30"&gt;&lt;/RowDefinition&gt;
                &lt;/Grid.RowDefinitions&gt;
                &lt;Grid Grid.Row="0" Name="DMTitle"&gt;
                &lt;/Grid&gt;
            &lt;/Grid&gt;
            &lt;ResizeGrip VerticalContentAlignment="Bottom" HorizontalContentAlignment="Right" HorizontalAlignment="Right" VerticalAlignment="Bottom"&gt;&lt;/ResizeGrip&gt;
        &lt;/Grid&gt;
&lt;/Border&gt;
</code>
</pre>

<h1>更多效果图</1>
<img  src="https://raw.githubusercontent.com/944095635/DMSkin-for-WPF/master/图片/A (1).gif" />
<img  src="https://raw.githubusercontent.com/944095635/DMSkin-for-WPF/master/图片/A (2).jpg" />
<img  src="https://raw.githubusercontent.com/944095635/DMSkin-for-WPF/master/图片/B.png" />
<img  src="https://raw.githubusercontent.com/944095635/DMSkin-for-WPF/master/图片/A (3).jpg" />
<img  src="https://raw.githubusercontent.com/944095635/DMSkin-for-WPF/master/图片/A (4).jpg" />
