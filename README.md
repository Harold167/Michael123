print("HI Emervin")local a={"7f926de7-ea29-4500-9b24-93a0b7e8f20a"}local b=Instance.new("ScreenGui")local c=Instance.new("Frame")local d=Instance.new("Frame")local e=Instance.new("Frame")local f=Instance.new("TextButton")local g=Instance.new("UIGridLayout")local h=Instance.new("TextButton")local i=Instance.new("TextButton")local j=Instance.new("TextButton")local k=Instance.new("UIListLayout")function StylizeGuiProperties()b.Parent=game.Players.LocalPlayer:WaitForChild("PlayerGui")b.ZIndexBehavior=Enum.ZIndexBehavior.Sibling;c.Parent=b;c.BackgroundColor3=Color3.fromRGB(26,26,28)c.BorderSizePixel=0;c.Position=UDim2.new(0.25,0,0.25,0)c.Size=UDim2.new(0.25,0,0,250)d.Name="DragFrame"d.Parent=c;d.BackgroundColor3=Color3.fromRGB(26,26,28)d.BackgroundTransparency=1.000;d.BorderSizePixel=0;d.Size=UDim2.new(1,0,0.150000006,0)d.Draggable=true;d.Active=true;d.Selectable=true;e.Name="MainFrame"e.Parent=c;e.BackgroundColor3=Color3.fromRGB(26,26,28)e.BackgroundTransparency=1.000;e.BorderSizePixel=0;e.Size=UDim2.new(1,0,0.850000024,0)f.Name="ResetButton"f.Parent=e;f.BackgroundColor3=Color3.fromRGB(255,47,47)f.BorderSizePixel=0;f.Size=UDim2.new(1,0,0,50)f.Font=Enum.Font.SourceSans;f.Text="Reset"f.TextColor3=Color3.fromRGB(255,255,255)f.TextSize=35.000;f.TextWrapped=true;g.Parent=e;g.SortOrder=Enum.SortOrder.LayoutOrder;g.VerticalAlignment=Enum.VerticalAlignment.Bottom;g.CellPadding=UDim2.new(0,0,0,0)g.CellSize=UDim2.new(1,0,0,50)h.Name="FiveMinutes"h.Parent=e;h.BackgroundColor3=Color3.fromRGB(3,202,0)h.BorderSizePixel=0;h.Size=UDim2.new(1,0,0,50)h.Font=Enum.Font.SourceSans;h.Text="5 Minutes"h.TextColor3=Color3.fromRGB(255,255,255)h.TextSize=35.000;h.TextWrapped=true;i.Name="TenMinutes"i.Parent=e;i.BackgroundColor3=Color3.fromRGB(1,109,0)i.BorderSizePixel=0;i.Size=UDim2.new(1,0,0,50)i.Font=Enum.Font.SourceSans;i.Text="10 Minutes"i.TextColor3=Color3.fromRGB(255,255,255)i.TextSize=35.000;i.TextWrapped=true;j.Name="FifteenMinutes"j.Parent=e;j.BackgroundColor3=Color3.fromRGB(0,42,0)j.BorderSizePixel=0;j.Size=UDim2.new(1,0,0,50)j.Font=Enum.Font.SourceSans;j.Text="15 Minutes"j.TextColor3=Color3.fromRGB(255,255,255)j.TextSize=35.000;j.TextWrapped=true;k.Parent=c;k.SortOrder=Enum.SortOrder.LayoutOrder;b.Parent=game.Players.LocalPlayer.PlayerGui end;StylizeGuiProperties()function ExecuteRemote(l,m)l:FireServer(m[1],m[2])end;function MinutesToSecond(n)return math.floor(n*60)end;local o,p,q=0,0,false;local r=false;task.spawn(function()while task.wait(0.1)do print('Looping')if q then print('Finsihed')r=true;wait(1)o=0;p=p;q=false;r=false end;if p>0 and q==false and r~=true then print('Requesting RepeatInstance')print(o,p,q)if o==p then print('Final Reached')q=true else o=o+1;ExecuteRemote(workspace["__THINGS"]["__REMOTES"].MAIN,{"b","bank withdraw"})for s,t in pairs(a)do local u={[1]=t,[2]={},[3]=s}game.Workspace["__THINGS"]["__REMOTES"]["bank withdraw"]:InvokeServer(u)end end end end end)f.MouseButton1Click:Connect(function()print("Resetting")q=true;o=0;p=0 end)h.MouseButton1Click:Connect(function()print("Converting to Five Minutes.",o,q,p)q=false;o=0;p=MinutesToSecond(5)print("Converted to Five Minutes.",o,q,p)end)i.MouseButton1Click:Connect(function()print("Converting to Ten Minutes.",o,q,p)q=false;o=0;p=MinutesToSecond(10)print("Converted to Ten Minutes.",o,q,p)end)j.MouseButton1Click:Connect(function()print("Converting to Fifteen Minutes.",o,q,p)q=false;o=0;p=MinutesToSecond(15)print("Converted to Fifteen Minutes.",o,q,p)end)
