# databinding
databinding

deze xaml code hieronder is eigenlijk de enige code die je nodig hebt voor databinding
     bij de lebel geeft x:Name aan dat het een globale variabellen is dus dan kan er data aan worden gelinkt
     
     <Label x:Name="label"
               Text="test text"
               HorizontalOptions="Center"
               VerticalOptions="CenterAndExpand" />

  hier bij bindingcontext geef je met x reference aan aan welk object deze word gelinkt in dit geval de label die hierboven is gedeclareerd  value geeft aan welke value hij moet meegeven 
            <Slider x:Name="scaleSlider"
            
                BindingContext="{x:Reference label}"
                Grid.Row="1" Grid.Column="0"
                Maximum="10"
                Value="{Binding Scale, Mode=TwoWay}" />
text is gebind aan de waarde die het slider object hierboven heeft 

            <Label BindingContext="{x:Reference scaleSlider}"
               Text="{Binding Value, StringFormat='Scale = {0:F1}'}"
               Grid.Row="1" Grid.Column="1"
               VerticalTextAlignment="Center" />
