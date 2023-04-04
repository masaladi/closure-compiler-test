"D:\Program Files\Java\jdk-17.0.6\bin\java.exe" -Dmaven.multiModuleProjectDirectory=D:\workspaceEG\closure-compiler-test "-Dmaven.home=D:\Program Files\JetBrains\IntelliJ IDEA 2021.2.2\plugins\maven\lib\maven3" "-Dclassworlds.conf=D:\Program Files\JetBrains\IntelliJ IDEA 2021.2.2\plugins\maven\lib\maven3\bin\m2.conf" "-Dmaven.ext.class.path=D:\Program Files\JetBrains\IntelliJ IDEA 2021.2.2\plugins\maven\lib\maven-event-listener.jar" "-javaagent:D:\Program Files\JetBrains\IntelliJ IDEA 2021.2.2\lib\idea_rt.jar=53433:D:\Program Files\JetBrains\IntelliJ IDEA 2021.2.2\bin" -Dfile.encoding=UTF-8 -classpath "D:\Program Files\JetBrains\IntelliJ IDEA 2021.2.2\plugins\maven\lib\maven3\boot\plexus-classworlds-2.6.0.jar;D:\Program Files\JetBrains\IntelliJ IDEA 2021.2.2\plugins\maven\lib\maven3\boot\plexus-classworlds.license" org.codehaus.classworlds.Launcher -Didea.version=2021.2.2 package
[INFO] Scanning for projects...
[INFO] 
[INFO] -----------------< com.example:closure-compiler-test >------------------
[INFO] Building closure-compiler-test 0.0.1-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- closure-compiler-maven-plugin:2.21.0:minify (dynamic-imports-test) @ closure-compiler-test ---
[INFO] Starting JavaScript task:
[INFO] Skipping the merge step...
[INFO] Creating the minified file [main.js].
4月 04, 2023 5:08:58 下午 com.google.javascript.jscomp.LoggerErrorManager println
严重: js/lib/test/main.js:1:0: ERROR - [JSC_JS_MODULE_LOAD_WARNING] Failed to load module "./utils.js"
  1| import { enableAwesomeFeature } from "./utils.js";
     ^

4月 04, 2023 5:08:58 下午 com.google.javascript.jscomp.LoggerErrorManager printSummary
警告: 1 error(s), 0 warning(s)
[ERROR] D:\workspaceEG\closure-compiler-test\src\main\resources\public\js\lib\test\main.js [1:0]: ERROR - Failed to load module "./utils.js"

[ERROR] Failed to process the source files [main.js, utils.js].
com.github.blutorange.maven.plugin.closurecompiler.common.FileException
    at com.github.blutorange.maven.plugin.closurecompiler.plugin.ProcessJSFilesTask.checkForErrors (ProcessJSFilesTask.java:195)
    at com.github.blutorange.maven.plugin.closurecompiler.plugin.ProcessJSFilesTask.minify (ProcessJSFilesTask.java:139)
    at com.github.blutorange.maven.plugin.closurecompiler.plugin.ProcessJSFilesTask.minify (ProcessJSFilesTask.java:84)
    at com.github.blutorange.maven.plugin.closurecompiler.plugin.ProcessFilesTask.processFiles (ProcessFilesTask.java:204)
    at com.github.blutorange.maven.plugin.closurecompiler.plugin.ProcessFilesTask.call (ProcessFilesTask.java:151)
    at com.github.blutorange.maven.plugin.closurecompiler.plugin.MinifyMojo.execute (MinifyMojo.java:866)
    at org.apache.maven.plugin.DefaultBuildPluginManager.executeMojo (DefaultBuildPluginManager.java:137)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:210)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:156)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:148)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:117)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:81)
    at org.apache.maven.lifecycle.internal.builder.singlethreaded.SingleThreadedBuilder.build (SingleThreadedBuilder.java:56)
    at org.apache.maven.lifecycle.internal.LifecycleStarter.execute (LifecycleStarter.java:128)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:305)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:192)
    at org.apache.maven.DefaultMaven.execute (DefaultMaven.java:105)
    at org.apache.maven.cli.MavenCli.execute (MavenCli.java:957)
    at org.apache.maven.cli.MavenCli.doMain (MavenCli.java:289)
    at org.apache.maven.cli.MavenCli.main (MavenCli.java:193)
    at jdk.internal.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at jdk.internal.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:77)
    at jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:568)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced (Launcher.java:282)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launch (Launcher.java:225)
    at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode (Launcher.java:406)
    at org.codehaus.plexus.classworlds.launcher.Launcher.main (Launcher.java:347)
    at org.codehaus.classworlds.Launcher.main (Launcher.java:47)
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  1.488 s
[INFO] Finished at: 2023-04-04T17:08:58+08:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal com.github.blutorange:closure-compiler-maven-plugin:2.21.0:minify (dynamic-imports-test) on project closure-compiler-test: Closure compilation failure: FileException -> [Help 1]
[ERROR] 
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR] 
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoExecutionException

Process finished with exit code 1
