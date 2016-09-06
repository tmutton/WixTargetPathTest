# WixTargetPathTest

<Directory Id="TARGETDIR" Name="SourceDir">
	<Directory Id="ProgramFilesFolder">
		<Directory Id="INSTALLFOLDER" Name="WixTest.Installer" />
	</Directory>
</Directory>

By default the target directory will be set to the root (usually C). It will then target the program files folder.

To change that we can install the msi via the command line like so: msiexec /i myMsi.msi INSTALLFOLDER="C:\myCustomInstallFolder"

This will install our msi into a folder on the root drive called myCustomInstallFolder (it will create the directory if it doesn't exist).
