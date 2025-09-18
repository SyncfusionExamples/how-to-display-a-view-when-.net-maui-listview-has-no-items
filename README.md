# how-to-display-a-view-when-.net-maui-listview-has-no-items
This demo shows how to display a custom view when .NET MAUI ListView has no items.

## Sample

```xaml
<syncfusion:SfListView x:Name="listView" 
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
            <code>
            . . .
            . . .
            <code>
        </DataTemplate>
    </syncfusion:SfListView.ItemTemplate>
</syncfusion:SfListView>
```