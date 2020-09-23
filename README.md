<div align="center">

## Gradient Back Color \- WinForm


</div>

### Description

Demonstrate how a form's back color could be a gradient color.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Coder14U](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/coder14u.md)
**Level**          |Intermediate
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |C\#
**Category**       |[GUIs](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/guis__10-30.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/coder14u-gradient-back-color-winform__10-1899/archive/master.zip)





### Source Code

```
PASTE THE FOLLOWING CODE IN THE "PAINT" EVENT OF YOUR FORM.
==================================================
Graphics g=e.Graphics;
			Single intWidthdx;
			Single intIncrement=255/this.Width;
			Single intRedDx=0;
			if(intIncrement==0)
			{
				intIncrement+=(float)0.1;
			}
			for(intWidthdx=0;intWidthdx<this.Width;intWidthdx+=intIncrement)
			{
				//intRedDx=intWidthdx;
				if(intWidthdx>255)
				{
					intRedDx=255-(intWidthdx%255);
				}
				else
				{
					intRedDx=intWidthdx;
				}
				g.FillRectangle(new SolidBrush(Color.FromArgb((int)intRedDx,10,80)),intWidthdx,0
					,intIncrement,this.Height );
			}
```

