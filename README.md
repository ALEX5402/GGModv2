#GGMod
Provide GameGuardian MOD tutorials and codes, such as luajava library, repair os.execute function, improve String library, add Canvas, etc.
Compared with providing java source code, providing packaged dex or smali allows most people to use it directly, even if he does not know any language, he can get what he needs according to the tutorial. If you want to learn Java source code, then dex and smali won't bother you, right? ?
2021.10.01 will be updated from time to time

# Mobile tools
<p>MT file manager.apk</p>
<p>AIDE.apk</p>
<p>GameGuardian.apk</p>

# language
Mainly involved in the following languages
<p>Lua</p>
<p>LuaJ</p>
<p>LuaJava</p>
<p>Java</p>

# template
<p>Because luajava cannot provide convenient String class interaction, we need to encapsulate some methods in the String class and add them to the string library in the _G global table</p>
<p>The StringLib.java class is a template for the writing method of the original String library of Luaj (not the source code of the StringLib packaged by me). Refer to this writing method to effectively learn the method of function encapsulation</p>
<p>https://github.com/JealousCat/GGMod/blob/main/Function/StringLib.java</p>

# beautification tutorial
Note: Refers to making changes to non-function library functions or UI interfaces, etc., to make the modifier experience better and the interface more beautiful

<p><a href="https://alywp.net/35mDO4">1. Changing the name of the installation package can also remove random installation</a></p>
<p><a href="https://alywp.net/5bzBxRoW">Second, replace the modifier icon</a></p>
<p><a href="https://alywp.net/VYt9B">3. Change two desktop icons into one</a></p>
<p><a href="https://alywp.net/2i2gJg">4. Reduce the size of the installation package through the arsc file</a></p>
<p><a href="https://alywp.net/3olKpw">5. Reduce the size of the installation package through the res file</a></p>
<p><a href="https://alywp.net/46L2QB">6. Reduce the size of the installation package through the dex file</a></p>
<p><a href="https://alywp.net/3FI6PT">7. Remove the words "Script has ended:" at the end of script execution to facilitate copying the end content</a></p>
<p><a href="https://alywp.net/3mSuk5">8. UI icon beautification</a></p>
<p><a href="https://alywp.net/6XmSy4">9. Set the color stroke transparent background pop-up window</a></p>
<a href="https://github.com/JealousCat/GGMod/blob/main/beautify/Alert.smali">Alert.smali download in the pop-up window beautification tutorial</a>
<p><a href="https://alywp.net/2EKe3V">10. Remove the explanatory text of the search list and save list</a></p>
<p><a href="https://alywp.net/4BjGoS">11. Status bar</a></p>
<p>const/4 v4, 0x1</p>
<p>invoke-virtual {p0, v4}, Landroid/ext/BaseActivity;->requestWindowFeature(I)Z</p>
<p><a href="https://alywp.net/4i8iUT">Twelve. Delete unused buttons on the homepage without error, beautify the button UI, and set the background image of the homepage</a></p>
<p><a href="https://alywp.net/2TLeyq">Thirteen, remove the link display on the pop-up window and other interfaces</a></p>
<p><a href="https://alywp.net/1m2Fj9">Fourteen, set transparent button</a></p>
<p>const v1, 0x0</p>
<p></p>
<p>invoke-virtual {p0, v1}, Landroid/fix/Button;->setBackgroundColor(I)V</p>




# Function Add Tutorial
Note: refers to adding the compiled function file to the function library of the GG modifier
<p><a href="https://github.com/JealousCat/GGMod/blob/main/LuaJava/Luajava.dex">luajava.dex file download</a></p>
(2022.1.17 Note: The function library of luajava has been updated, see the readme of Luajava)
The LuaJava library replaces the original official Loadlib with LoadDex, and adds luajava.astable, luajava.toArray, and luajava.methods. The specific usage is reflected in the follow-up tutorial, or use jadx to view the java code
<p><a href="https://alywp.net/2KzA5a">1. Add luajava library for interaction between lua and java, and java methods</a></p>
<p><a href="https://alywp.net/7I7PeA">Second, add the String library and improve on the original basis</a></p>
<p><a href="https://alywp.net/3uFJjb">3. Add a single new function to the string and math libraries</a></p>
Two new functions have been added, and their added tutorials can be used as the above tutorial
<p><a href="https://github.com/JealousCat/GGMod/blob/main/Function/StringLib%24similarity.dex">string.similarity</a></p>
<p><a href="https://github.com/JealousCat/GGMod/blob/main/Function/MathLib%24gcd.dex">math.gcd greatest common divisor calculation</a></p>
<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/ToolsLib.dex">4. ToolsLib.dex, a tool function library born out of GG native class</a>< /p>
Organize the methods in all the original classes of GG, and encapsulate the static methods that can be directly accessed and have certain use value in the script in ToolsLib
<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/ToolsLib.dex"></a>As a newly compiled extension library, ToolsLib.dex can be like StringLib, etc. The library is instantiated in the Script class and loaded into the global environment, or you can use luajava.loadDex for non-merged local loading</p>
<p>tools.removeNewLinesChars, tools.getCacheDir, tools.getHiddenDir, tools.getRamSizeKb, tools.isRootMode, tools.tryRoot, tools.toString64, tools.getLogcatFilename, tools.openAppInfo, tools.chmod, tools.executeScript, tools.isScreenOn , tools.getCacheDirHidden, tools.isPackageInsta, tools.alertBigText, tools.getNativePath, tools.exec, tools.prefixLongHex, tools.getFilesDir, tools.sendRestartIntent, tools.dump, tools.compare, tools.getStubLib, tools.hash, tools .crc32, tools.isLandscape, tools.ToHexString, tools.getScreenSize, tools.isX86, tools.trimDirPath, tools.doubleToTime, tools.allowExecute, tools.getSdcardPath, tools.prefix, tools.formatFileSize, tools.dp2px, tools.copyFile , tools.restartApp, tools.longToTime, tools.getDaemonDir, tools.getDaemonPath, tools.getFilesDirHidden, tools.parseTime, tools.getFreeMem, tools.getDataDirSafe</p>
Have the opportunity to elaborate on the usage of each function

<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/SmaliManager.dex">5. dex to samli</a></p>
<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/res.dex">Decompile arsc, xml</a></p>
<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/apksigner.dex">Six, apk signature</a></p>
<p>You can access them with the luajava library</p>
<p><a href="https://alywp.net/1PsYLn">7. CoroutineLib coroutine addition</a></p>
<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/LogPrint.dex">8. Added LogPrint, which can view the printed content in real time, which is different from print which needs the script to end look. See LogPrint.lua for usage method</a></p>
<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/RSASecurity.smali">9. RSA encryption and decryption, three methods in the class: decrypt, encrypt, generateKeyPair</ a></p>
<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/RootUtil.smali">10. Root management class, including execRootCmd, execRootCmdSilent, haveRoot</a>< /p>
<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/ScreenMetrics.smali">11. Screen parameter class, initialize the Activity through initIfNeeded to get some parameters, click the link for details View source code</a></p>
<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/ZipUtil.smali">12. Zip management class, including compression method zip, decompression method unzip, data stream copy copy method, append method to add content to the compressed package</a></p>

<p><a href="https://github.com/JealousCat/GGMod/blob/main/dex/TableLib.dex">Thirteen, add table.equals to compare whether the contents of two tables are equal; table The .allPerm array is fully arranged. Need to merge with classes.dex, tutorial reference Mat


