# TODO - ESC font size: support 3 levels

## Step 1: Implement plan for 3-level font size (default + small + large)
- Update `lib/src/enum_tool.dart` ✅
  - Change `EscFontSize` from `default_, size1..size7` to `default_, small, large` ✅
  - Update `EnumTool.getEscFontSize` mapping accordingly ✅


## Step 2: Keep ESC command API consistent
- Update `lib/src/esc_command.dart` docs/parameter references if needed

## Step 3: Fix iOS native mapping for new 3-level values ✅
- Update `ios/Classes/EscCommandPlugin.m` ✅
  - Map `size` (0/1/2) to `charcterSize` for small/large ✅
  - Remove/avoid reset after `addText` ✅



## Step 4: Fix Android native mapping for new 3-level values ✅
- Update `android/.../EscCommandPlugin.java` ✅
  - Ensure `size=1/2` maps to supported zoom multipliers ✅


## Step 5: Run basic checks ✅
- `flutter analyze` sudah dijalankan dan tidak ada error Dart terkait `EscFontSize` lagi ✅


