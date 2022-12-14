```
/* ************************************************************************** */
/*                                                                            */
/*                                                        :::      ::::::::   */
/*   cub3d                                              :+:      :+:    :+:   */
/*                                                    +:+ +:+         +:+     */
/*   By: makhtar <makhtar@student.42Abudhabi.ae>    +#+  +:+       +#+        */
/*   By: hawadh <hawadh@student.42Abudhabi.ae>    +#+#+#+#+#+   +#+           */
/*   Created: 2022/06/21 17:31:03 by makhtar           #+#    #+#             */
/*   Created: 2022/06/21 17:31:31 by hawadh           ###   ########.fr       */
/*                                                                            */
/* ************************************************************************** */
```

```
***NOTES:***
NULL

```

`#BUGS: NULL`

1.	~~***HA:***	Segfaul in `get_next_line();` due to `ft_strchr();` in `libft`~~
2.	~~***HA:***	Function parses whole file, should stop at first line of map~~
3.	~~***HA:***	Leak in `extract_file();` line `#26`~~
4.	~~***HA:***	Segfault when moving mouse in window in function `mlx_mouse_get_pos();` in function `draw_cursor();`~~
5.	~~***HA:***	Crosshair was not drawing~~
6.	~~***HA:***	Map printed with extra spaces~~
7.	~~***HA:***	Memory leak in `parse_layout();` in my function `store_confg_map();` line `#47`~~
8.	~~***MAK:*** Parser returning invalid map on checking walls if any `0` is present, `line #13` in file.cub~~
9.	~~***HA:***	xpm file opening failing~~
10.	~~***HA:***	On full screen, pause causes window to turn red if window resized to full screen~~
11.	~~***HA:***	Parser function `check_tabs();` had issue with iteration (Did I write this late night?) where `i = -1` and `while (++i > 0)`~~
12.	~~***HA:***	in `add_xpm();` image not placing in only Blue~~
13.	~~***HA:***	Map not redrawing on clearing window when hitting pause button a second time~~
14.	~~***HA:***	Minimap skipping areas and not drawing in walls~~
15. ~~***HA:***	Minimap not drawing walls when player is closer to **TOP** side of array~~
16.	~~***HA:***	Walls not drawing in correct position of window~~
17. ~~***MAK:*** Walls not drawing in correct distance, it is drawing as inversed distance.~~
18.	~~***MAK:*** Check if bugs are present when have 1920 rays for walls.~~
19.	~~***MAK:*** Parse spaces for the map.~~
20. ~~***MAK && HA:***Fish Eye fixed.~~
21. ~~***MAK:*** Given directions of all the sides of the wall in the game with direction.c, function named wall_hit_direction.~~
22. ~~***MAK && HA:*** When the game starts the position of player is different than playing the game, even with the pause function- the player is somewhere else in the map not when in his latest position. Need to be fixed. Probably the init_rays function is not functioning it properly.~~
23.	~~***HA && MAK:***	Bug, NO, SO, EA, WE can be in any order, our parser fails it.~~
24.	~~***MAK && HA:***	Map should not contain any spaces within the map. Spaces in the middle of the map with 1's and 0's should be invalid? Need to confirm this.~~
25.	~~***HA:***	`add_xpm();` still not incrementing y in correct increments to draw walls~~
26. ~~***HA:***	Mouse not being released on hitting pause~~
27. ~~***HA:***	Minimap jumping and resetting when approaching 0 index on both x and y.~~
28. ~~***HA:***	Parsing for newlines etc; between map lines not working.~~
29.	~~***HA:***	Parsing of 0 on right side of map not function for borders~~
30.	~~***MAK:*** Player jumps into wall when increase speed by hitting left shift.~~
31.	~~***HA:***	Double free in `store_data();`~~

`#TODO:`

1.	~~***HA:***	Incorprate `get_next_line();` in `ft_reading();`~~
2.	~~***HA:***	Refactor `isdir();` and double check project for forbidden functions~~
3.	~~***HA:***	Parse and store map and config in separate 2D array for each~~
4.	~~***HA:***	Figure out how to separate map from configurations~~
5.	~~***HA:***	Add `make vg` rule in Makefile for debugging~~
6.	~~***HA:***	Debug segfault in `get_size();` due to~~
7.	~~***HA:***	Double check space stripping in squash~~
8.	~~***MAK:***	Declare a new structure to fetch the info and place it in the main root of the structure which will work on every aspect of the program.~~
9.	~~***HA:***	Study Raycasting~~
10.	~~***HA:***	Discuss images to be used with **`MA`**~~
11.	~~***HA:***	Figure out correct drawing and following of mouse cursor~~
12.	~~***MAK:***	Take xpm files and read it to check if the file reading is working perfectly or not.~~
13.	~~***MAK:***	Time for raycasting math to solve.~~
14.	~~***HA:***	Draw interior of minimap~~
15.	~~***HA:***	Figure out hook management for hook_num 46, see comments in `utils_hooks.c`~~
16.	~~***HA:***	Figure out what is the event that detects clicking on window edges~~
17.	~~***HA:***	Figure out XPM image for pause in center of screen and implement removal~~
18.	~~***HA:***	Correctly implement # 14~~
19.	~~***HA:***	Fix minimap drawing to draw when player is closer to left side of array coords, possibly due coords calculation making coords negative and invalid read~~
20.	~~***HA:***	Fix walls drawing in wrong position of image, perhaps because ra->y not correct value. X is also not increment in correct amount.~~
21.	~~***HA && MAK:***	Figure out solution to fish-eye effect.~~
22. ~~***MAK:*** Implement edge cases for the rays.~~
23. ~~***MAK:*** Need to work on fixing the directions of the rays when hits the wall.~~
24. ~~***MAK:*** Raycasting is optimised with DDA Algorithm~~
27. ~~***MAK:*** Animation effect when the AK-47 is triggered.~~
25.	~~***HA:***	Figure out y step increments~~
26. ~~***MAK:*** Work on sprites when rays will hit.~~
28. ~~***MAK:*** Work on the management of sprites.~~
29. ~~***MAK:*** Have character types for different types of sprites like D for Door, F for fire, B for barrel, etc.~~
30. ~~***HA:*** Refactor minimap drawing in `utils_minimap.c` see `mini_interior();` on branch hawadh-minimap.~~
31.	~~***MAK:*** Finished working on the parsing for doors.~~
32. ~~***MAK:*** Allocate structure for the doors and put xpm addresses in the sprites structures when the wall hits.~~
33. ~~***MAK:*** Working on Integration for the doors.~~
34. ~~***HA:*** Minimap not drawing EA/WE facing doors correctly. Need to adjust drawing depending on walls surrounding.~~
35.	~~***HA:***	Resize minimap dimensions and values. Reduce them by half `MINI_DIM 90`.~~
36.	~~***HA:***	Fix map file parsing, map does not fail if newlines or any whitespace between map lines.~~
37.	~~***MAK:***	Add rotation to minimap player model.~~
38. ~~***MAK:***	Minimap Door Integration.~~
39. ~~***MAK:***	Norm fix for some files.~~
40. ~~***HA:***	Norm fix for `mini_map.c` function `mini_interior();`~~
41. ~~***HA:***	Parse for any lines before first element in file.~~

`#CURRENT STATUS`

`HA:	25 Nov 2022`

1.	New files to split functions `parse_file.c`, `errors.c`, `parse_file.c`
2.	Added .gitignore
3.	Created new Function `err_return();` to exit status 1 with correct error message
4.	Added get_next_line(); and minilibx_opengl
5.	Added debugger files to run debugger
6.	Refactored function `ft_reading();` and, now static `init();`
7.	New functions `get_size();` to get number of lines in file in `utils_parse.c`
8.	New struct pointer in `t_info` called `t_data`
9.	New function static `extract_data();` to extract data from file and store in a 2D array
10.	Added my `libft` function `ft_strchr();` to cub3d libft
11.	Added new function `ft_ptrptrlen();` to our libft returns 2D array size
12.	Added new function `ft_isspace();` to our libft, if ascii whitespace return `TRUE`
13.	New function `clean_file();` in new file `utils_file.c` to clean file input
14.	Helper functions for above `squash();` and `count_str_size();`. Squash removes all excess whitespaces in line and `count_str_size();` returns correct str size without excess white spaces
15.	New function called `free_split();` to free 2D arrays in new file `memory_mngmnt.c`
16.	Parsing Configurations almost complete, see `TODO #4`
17.	Moved function `get_act_size();` to file `utils_parse.c`
18.	New file `utils_file_ext.c` with functions `**squash_lines();` and, new function, `check_line(); to only clean file up to last line not including map to be left for parsing.
19.	Cleaning file complete.
20.	`make vg` rule added, see Makefile
21.	Leak found and fixed in `clean_whitespaces();` was missing a pointer
22.	Added new function to libft: `ft_strrmc();` removes `char c` from array
23.	Uncomment of MLX related lines in Makefile, MLX now functional in Program
24.	`mlx_loop();` now called in function `init();`
25.	Window now initialised and opening, by adding function calls `mlx_new_window();` in `main.c` function `init();`
26.	Two new files, `window.c` for window functions and `utils_hooks.c` for key hook utilities
27.	Calling `mlx_key_hook();` int `init();` that calls new function `key_hook_manage();` which currently only handles **ESC**
28. New function `esc_win();` which calls `free_data();` and `exit(0);`, this function handles both `(x) and esc`
29.	Calling `mlx_hook();` in `init();` to handle above `(x)`
30.	Two new functions in `window.c` to initialise and store window + image address, `init_window();` and `get_img_addr();`
31.	New file `draw.c` contains 2 new functions `draw_cursor();` and `my_pixel_put();`
32.	Function draw cursor calls `MLX` function `mlx_mouse_get_pos();` to get mouse position for cursor drawing ***WIP***
33.	Updated `memory_mngmnt.c` with 3 new `free_struct_???();` functions one for each struct and struct members
34.	Added error message `ERROR: Minilibx Failure` for any failure from minilibx functions
35.	Added print loop in `check_map();` to print file contents after cleaning and parsing
36.	Refactored `draw_cursor();` and new function `init_mouse();` in new file `mouse.c`
37.	New file `hooks.c` to contain new function `hook_management();` to hold all `mlx_hook();` calls
38.	Refactored `draw_cursor();` and new function `mouse_move();` calls `init_cursor();` from within `hook_management();`
39.	Moved `mlx_loop();` to `window.c` called in function `init_window();`
40.	Refactored `init_cursor();` now draws half cursor in centre of screen
41.	New file `rgb.c` with new function `rgb();` to calculate colours for roof and ceiling.
42. Three new functions in new file `utils_draw.c` to draw roof and ceiling colours `draw_ceiling();` and `draw_floor();` called from function `ceiling_floor();`
43.	New function `draw_map();` called in `init_window();` in `draw.c` to draw currently contains `ceiling_floor();`  -> to draw ceiling and floor, and `init_cursor();` -> to redraw cursor
44.	New file `mini_map.c` contains 3 functions to draw minimap border and interior see TODO #14, functions named `draw_minimap(); mini_bottom_top(); mini_interior();`
45.	Minimap drawn in top left corner, Missing interior
46.	Downloaded some xpm images and added window control flags to MLX library
47.	Removed fullscreen flag from `mlx_new_window.m` flag is `NSWindowStyleMaskFullScreen;`
48.	Buttom `m` on keyboard stops mouse capture and releases mouse
49.	Added `mlx_string_put();` function from old `MLX` to current `MLX` library, and updated `mlx.h`
50.	New function `check_tabs();` called in `squash_lines();` replaces all tabs to 4 spaces within the `map` only in file `utils_file_ext.c`
51.	New function to mimic `ft_strlen();` but adds +4 to the count for each tab found
52.	Bug #6 Fixed, was due invalid write due to incorrect calculation in `get_tab_size();`
53.	Added `xpm_images/` file with sample xpm images to discuss
54.	New Function `init_xpm();` to init and store all xpm images placed in `window.c`
55.	New function in `parse_layout.c` called `store_map();` & `**map` of `data->file`
56.	New function `confg_count();` to count number of lines for `data->confg` & `data->map` in `parse_layout();`
57.	Added Loading and implementation fo Pause Message on hitting `'m' hook number 64` in `key_hook_manage();`, yet to implement removal of Pause Message
58.	Fixed leak in `store_map();` line 47, due starting iteration at `i = -1;` solution was to increment `i` before check `data->file[i]` in `while (++i < len && data->file[i])`
59.	Deleted unnecessary file `utils_parse_ext.c`
60.	Moved function call `parse_arg();` to function `check_map();` as clean-up of `main.c`
61.	Added error message `status == 5` in `errors.c` for XPM Image loading failure
62.	Added parameter `t_info *info` to function prototype `void err_return(int status, t_info *info);` and sending in `t_info *info` to all occuring function calls to free any allocated data within the structure in case of any error returns before exit
63.	New function `store_confg_map();` which stores the map and the confg in their respective 2D Arrays
64.	New File `utils_xpm.c` to hold all xpm related functions
65.	Renamed `xpm_images/` to `imgs/`
66.	New Function `init_minimap();` called in `init_window();` inits memory for `t_mini` structure to be used for initialising a new image for minimap and calling `mlx_get_data_addr();` to place image in main window for faster redrawing of minimap
67.	Due to above, `draw_minimap();` completely refactored now only 1 function called within `mini_interior();` to draw interior
68.	New Custom `pixel_put();` function for mini map called `mini_pixel_put();` uses `t_mini *mini` as struct pointer
69.	Added new error message and status to `err_return();`, and removed print of `d->confg` from `check_map();`
70.	New function prints layout content in `parse_layout();` called `print_xpm();`
71.	Refactored `check_tabs();` and `squash_lines();` to reduce number of lines and fix extra removal of character from `check_tabs();`, `squash_lines();` now has 2 additional `else if` statements
72.	Changed position of `PAUSE` image in window within function `key_hook_manage();` line `#44`
73.	New file `utils_xpm.c` with function `opem_xpm();` uses `mlx_xpm_file_to_image();` to open all xpm images and store in `data->confg` called in `init_xpm();`
74.	Added `&& i < len` line `#39` in `open_xpm();` to fix `bug #9`
75.	Added new function  `free_struct_mini();` in `memory_mngmnt.c` to free struct `t_mini` and it's contents
76.	New File `utils_mini_map.c`
77.	New Struct `s_player` to save all player related data, also new function, `draw_player_walls();` to extract player position and future drawing of minimap in `mini_interior();` with 2 functions `find_player_array();` for Y and `find_player_index();` for X while also extracting Perspective
78.	Bug fix `#11`
79.	New function added to `libft` `ft_ismapicon();` to detect if character in string is a valid map character, now called in `check_if_map();`
80.	New Approved map walls xpm images
81.	Implemented Colour bit Masking, and renamed file `utils_mini_map.c` into `player.c` and renamed function `draw_walls_player();` to `init_player`
82.	New function in `window.c` called `init_all();`, calls all `init?????();` functions before drawing and pushing to window`
83.	Refactored `open_xpm();` and new function `get_xpm_addr();` to extract addresses of each xpm file for later use in merging with main image
84.	Added `# define WIDTH 1920` and `# define HEIGHT 1080` in `cub.h`
85.	New Struct `s_xpm` in array to contain all image data, with new Enum to contain `NO`, `SO`, `WE`, `EA`
86.	Added free for `data->xpm` struct in `memory_mngmnt.c` and moved `free_split();` to new `utils_memory_mngmnt.c`
87.	Two new Functions in `draw.c` called `place_xpm();` and `add_xpm();`; Function `place_xpm();` to determine initial player orientation, and `add_xpm();` draws the image to main image address
88.	New Pause button `'p' == hook_num 35`
89.	Implemented correct method of adding xpm address to img
90.	Added `mlx_clear_window();` for pause removal. See bug #13
91.	New Variable `xpm->divisible` to determine size of walls
92.	New function to hold Pause code `handle_pause();` located in `utils_hooks.c`
93.	Refactored `add_xpm();` with correct iteration of image `char *`, still not drawing correctly
94.	Started mini map drawing, see `mini_map.c` and file `utils_mini_math.c` renamed to `utils_minimap.c`
95.	New XPM image implemented `Ak47.xpm` for weapon, and new images for `NO SO WE EA`
96.	Buf #12 FIXED, now correctly implementing copying of image pixels with colours to main image window via `char *`, also added `wi - 4` && `hi - 4` to avoid invalid read within images
97.	Currently working on and implementing of drawing interior contents of minimap, with 2 new functions, `draw_mini_player();` which draws player in centre of minimap (Currently white square also drawn around to figure out scaling) and `draw_mini_walls();` to attempt to draw walls in respective positions in the minimap.
98.	Changed size of minimap image from `260x185` to `185x185` and moved function `mini_interior();` to `utils_minimap.c`
99.	Added new `# define MINI_SCALE 29` for minimap scaling and new variable `data->gun`
100. New Wall images Implemented
101. Attempting new algorithm in `mini_interior();` WIP
102. Removed `TRUE FALSE` from `cub.h` since it already exists in `libft.h`
103. Minimap fully functional, refactored `mini_intrior();` and 2 new functions `draw_mini_enemy();` and temporary function `draw_square();` for scaling testing confirmation
104. Moved function `draw_mini_player();` and `draw_square();`
105. Added acceptable character in `valid_key();` in `parse_map.c` character `'m'` for enemies, `line #32 -> #33`
106. Refactored scaling and sizes of mini-map drawing to fit player and map exact centre in minimap
107. Swapped `EA` and `NO` walls images
108. New function `find_player();` in `player.c` to find player position in map array, Function is `NOT STATIC` so it can be recalled with each iteration to redraw mini-map, added function call in `draw.c draw_map();`
109. WIP free xpm struct array in `memory_mngmnt.c` and new test map `zmap.cub`
110. Refactored `place_walls()` in `draw.c` now takes angle and draws wall texture accordingly.
111. Added `if (x == 0){ x = ray.x; }` in `moves.c` line `#244` and added place walls call line `#251` along with `x = 0 line `#255`
112. Added correct values for `ra->ang` comparison with `int * RADIAN` with two separate conditions for east
113. Made short loop for `while (x < ray.x1 (ray.x1 == 0 && x == 0))` with a call `place_walls();` and made `ray.x1 += 16.1` increments
114. Walls now drawing in correct width and height, but see bug `#17`
115. Removed Variable xpm->divisible as is no longer needed.
116. Refactored line `#208` in `moves.c` for height calculation.
117. New function called  `linux_osx_mouse();` lines `#88` && `#95` in `mouse.c`
function placed in `linux_osx_mouse.c`
118. Line `#37` in `draw.c` to now make `y = (HEIGHT / 2) - (ray>height / 2);`
119. Implemented `ifeq` and `else` in `Makefile` to determine OSX or Linux lines `#40` -> `#50'.
120. New file `linux_osx_mouse.c` calls mouse functions depending on OSX or Linux.
121. Changed all values within `ray.c` to `RAYS` as defined to ease change.
122. Attempting new method of calculating `x` and `y` positions in XPM file and `xpm_y` iteration in `draw.c` `add_xpm();`
123. Removed unused variables in `init_rays();` and `wall_ht_direction();`
124. Added `#ifdef OSX`, `#ifdef LINUX` in `cub.h` to ease transition between `OSX` and `Linux`.
125. New function in `utils_math.c` called `euclidean();` called in `rays.c` line `#79` to calculate real distance from player view plane
126. Added `free(info->mlx);` in `memory_mngment.c` lines `#100 -> #104`
127. `xpm_x = ray->y * xpm->wi` to extract x coordinate on texture, still need step incrementation for y
128. Adjust conditions for `while` loop in `draw.c` current lines `#40` and `#43` and changed `y` value calculation to `y = (HEIGHT - ray->height) / 2;` to get correct wall height drawing.
129. Implemented `if (ray->dir_wall == 1 || ray->dir_wall == 2) { xpm_x = ray->x * xpm->wi; }` in `draw.c` current lines `#38 -> #39`
130. Fixed issue with mouse not being released on hitting pause, by implementing `int status` in function parameter `linux_osx_mouse(t_info *info, int x, int y, int status)` to only trigger mouse move when pause flag is triggered.
131. Muazzam gave calculation `step = ((xpm->hi * xpm->wi) / ray->dist) / ray->height;` implemented in `draw.c` in current line `#46`, step was placed in `xpm->addr[]`
132. Branched from main to `hawadh-minimap` branch & refactoring minimap drawing algorithm.
133. Implemented `# define NUM_SPRITES` in `cub.h` to auto increase allocation for `t_xpm *xpm` to add any new sprites to structures.
134. Check comments for `utils_math.c` `utils_minimap.c` `utils_xpm.c`
135. New file `utils_minimap_ext.c` with two new functions `x_y_values();` & `mini_img_limit();` called in `utils_minimap.c` in function `mini_interior();`
136. New Function `x_y_values();` returns values of either `x` or `y` depending on whether index values are negative. Returns the values with calculation of scale for offset in minimap.
137. New Function `mini_img_limit();` checks if `y` or `x` value has reached the loop limit to decide to continue or exit.
138. New function `assign_index_values();` placed in file `utils_minimap_ext.c` returns index value depending if index calculated via input parameter and returns necessary value.
139. Renamed `door1.xpm` to `door.xpm` and resized all wall images to 1920x1080.
140. Adjust player drawing size in `mini_map.c` to draw smaller player.
141. New `#define MINI_DIM` variable for minimap dimensions in `cub.h` and replaced all values in mini map functions that determined map dimensions.
142. New function in `utils_minimap.c` draw_mini_interior()` to determine which map icon was detected to draw.
143. New `#define NUM_SPRITES` in `cub.h` to adjust memory allocation for `t_xpm*` when necessary as number of sprites increment.
144. New function in `utils_minimap.c` called `draw_mini_doors();` WIP (NEEDS NORMINETTING) to draw doors on minimap.
145. Removed `p_ang` from `get_height();` parameters in `utils_math.c` and all `get_height();` function calls input.
146. Added call `err_return();` with error `status == 3` in file `utils_door.c` to call error for invalid doors location.
147. Finalised drawing of walls in minimap with two new functions `draw_mini_doors_horizontal();` and `draw_mini_doors_vertical();` separated due to different `x_one` and `y_one` values required. Functions placed in `utils_minimap_ext.c`
148. Added `MINI_DIM` variables in all `draw_mini_player();` values to make change of minimap size more streamlined in file `mini_map.c`.
149. Renamed function `draw_mini_enemy();` in `utils_minimap.c` to `draw_mini_sprite();`
150. Refactored `x_y_values();` in `utils_minimap_ext.c` to calculate correct `x` & `y` values.
151. Moved `squash_lines();` to `parse_file.c` & now sending `t_info *info` to `store_data();` in `utils_file.c`
152. New function in `parse_layout.c` called `hceck_map_config_lines();` called from `check_map_lines();` in `utils_file_ext.c`
153. Fixed parsing issue with any new lines or empty spaces between map lines. See `#151` -> `#152`.
154. Removed unused function in `directions.c` called `print_map(char **str);`.
155. Refactored `rgb_door_status();` in `utils_minimap_ext.c` now calls `get_door();` from `hooks.c` to check if door status in `t_doors*` structure array.
156. Removed function `rgb_door_status();` and no longer checking door status.
157. Fixed double free() in `store_data();` in `utils_file.c` was attempting to free 2D array when only the main array was allocated.
158. Fixed norm issues in `check_config_map();` in file `utils_file_ext.c` now calls function `check_config_lines()` placed in new file `utils_line_check.c`.
159. Removed `utils_sprite.c` completely & removed `key_sprite();`.
160. Moved function `valid_key();` from `parse_map.c` to `utils_parse.c`.
161. New function `free_more();` placed in `utils_memory_mngmnt.c` called in `free_data();` to reduce number of lines.
162. Moved `free_gun();` to `utils_memory_mngmnt.c` && removed function name `working_sprite();` from `cub.h` as not used anywhere.
163. Removed function `draw_mini_sprites();` as it is not in use from `utils_minimap.c`.
164. Added empty line check in `utils_file_ext.c` in two functions `check_map_lines();` && `check_config_map();` to detect any non-empty lines between elements that contain only whitespaces other than a newline.
165. Fixed norm issue in `minimap.c` in function `mini_interior();` by creating new function to call `x_y_values();` and `extract_decimal()` for `x` and `y` values, function is called `get_values();` placed in `utils_minimap.c`.
166. Added 20 more to `ang_iter` in `mini_rot()` in file `mini_map_rot.c` to make view cone longer in minimap, and changed colour value from `0x00FF0000` to `0x00A0F0F0`.
167. Added `*map_icon == 'O'` to `draw_mini_interior();` in `utils_minimap.c` and changed input for `draw_mini_doors_*(t_info *info, int x, int y, >>char *map_icon<<);` to send `*map_icon` to draw correct door colour.
168. Refactored `check_open();` in `utils_minimap_ext.c` to take `char *map_icon` as parameter from `draw_mini_interior();`. Function now return green only if `*map_icon == 'O'` else it returns red. Function `check_open();` is called in `draw_mini_doors_*();` in the position of `rgb` of `mini_pixel_put();`
169. Added check in `squash_line();` `if (i == 0 && check_line())` to clean and return error if any lines before config at the begining of the file as it is invalid.
170. Added `t_info *info` parameter to `squash_lines();` to call `err_return();` for cleanup before exit.
171. Added comments to some functions in `doors.c` && `draw.c` && `utils_xpm.c` && `parse_layout.c`.
172. Added bool condition in `if`, `if else` && `else` statements in function `xpm_store();` in file `config_xpm.c` to check if data already exists in case of duplicates to fix memory leak.
172. Fix for `xpm_store();` now compares with empty string.
173. Refactored `data_init();` to now loop through `data->confg` 2D array to set each element as `NULL` to avoid future invalid reads and leaks and changed back to bool condition for `HA:#172`.
174. Added ASCII art and credits to `Makefile`.
175. Added comments to functions in `angle.c` && `memory_mngmnt.c` && `utils_memory_mngnmnt.c`.

`MAK:	4 July 2022`

1.	Parsing for different types of layout is finished. Memory leaks, and norms are done.
2.	For better reference please read the comments to know what is the structure for parser.
3.	Changed char to const char in ft_strcmp.
4.	Updated crosshair with green line and minimal size of the crosshair.
5.	Updated parsing function to fetch the values based on the requirements like path to different xpm files, colours given based on RGB combination for floor and ceilings.
6.	Updated Crosshair
7.	Rotations are done.
8.	Movements of the player are functioning perfectly.
9.	Given the field of view as 70 degree and number of rays are 1920.
10.	With the Help of shooting rays, we have the height formula given the distance of the rays when hits the wall.
11.	Iteration of each ray in X-coordinate is 1 and the angle iteration is 0.000636318 in radian.
12.	The project is functioning perfectly in MAC and Linux OS.
13. Created New Basic Movements which can have the basic functions of the player- movements and rotation.
14.	Created New File rays.c which can initialise rays and work on the calculations.
15.	Created New file edge-cases.c which can hold the account of the scenario if the free path is in the middle of the walls.
16. Created a new structure t_str which can help us in the iteration of the parsing of the map. 
17. Created New file parse_spaces.The function will help us to check if there is a space at any index of the map, then there should be either the wall or the space else it will throw an error.
18.	Created New file utils_math.c to store the function sq and dist.
19.	Created New file utils_str.c since the function ptrptrlen and strlen returns the values in size_t, we needed the same function but to return as an int to avoid memory leaks in parsing. So the names are get_2d_len, ft_strlen_int.
20. Finished working on Fish eye effect.
21. Finished working on the edge cases.
22. Created a new function get_height which does the formula and revise it if it exceeds the window.
23. Created a new file directions.c and added a function named wall_hit_direction which gives the direction of all the sides of the wall.
24. Edited some codes in draw.c which can link it with the wall_hit_direction to give a better clarity to the game.
25. Created a new Function Euclidean which handles the functions for right angle triangle for different rays.
26. Parsing for different orders of the layout is completed.
27. Created a new file named utils_type and inside created new functions which are linked in this way- NO 1, SO 2, WE 3, EA 4, C 5, F 6, with any type of input I get the value as string or an int.
28. Created a new Folder named Raycasting Algorithm which contains a text document. For to post it on how the collaboration was as a team and what we have developed in cub3D.
29. Created new files sprite.c, utils_sprite.c. Working on the management of sprites- parsing in rays, allocation for structure of sprites and more.
30.	Created an animation effect for AK-47.
31. Finished Parsing for the doors.
32. Finished allocations for the sprites.
33. Parsing for Duplicates and rgb with commas are done.
34. Got the door integration for the map.
35. Added a new function for freeing the configuration data. Using if statements for each and every index of the 2d array if the memory exists and freeing it if it exists.The function is called from free_struct_data -> free_config(data->cong)
36. Moved #35 to utils_memory_management.
