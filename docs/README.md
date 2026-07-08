# Dear ReGui
Dear ReGui is a retained dear ImGui library remake designed to be used on Roblox!
This is perfect for beginners and performance.

<!-- > Demo place: https://www.roblox.com/games/136436665525145/ReGui-Demo \ -->
> Documentation: https://depso.gitbook.io/regui

## Notices
- For suggestions or questions, please visit the [discussions page](https://github.com/depthso/Dear-ReGui/discussions)
- If you would like to fork this, please read the [Forking](#forking) section
- Technical documentation and addional infomation such as commonly asked questions can be found on the [Gitbook documentation](https://depso.gitbook.io/regui)

## Demo
The best way to learn ReGUI is to look through the Demo window which comes bundled with ReGUI.
The demo window is updated every significant update such as an addition of an element or a flag has been renamed.

> https://github.com/depthso/Dear-ReGui/blob/main/src/Demo%20window.lua

## Usage
ReGui can be used on any GUI type you want such as CoreGui, PlayerGui, BillboardGui, PluginGui, and SurfaceGui.
Installation is as simple as importing the rbxm model into your project and connecting a client script to begin using it!

ReGui requires prefabs as it does not generate the base elments required for many elements such as the Window.

See the [Getting Started - Installing](https://depso.gitbook.io/regui/getting-started/installing) section for more details

Once you have installed ReGUI into your project, it can be used by any client script anywhere!
```lua
local Window = ReGui:Window({
	Title = "Hello world!",
	Size = UDim2.fromOffset(300, 200)
})

Window:Label({Text="Hello, world!"})
Window:Button({
	Text = "Save",
	Callback = function()
		MySaveFunction()
	end,
})
Window:InputText({Label="string"})
Window:SliderFloat({Label = "float", Minimum = 0.0, Maximum = 1.0})
```

<img 
src="https://github.com/user-attachments/assets/8e92a7e9-a1f8-4e89-8087-a37fa67b91a0">

## Gallery
<table>
	<tr>
		<td width="50%">
			<img src="https://github.com/user-attachments/assets/63474257-2ff6-4733-a193-d9b62530ad94">
		</td>
  		<td width="50%">
			<img src="https://github.com/user-attachments/assets/37db5a36-8356-4419-895c-ee526db275b0">
		</td>
	</tr>
	<tr>
		<td>
			Advanced customization example
			<img src="https://github.com/user-attachments/assets/992a8422-c976-41bd-a087-d3af59cc5d60">
		</td>
		<td>
			Demo window  
			<img src="https://github.com/user-attachments/assets/529b628f-ed3b-4630-af88-53c9090acdca">
		</td>
	</tr>
</table>

## Forking
If you would like to create a fork of ReGui, please read the steps below

<!-- ### Custom module
If you are going to edit the module and publish it, please create a copy of the [Prefabs](https://create.roblox.com/store/asset/71968920594655) 
as the module will quickly become outdated and cause issues with the Prefabs. Currently you only need to download a copy of the `main.lua` file -->

### Custom Prefabs
Using custom prefabs with ReGUI is very simple. 
To use custom prefabs you can point the library's `Prefabs` to the custom prefabs in the `:Init` call. For externally using custom prefabs, replace `rbxassetid://{ReGui.PrefabsId}` with `rbxassetid://PrefabsID` and replace `PrefabsID` with the id of your custom prefabs that you have published on Roblox.

ReGui prefabs asset: [Prefabs Gui - Roblox](https://create.roblox.com/store/asset/71968920594655)
