# How-to-create-a-Glass-Like-TabView-in-.NET-MAUI

A sample application that demonstrates how to create a glass-like `TabView` in .NET MAUI. Syncfusion’s .NET MAUI TabView provides built-in support for a glass-like visual effect through the `EnableLiquidGlassEffect` property. To enable or disable the liquid glass effect on the TabView, set the `EnableLiquidGlassEffect` property in `SfTabView`.

## Prerequisites

* Visual Studio 2026 with .NET MAUI workload

## How to run this sample

1. Clone the repository.
2. Open the solution file `TabView.sln` in Visual Studio 2026.
3. Build and run the project.

## Code Snippet

To achieve the glass-like effect, use below code.

```xml
    <Grid>
        <Image Source="liquidglassimage1.jpg" Aspect="AspectFill"/>
        <Border Margin="5" WidthRequest="450" BackgroundColor="Transparent" HorizontalOptions="Center">
            <tabView:SfTabView x:Name="tabView" 
                               EnableLiquidGlassEffect="True"
                               TabBarHeight="75"
                               TabWidthMode="Default"
                               EnableSwiping="True"
                               TabBarPlacement="Bottom"                                                       
                               IndicatorPlacement="Fill">
                <tabView:SfTabView.Items>
                    <tabView:SfTabItem Header="Favorites" ImagePosition="Top" >
                        <tabView:SfTabItem.Content>
                            <Grid>
                                <Grid Grid.Row="1" VerticalOptions="End"  HeightRequest="20">
                                </Grid>
                                <ScrollView HorizontalScrollBarVisibility="Never" VerticalScrollBarVisibility="Never">
                                    <VerticalStackLayout>
                                        <BindableLayout.ItemsSource>
                                            <x:Array Type="{x:Type x:String}">
                                                <x:String>James</x:String>
                                                <x:String>Richard</x:String>
                                                <x:String>Michael</x:String>
                                                <x:String>Alex</x:String>
                                                <x:String>Clara</x:String>
                                            </x:Array>
                                        </BindableLayout.ItemsSource>
                                        <BindableLayout.ItemTemplate>
                                            <DataTemplate x:DataType="{x:Type x:String}">
                                                <Grid ColumnDefinitions="*" HeightRequest="35" Margin="10,5">
                                                    <Label Grid.Column="0" 
                                        VerticalOptions="Center" 
                                        HorizontalOptions="Start"                                                       
                                        FontSize="16" 
                                        Text="{Binding}"/>
                                                </Grid>
                                            </DataTemplate>
                                        </BindableLayout.ItemTemplate>
                                    </VerticalStackLayout>
                                </ScrollView>
                            </Grid>
                        </tabView:SfTabItem.Content>
                    </tabView:SfTabItem >
                    <tabView:SfTabItem Header="Recents" ImagePosition="Top">
                        <tabView:SfTabItem.Content>
                            <Grid>
                                <Grid Grid.Row="1" VerticalOptions="End"  HeightRequest="20">
                                </Grid>
                                <ScrollView HorizontalScrollBarVisibility="Never" VerticalScrollBarVisibility="Never">
                                    <VerticalStackLayout>
                                        <BindableLayout.ItemsSource>
                                            <x:Array Type="{x:Type x:String}">
                                                <x:String>James</x:String>
                                                <x:String>Richard</x:String>
                                                <x:String>Michael</x:String>
                                                <x:String>Alex</x:String>
                                                <x:String>Clara</x:String>
                                            </x:Array>
                                        </BindableLayout.ItemsSource>
                                        <BindableLayout.ItemTemplate>
                                            <DataTemplate x:DataType="{x:Type x:String}">
                                                <Grid ColumnDefinitions="*" HeightRequest="35" Margin="10,5">
                                                    <Label Grid.Column="0" 
                                                           VerticalOptions="Center" 
                                                           HorizontalOptions="Start"                                                       
                                                           FontSize="16" 
                                                           Text="{Binding}"/>
                                                </Grid>
                                            </DataTemplate>
                                        </BindableLayout.ItemTemplate>
                                    </VerticalStackLayout>
                                </ScrollView>
                            </Grid>
                        </tabView:SfTabItem.Content>
                    </tabView:SfTabItem>
                </tabView:SfTabView.Items>
            </tabView:SfTabView>
        </Border>
    </Grid>
```

## Further references

* [TabView Liquid Glass ](https://help.syncfusion.com/maui/tabview/liquidglasssupport)

