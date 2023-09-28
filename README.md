# how-to-display-a-view-when-.net-maui-listview-has-no-items

This demo shows how to display a custom view when .NET MAUI ListView has no items.

## XAML 
<syncfusion:SfListView x:Name="listView" 
            Grid.Row="3"
            SelectionMode="None"                                     
            ItemsSource="{Binding Items}"                      
            ItemSize="56">

    <syncfusion:SfListView.EmptyView>
        <StackLayout VerticalOptions="CenterAndExpand">
            <Label Text="&#xe725;" FontSize="40" TextColor="#666666" Opacity="0.8"
                    FontFamily="{OnPlatform iOS=ListViewFontIcons, MacCatalyst=ListViewFontIcons, Android=ListViewFontIcons.ttf#, UWP=ListViewFontIcons.ttf#ListViewFontIcons}"
                    HorizontalTextAlignment="Center" VerticalTextAlignment="Center" />
            <Label TextColor="#666666" Text="No Items" FontSize="16" FontFamily="Roboto-Regular" HorizontalTextAlignment="Center" VerticalTextAlignment="Center"  Margin="0,10,0,0"/>                        
        </StackLayout>                    
    </syncfusion:SfListView.EmptyView>

    <syncfusion:SfListView.ItemTemplate>
        <DataTemplate x:Name="ItemTemplate">
          ---
        </DataTemplate>
    </syncfusion:SfListView.ItemTemplate>
</syncfusion:SfListView>

## Requirements to run the demo

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/)
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## Troubleshooting

### Path too long exception

If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
