#
# Nutanix Community Edition Deployment Tool for vSphere
#
# Author:  Mike Cutsail (mike@cutsail.com)
#

#region XAML Definition


#  Defines the Window and Controls that make up the GUI
#  XML Nodes become objects that enable the getting and setting of I/O as well as handling input events

$xamlCode = @"
<Window xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:NutanixCEConfiguation"
        Title="Nutanix Community Edition Deployment Tool for vSphere" ResizeMode="NoResize" SizeToContent="WidthAndHeight" >

    <Grid>
        <Grid.RowDefinitions>
            <RowDefinition Height="30" />
            <RowDefinition Name="rowDef0" Height="190" />
            <RowDefinition Name="rowDef1" Height="0" />
            <RowDefinition Name="rowDef2" Height="0" />
            <RowDefinition Name="rowDef3" Height="0" />
            <RowDefinition Name="rowDef4" Height="0" />
            <RowDefinition Name="rowDef5" Height="0" />
            <RowDefinition Name="footer" Height="0" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="953"/>
        </Grid.ColumnDefinitions>
        <Grid Grid.Row="0">
            <TextBlock Name="infoPanel" HorizontalAlignment="Left" Margin="10,10,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="933" Text="Fill in the required fields to connect to vCenter" FontSize="14.667" Foreground="Blue"/>
        </Grid>
        <Grid Grid.Row="1">

            <TextBox Name="vcenterServerName" HorizontalAlignment="Left" Height="23" Margin="10,26,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="230" Grid.Row="1" Background="Pink"/>
            <TextBox Name="vcenterServerUsername" HorizontalAlignment="Left" Height="23" Margin="284,26,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="230" Grid.Row="1" Background="Pink" />
            <PasswordBox Name="vcenterServerPassword" HorizontalAlignment="Left" Margin="564,26,0,0" Grid.Row="1" VerticalAlignment="Top" Width="230" Height="23" Background="Pink"/>
            <Button Name="connectToVcenter" Content="Connect" HorizontalAlignment="Left" Margin="824,26,0,0" VerticalAlignment="Top" Width="121" Grid.Row="1" Height="22"/>
            <ComboBox Name="nodesToDeploy" HorizontalAlignment="Left" Margin="10,87,0,0" VerticalAlignment="Top" Width="94" Height="22" SelectedIndex="0" IsEnabled="False"/>
            <TextBox Name="vmNameBase" HorizontalAlignment="Left" Height="23" Margin="129,87,0,0" TextWrapping="Wrap" Text="NutanixCE" VerticalAlignment="Top" Width="153" IsEnabled="False"/>
            <Button Name="browseForCeImage" Content="Browse" HorizontalAlignment="Left" Margin="318,86,0,0" VerticalAlignment="Top" Width="68" Height="22" IsEnabled="False"/>
            <TextBox Name="pathToCeImage" HorizontalAlignment="Left" Height="23" Margin="391,86,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="552" IsReadOnly="True" />
            <TextBox Name="portGroupName" HorizontalAlignment="Left" Height="23" Margin="10,149,0,0" TextWrapping="Wrap" Text="NutanixCE" VerticalAlignment="Top" Width="141" IsEnabled="False"/>
            <CheckBox Name="trunkPortGroup" Content="Trunk" HorizontalAlignment="Left" Margin="164,153,0,0" Grid.Row="1" VerticalAlignment="Top" IsEnabled="False"/>
            <TextBox Name="vlanId" HorizontalAlignment="Left" Height="23" Margin="230,149,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="52" IsEnabled="False"/>
            <TextBox Name="numCpu" HorizontalAlignment="Left" Height="23" Margin="318,148,0,0" TextWrapping="Wrap" Text="4" VerticalAlignment="Top" Width="94" IsEnabled="False"/>
            <TextBox Name="ramGB" HorizontalAlignment="Left" Height="23" Margin="443,148,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="94" Text="16" IsEnabled="False"/>
            <Button Name="deployButton" Content="Deploy Nutanix Nodes" HorizontalAlignment="Left" Margin="577,128,0,0" VerticalAlignment="Top" Width="366" IsEnabled="False" Height="44"/>
            <TextBlock Name="textBlock" HorizontalAlignment="Left" Margin="10,65,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Height="22" Width="94"><Run Text="Nodes to deploy"/><LineBreak/><Run/></TextBlock>
            <TextBlock Name="textBlock1" HorizontalAlignment="Left" Margin="10,9,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="121" Text="vCenter / EXSi Server" Height="16"/>
            <TextBlock Name="textBlock29" HorizontalAlignment="Left" Margin="10,128,0,0" TextWrapping="Wrap" Text="vSwitch Port Group" VerticalAlignment="Top" Height="16" Width="150"/>
            <TextBlock Name="textBlock30" HorizontalAlignment="Left" Margin="391,65,0,0" TextWrapping="Wrap" Text="Path to Nutanix Community Edition Disk Image" VerticalAlignment="Top" Height="16" Width="264"/>
            <TextBlock Name="textBlock1_Copy" HorizontalAlignment="Left" Margin="284,9,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="103" Text="Username" Height="16" Grid.Row="1"/>
            <TextBlock Name="textBlock1_Copy1" HorizontalAlignment="Left" Margin="564,9,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="103" Text="Password" Height="16" Grid.Row="1"/>
            <TextBlock Name="textBlock5" HorizontalAlignment="Left" Margin="318,128,0,0" Grid.Row="1" TextWrapping="Wrap" Text="Number of vCPUs" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock11" HorizontalAlignment="Left" Margin="456,128,0,0" Grid.Row="1" TextWrapping="Wrap" Text="RAM (GB)" VerticalAlignment="Top" Width="69"/>
            <TextBlock Name="textBlock38" HorizontalAlignment="Left" Margin="129,65,0,0" TextWrapping="Wrap" Text="VM Name Base" VerticalAlignment="Top" Width="141"/>
            <TextBlock Name="textBlock39" HorizontalAlignment="Left" Margin="230,128,0,0" TextWrapping="Wrap" Text="VLAN ID" VerticalAlignment="Top"/>

        </Grid>
        <Grid Grid.Row="2">
            <Border BorderBrush="#FFE0E0E0" BorderThickness="0 1 0 0" />
            <ComboBox Name="esxiHostName1" HorizontalAlignment="Left" Margin="71,30,0,0" VerticalAlignment="Top" Width="200"/>
            <ComboBox Name="ssdDatastore1" HorizontalAlignment="Left" Margin="512,30,0,0" VerticalAlignment="Top" Width="200"/>
            <ComboBox Name="hddDatastore1" HorizontalAlignment="Left" Margin="512,88,0,0" VerticalAlignment="Top" Width="200"/>
            <Button Name="openVmConsole1" Content="Open VM Console" HorizontalAlignment="Left" Margin="824,88,0,0" VerticalAlignment="Top" Width="121" IsEnabled="False" />
            <ComboBox Name="acropolisHomeDatastore1" HorizontalAlignment="Left" Margin="292,88,0,0" VerticalAlignment="Top" Width="200"/>
            <CheckBox Name="useSameDatastore1" Content="Use Same Datastore for All vDisks" HorizontalAlignment="Left" Margin="292,33,0,0" VerticalAlignment="Top"/>
            <ComboBox Name="vswitch1" HorizontalAlignment="Left" Margin="71,88,0,0" VerticalAlignment="Top" Width="200" Height="22"/>
            <TextBox Name="ssdSize1" HorizontalAlignment="Left" Height="23" Margin="726,30,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="79"/>
            <TextBox Name="hddSize1" HorizontalAlignment="Left" Height="23" Margin="726,87,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="79"/>
            <TextBlock Name="deploymentStatus1" HorizontalAlignment="Left" Margin="830,40,0,0" TextWrapping="Wrap" Text="Not Deployed" VerticalAlignment="Top" Foreground="#FFFF0303" Height="32" Width="103" FontSize="16"/>

            <TextBlock Name="textBlock12" HorizontalAlignment="Left" Margin="726,12,0,0" TextWrapping="Wrap" Text="Size (GB)" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock12_Copy" HorizontalAlignment="Left" Margin="726,70,0,0" TextWrapping="Wrap" Text="Size (GB)" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock2" HorizontalAlignment="Left" Margin="512,10,0,0" TextWrapping="Wrap" Text="SSD Datastore" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock3" HorizontalAlignment="Left" Margin="512,70,0,0" TextWrapping="Wrap" Text="HDD Datastore" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock6" HorizontalAlignment="Left" Margin="71,9,0,0" TextWrapping="Wrap" Text="ESXi Host Name" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock7" HorizontalAlignment="Left" TextWrapping="Wrap" Text="Node 1" VerticalAlignment="Top" Margin="10,48,0,0" RenderTransformOrigin="0.568,5.451" FontSize="14.667"/>
            <TextBlock Name="textBlock10" HorizontalAlignment="Left" Margin="830,13,0,0" TextWrapping="Wrap" Text="Deployment Status:" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock4" HorizontalAlignment="Left" Margin="292,70,0,0" TextWrapping="Wrap" Text="Acropolis Hypervisor Datastore (8GB)" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock26" HorizontalAlignment="Left" TextWrapping="Wrap" Text="vSwitch Name" VerticalAlignment="Top" Height="16" Width="94" Margin="71,67,0,0"/>
        </Grid>

        <Grid Grid.Row="3" >
            <Border BorderBrush="#FFE0E0E0" BorderThickness="0 1 0 0" />
            <ComboBox Name="esxiHostName2" HorizontalAlignment="Left" Margin="71,30,0,0" VerticalAlignment="Top" Width="200"/>
            <ComboBox Name="ssdDatastore2" HorizontalAlignment="Left" Margin="512,30,0,0" VerticalAlignment="Top" Width="200"/>
            <ComboBox Name="hddDatastore2" HorizontalAlignment="Left" Margin="512,88,0,0" VerticalAlignment="Top" Width="200"/>
            <TextBlock Name="textBlock8" HorizontalAlignment="Left" Margin="512,10,0,0" TextWrapping="Wrap" Text="SSD Datastore" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock9" HorizontalAlignment="Left" Margin="512,70,0,0" TextWrapping="Wrap" Text="HDD Datastore" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock13" HorizontalAlignment="Left" Margin="71,9,0,0" TextWrapping="Wrap" Text="ESXi Host Name" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock14" HorizontalAlignment="Left" TextWrapping="Wrap" Text="Node 2" VerticalAlignment="Top" Margin="10,48,0,0" RenderTransformOrigin="0.568,5.451" FontSize="14.667"/>
            <Button Name="openVmConsole2" Content="Open VM Console" HorizontalAlignment="Left" Margin="824,88,0,0" VerticalAlignment="Top" Width="121" IsEnabled="False" />
            <TextBlock Name="deploymentStatus2" HorizontalAlignment="Left" Margin="830,40,0,0" TextWrapping="Wrap" Text="Not Deployed" VerticalAlignment="Top" Foreground="#FFFF0303" Height="32" Width="103" FontSize="16"/>
            <TextBlock Name="textBlock15" HorizontalAlignment="Left" Margin="830,13,0,0" TextWrapping="Wrap" Text="Deployment Status:" VerticalAlignment="Top"/>
            <ComboBox Name="acropolisHomeDatastore2" HorizontalAlignment="Left" Margin="292,88,0,0" VerticalAlignment="Top" Width="200"/>
            <TextBlock Name="textBlock16" HorizontalAlignment="Left" Margin="292,70,0,0" TextWrapping="Wrap" Text="Nutanix CE Disk Image Datastore" VerticalAlignment="Top"/>
            <CheckBox Name="useSameDatastore2" Content="Use Same Datastore for All vDisks" HorizontalAlignment="Left" Margin="292,33,0,0" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock17" HorizontalAlignment="Left" TextWrapping="Wrap" Text="vSwitch Name" VerticalAlignment="Top" Height="16" Width="94" Margin="71,67,0,0"/>
            <ComboBox Name="vswitch2" HorizontalAlignment="Left" Margin="71,88,0,0" VerticalAlignment="Top" Width="200" Height="22"/>
            <TextBox Name="ssdSize2" HorizontalAlignment="Left" Height="23" Margin="726,30,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="79"/>
            <TextBlock Name="textBlock18" HorizontalAlignment="Left" Margin="726,12,0,0" TextWrapping="Wrap" Text="Size (GB)" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock12_Copy1" HorizontalAlignment="Left" Margin="726,70,0,0" TextWrapping="Wrap" Text="Size (GB)" VerticalAlignment="Top"/>
            <TextBox Name="hddSize2" HorizontalAlignment="Left" Height="23" Margin="726,87,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="79"/>

        </Grid>

        <Grid Grid.Row="4" >
            <Border BorderBrush="#FFE0E0E0" BorderThickness="0 1 0 0" />
            <ComboBox Name="esxiHostName3" HorizontalAlignment="Left" Margin="71,30,0,0" VerticalAlignment="Top" Width="200"/>
            <ComboBox Name="ssdDatastore3" HorizontalAlignment="Left" Margin="512,30,0,0" VerticalAlignment="Top" Width="200"/>
            <ComboBox Name="hddDatastore3" HorizontalAlignment="Left" Margin="512,88,0,0" VerticalAlignment="Top" Width="200"/>
            <TextBlock Name="textBlock19" HorizontalAlignment="Left" Margin="512,10,0,0" TextWrapping="Wrap" Text="SSD Datastore" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock20" HorizontalAlignment="Left" Margin="512,70,0,0" TextWrapping="Wrap" Text="HDD Datastore" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock21" HorizontalAlignment="Left" Margin="71,9,0,0" TextWrapping="Wrap" Text="ESXi Host Name" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock22" HorizontalAlignment="Left" TextWrapping="Wrap" Text="Node 3" VerticalAlignment="Top" Margin="10,48,0,0" RenderTransformOrigin="0.568,5.451" FontSize="14.667"/>
            <Button Name="openVmConsole3" Content="Open VM Console" HorizontalAlignment="Left" Margin="824,88,0,0" VerticalAlignment="Top" Width="121" IsEnabled="False" />
            <TextBlock Name="deploymentStatus3" HorizontalAlignment="Left" Margin="830,40,0,0" TextWrapping="Wrap" Text="Not Deployed" VerticalAlignment="Top" Foreground="#FFFF0303" Height="32" Width="103" FontSize="16"/>
            <TextBlock Name="textBlock23" HorizontalAlignment="Left" Margin="830,13,0,0" TextWrapping="Wrap" Text="Deployment Status:" VerticalAlignment="Top"/>
            <ComboBox Name="acropolisHomeDatastore3" HorizontalAlignment="Left" Margin="292,88,0,0" VerticalAlignment="Top" Width="200"/>
            <TextBlock Name="textBlock24" HorizontalAlignment="Left" Margin="292,70,0,0" TextWrapping="Wrap" Text="Nutanix CE Disk Image Datastore" VerticalAlignment="Top"/>
            <CheckBox Name="useSameDatastore3" Content="Use Same Datastore for All vDisks" HorizontalAlignment="Left" Margin="292,33,0,0" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock25" HorizontalAlignment="Left" TextWrapping="Wrap" Text="vSwitch Name" VerticalAlignment="Top" Height="16" Width="94" Margin="71,67,0,0"/>
            <ComboBox Name="vswitch3" HorizontalAlignment="Left" Margin="71,88,0,0" VerticalAlignment="Top" Width="200" Height="22"/>
            <TextBox Name="ssdSize3" HorizontalAlignment="Left" Height="23" Margin="726,30,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="79"/>
            <TextBlock Name="textBlock27" HorizontalAlignment="Left" Margin="726,12,0,0" TextWrapping="Wrap" Text="Size (GB)" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock12_Copy2" HorizontalAlignment="Left" Margin="726,70,0,0" TextWrapping="Wrap" Text="Size (GB)" VerticalAlignment="Top"/>
            <TextBox Name="hddSize3" HorizontalAlignment="Left" Height="23" Margin="726,87,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="79"/>

        </Grid>

        <Grid Grid.Row="5" >
            <Border BorderBrush="#FFE0E0E0" BorderThickness="0 1 0 0" />
            <ComboBox Name="esxiHostName4" HorizontalAlignment="Left" Margin="71,30,0,0" VerticalAlignment="Top" Width="200"/>
            <ComboBox Name="ssdDatastore4" HorizontalAlignment="Left" Margin="512,30,0,0" VerticalAlignment="Top" Width="200"/>
            <ComboBox Name="hddDatastore4" HorizontalAlignment="Left" Margin="512,88,0,0" VerticalAlignment="Top" Width="200"/>
            <TextBlock Name="textBlock28" HorizontalAlignment="Left" Margin="512,10,0,0" TextWrapping="Wrap" Text="SSD Datastore" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock31" HorizontalAlignment="Left" Margin="512,70,0,0" TextWrapping="Wrap" Text="HDD Datastore" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock32" HorizontalAlignment="Left" Margin="71,9,0,0" TextWrapping="Wrap" Text="ESXi Host Name" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock33" HorizontalAlignment="Left" TextWrapping="Wrap" Text="Node 4" VerticalAlignment="Top" Margin="10,48,0,0" RenderTransformOrigin="0.568,5.451" FontSize="14.667"/>
            <Button Name="openVmConsole4" Content="Open VM Console" HorizontalAlignment="Left" Margin="824,88,0,0" VerticalAlignment="Top" Width="121" IsEnabled="False" />
            <TextBlock Name="deploymentStatus4" HorizontalAlignment="Left" Margin="830,40,0,0" TextWrapping="Wrap" Text="Not Deployed" VerticalAlignment="Top" Foreground="#FFFF0303" Height="32" Width="103" FontSize="16"/>
            <TextBlock Name="textBlock34" HorizontalAlignment="Left" Margin="830,13,0,0" TextWrapping="Wrap" Text="Deployment Status:" VerticalAlignment="Top"/>
            <ComboBox Name="acropolisHomeDatastore4" HorizontalAlignment="Left" Margin="292,88,0,0" VerticalAlignment="Top" Width="200"/>
            <TextBlock Name="textBlock35" HorizontalAlignment="Left" Margin="292,70,0,0" TextWrapping="Wrap" Text="Nutanix CE Disk Image Datastore" VerticalAlignment="Top"/>
            <CheckBox Name="useSameDatastore4" Content="Use Same Datastore for All vDisks" HorizontalAlignment="Left" Margin="292,33,0,0" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock36" HorizontalAlignment="Left" TextWrapping="Wrap" Text="vSwitch Name" VerticalAlignment="Top" Height="16" Width="94" Margin="71,67,0,0"/>
            <ComboBox Name="vswitch4" HorizontalAlignment="Left" Margin="71,88,0,0" VerticalAlignment="Top" Width="200" Height="22"/>
            <TextBox Name="ssdSize4" HorizontalAlignment="Left" Height="23" Margin="726,30,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="79"/>
            <TextBlock Name="textBlock37" HorizontalAlignment="Left" Margin="726,12,0,0" TextWrapping="Wrap" Text="Size (GB)" VerticalAlignment="Top"/>
            <TextBlock Name="textBlock12_Copy3" HorizontalAlignment="Left" Margin="726,70,0,0" TextWrapping="Wrap" Text="Size (GB)" VerticalAlignment="Top"/>
            <TextBox Name="hddSize4" HorizontalAlignment="Left" Height="23" Margin="726,87,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="79"/>


        </Grid>
        

    </Grid>

</Window>
"@


#endregion

#region Function Declaration



Function OpenFileBrowseDialog
{
#Opens a Windows file browsing dialog to select the Nutanix CE disk image file.
#NOTE:  Dialog only accepts *.img as the file extension
    
    $dialog = New-Object System.Windows.Forms.OpenFileDialog
    $dialog.InitialDirectory = [IO.Path]::Combine($env:USERPROFILE,"Downloads")
    $dialog.filter = "Nutanix CE Disk Image (*.img)|*.img"
    $dialog.ShowDialog() | Out-Null
    return $dialog.FileName
}

Function PopulateValidEsxiHostValues
{
#Populates the contents of the dropdown menus for ESXi Host Name in each Node panel
#Initially sets the host for each node to the first 4 nodes alphabetically

    for($i=1; $i -le 4; $i++)
    {
        Invoke-Expression -Command $('$currentNodeComboBox = $esxiHostName'+$i)
        $currentNodeComboBox.Clear()
        foreach ($esxiHostName in ($esxiHosts.Keys | Sort-Object))
        {
            [void]($currentNodeComboBox.Items.Add($esxiHostName))
            if($i -gt $esxiHosts.Keys.Count)
            {
                $j = $esxiHosts.Keys.Count - 1
            }
            else
            {
                $j = $i - 1
            }
            $currentNodeComboBox.SelectedIndex = $j
            PopulateNodeParametersBasedOnSelectedEsxiHost -nodeNumber $i
        }
    }

}

Function SetInfoPanel
{
# Used to display instructions and information at the top of the window
# Depending on the type of information being displayed, it will be shown in a different color

    Param(
        [String]$message,
        [ValidateSet("info","success","warning","error")][String]$type,
        [Switch]$default
    )

    $messageColorHash = @{info="Blue";success="Green";warning="Orange";error="Red"}

    if($default)
    {
        $infoPanel.Text = "Create your desired configuration.  Please fill in the required fields to begin deployment"
        $infoPanel.Foreground = "Blue"
    }
    else
    {
        $infoPanel.Foreground = $messageColorHash[$type]
        $infoPanel.Text = $message
    }

}

            
Function ConnectToVcenterButtonClicked
{
# If connection parameters (pink by default) are populated with valid connection address and credentials, the connection will be successful.
# Upon successful connection, information about the ESXi hosts, datastores, vSwitches, and port groups are collected for validation purposes.
# Hostnames made available for deployment deliberately exclude those that are not connected to vCenter or do not have support for nested virtualization.
# Data is placed into a custom object for ongoing reference during validation and Nutunix node deployment.

    if($vcenterServerName.Text -and $vcenterServerUsername.Text -and $vcenterServerPassword.Password)
    {    
        if((Get-PSSnapin | %{$_.Name}) -notcontains "Vmware.VimAutomation.Core")
        {
            Add-PSSnapin Vmware.VimAutomation.Core -ErrorAction SilentlyContinue
        }

        if((Get-Module | %{$_.Name}) -notcontains "VMware.VimAutomation.Vds")
        {
            Import-Module VMware.VimAutomation.Vds -ErrorAction SilentlyContinue
        }

        Set-PowerCLIConfiguration -InvalidCertificateAction Ignore -Scope Session -DisplayDeprecationWarnings $false -DefaultVIServerMode Single -Confirm:$false
        
        Connect-VIServer $vcenterServerName.Text -User $vcenterServerUsername.Text -Password $vcenterServerPassword.Password -ErrorAction SilentlyContinue
        
        if($global:DefaultViServer -match $vcenterServerName.Text)
        {
            $connectToVcenter.Content = "Connected"
            $connectToVcenter.Foreground = "GREEN"
            
            $script:esxiHosts = @{}
        
            $hostViewObjects = Get-View -ViewType HostSystem

            foreach($hostViewObject in $hostViewObjects)
            {
                if($hostViewObject.Capability.NestedHVSupported -and ($hostViewObject.Summary.Runtime.ConnectionState -match 'connected'))
                {

                    $vSwitches = @()
					$portGroups = @()
                    foreach($standardvSwitch in $hostViewObject.Config.Network.Vswitch)
                    {
                        $vSwitches += [PSCustomObject]@{
                            name=$standardvSwitch.Name;
                            vSwitchType='Standard'
                        }
                    }
                    
                    foreach($distributedvSwitch in $hostViewObject.Config.Network.ProxySwitch)
                    {
                        $vSwitches += [PSCustomObject]@{
                            name=$distributedvSwitch.DvsName;
                            vSwitchType='Distributed'
                        }
                    }

                    foreach($portGroup in $($hostViewObject.Network | %{Get-View -Id $_ } | %{$_.Name}))
                    {
                        $portGroups += $portGroup
                    }

                    $script:esxiHosts.Add(
                        $($hostViewObject | Get-VIObjectByVIView | %{$_.Name}),
                        [PSCustomObject]@{
                            datastores = $hostViewObject.Datastore | %{Get-View -Id $_} | %{[PSCustomObject]@{name=$_.Name; freeSpaceGB=$($_.Summary.FreeSpace / 1GB)}};
                            vSwitches = $vSwitches;
                            portGroups = $portGroups
						}
                    )
				}
                else
                {
                    $ineligibleEsxiHosts += $hostViewObject | Get-VIObjectByVIView | %{$_.Name}
                }

            }
                            
             
            PopulateValidEsxiHostValues
           
            $connectToVcenter.IsEnabled = $false
            $nodesToDeploy.IsEnabled = $true
            $vmNameBase.IsEnabled = $true
            $browseForCeImage.IsEnabled = $true
            $pathToCeImage.IsEnabled = $true
            $pathToCeImage.Background = "Pink"
            $portGroupName.IsEnabled = $true
            $trunkPortGroup.IsEnabled = $true
            $vlanId.IsEnabled = $true
            $vlanId.Background = "Pink"
            $numCpu.IsEnabled = $true
            $ramGB.IsEnabled = $true

            ProcessNodesToDeploySelection
            SetInfoPanel -default
            
        }
        else
        {
            SetInfoPanel -message "There was a problem connecting to vCenter.  Check the server address and credentials before trying again." -type error
        }
    }
}

Function PopulateNodeParametersBasedOnSelectedEsxiHost
{
# When the ESXi host name is selected in a Nutanix node panel, the corresponding options associated with that host are also updated.
# Fields updated in the process:  vSwitches and ADatastores

    Param(
    [Int]$nodeNumber
    )
    
    Invoke-Expression -Command $('$currentNodeEsxiHostName = $esxiHostName' + $nodeNumber + '.SelectedValue')
	if($currentNodeEsxiHostName)
	{
		foreach($label in @('acropolisHome','ssd','hdd'))
		{
			Invoke-Expression -Command $('$currentField = $' + $label + 'Datastore' + $nodeNumber)
			$currentField.Items.Clear()
			foreach($datastore in ($esxiHosts[$currentNodeEsxiHostName].datastores | Sort-Object Name))
			{
				$textToDisplay = $($datastore.Name + "`t" + $("{0:N0}" -f $datastore.freeSpaceGB) + " GB Free")
				$currentField.Items.Add($textToDisplay)
				Add-Member -InputObject $datastore -MemberType NoteProperty -Name dropDownIndex -Value $($currentField.Items.Count - 1) -Force -TypeName Integer
			}
			$currentField.SelectedIndex = 0
		}

		Invoke-Expression -Command $('$currentField = $vSwitch' + $nodeNumber)
		$currentField.Items.Clear()
		foreach($vswitch in ($esxiHosts[$currentNodeEsxiHostName].vswitches | Sort-Object vswitchType,Name))
		{
				$currentField.Items.Add($vswitch.Name)
				Add-Member -InputObject $vswitch -MemberType NoteProperty -Name dropDownIndex -Value $($currentField.Items.Count - 1) -Force -TypeName Integer
		}
		$currentField.SelectedIndex = 0
	}
    
}

Function ProcessNodesToDeploySelection
{
# When the number of nodes to deploy is changed, the panels are selectively hidden or displayed based on that selection
# This function manipulates the XAML objects to display only the panels needed for deployment.

    for($i=1; $i -le 4;$i++)
    {
        if($i -le $nodesToDeploy.SelectedValue)
        {
            Invoke-Expression $('$rowDef' + $i + '.Height=120')
        }
        else
        {
            Invoke-Expression $('$rowDef' + $i + '.Height=0')
        }
    }
    $footer.Height = 10
}

Function ValidatePortGroupNameInput
{
# During input of the port group name or a change of the ESXi host to be deployed to, a check is performed to ensure that the port group name doesn't already exist.
# Although it's possible to have duplicate port group names with different attributes on separate hosts, this script follows best practices by ensuring consistency across hosts.

    $portGroupNameUnique = $true
    for($i=1; $i -le $nodesToDeploy.SelectedValue; $i++)
    {
        Invoke-Expression -Command $('$currentEsxiHostName = $esxiHostName' + $i + '.SelectedValue')
        
        if(CheckPortGroupExistsOnHost -esxiHostName $currentEsxiHostName -portGroupName $portGroupName.Text)
        {
            $portGroupNameUnique = $false
            $portGroupName.Background = "Pink"
            SetInfoPanel -type error -message "Port Group is already in use on one or more selected ESXi hosts."
        }
		else
		{
			if($portGroupName.Text.Length -gt 0)
			{
				SetInfoPanel -default
				$portGroupName.Background = "White"
			}
		}
    }
    if($portGroupNameUnique){Return $true}else{Return $false}
}


Function CheckIfDeployable
{
# The deployment button is not available until all variables are validated.
# Each host must have the following selected:
#   ESXi Host Name
#   Datastore(s)    
#   vSwitch
#   SSD size
#   HDD size
# There can be no duplicate port group names in the environment.
# An image file must be selected.
# The minimum CPU count and RAM must be met.
# VLAN ID must be valid.
#

    $isDeployable = $true
   
    for($i=1; $i -le $nodesToDeploy.SelectedValue; $i++)
    {
        Invoke-Expression -Command $('$currentField = $ssdSize' + $i)
        if ([int]$currentField.Text -lt $defaultSsdSize)
        {
            $isDeployable = $false
        }
        Invoke-Expression -Command $('$currentField = $hddSize' + $i)
        if ([int]$currentField.Text -lt $defaultHddSize)
        {
            $isDeployable = $false
        }
        Invoke-Expression -Command $('$currentField = $vswitch' + $i)
        if($currentField.SelectedValue.Length -eq 0)
        {
            $isDeployable = $false
        }
        if(-not (ValidatePortGroupNameInput))
        {
            $isDeployable = $false
        }

    }

    if(($portGroupName.Text.Length -eq 0) -or ($vmNameBase.Text.Length -eq 0) -or ($pathToCeImage.Text.Length -eq 0) -or ([int]$ramGB.Text -lt $defaultRamGB) -or ([int]$numCpu.Text -lt $defaultNumCpu) -or (0..4095 -notcontains [int]$vlanId.Text) -or ($vlanId.Text.Length -eq 0))
    {
        $isDeployable = $false
    }


    if($isDeployable)
    {
        $deployButton.Foreground = "Blue"
        $deployButton.isEnabled = $true
        SetInfoPanel -type success -message "Ready for Deployment"
    }
    else
    {
        $deployButton.Foreground = "Gray"
        $deployButton.IsEnabled = $false
    }
}

Function ValidateVlanId
{
# Flags the VLAN ID field if the value isn't valid

    if($vlanId.Text.Length -gt 0 -and (0..4095 -contains [Int32]$vlanId.Text))
    {
        $vlanId.Background = "White"
        SetInfoPanel -default
    }
    else
    {
        $vlanId.Background = "Pink"
        SetInfoPanel -type error -message "VLAN ID must be a value from 0 to 4095"
    }
}

Function DeployNodes
{
# Processes pre-validated input values to create desired node configuration
# Creates a single node first and uses it as a source template for cloning additional nodes.
# As each node is deployed, it is booted and available for customization.

    $deployButton.IsEnabled = $false

    $numberOfNodes = [Int]$nodesToDeploy.SelectedValue     
	$nodeConfigurations = @()
    for($i=1; $i -le $numberOfNodes; $i++)
    {
        $nodeConfiguration[$i].nodeNumber=$i;
        $nodeConfiguration[$i].esxiHostName=$(Invoke-Expression -Command $('$esxiHostName' + $i + '.SelectedValue'))
        $nodeConfiguration[$i].vmName=$($vmNameBase.Text + $i.ToString("0"));
        $nodeConfiguration[$i].numCpu=[Int]$numCpu.Text
        $nodeConfiguration[$i].ramGB=[Int]$ramGB.Text
        Invoke-Expression -Command $('$nodeConfiguration[$i].acropolisStorage.datastore = $esxiHosts[$nodeConfiguration[$i].esxiHostName].datastores | ?{$_.dropDownIndex -eq $acropolisHomeDatastore' + $i + '.SelectedIndex} | %{$_.Name}')
        foreach($storageType in @('ssd','hdd'))
        {
            Invoke-Expression -Command $('$nodeConfiguration[$i].' + $storageType + 'Storage.datastore = $esxiHosts[$nodeConfiguration[$i].esxiHostName].datastores | ?{$_.dropDownIndex -eq $' + $storageType + 'Datastore' + $i + '.SelectedIndex} | %{$_.Name}')
            Invoke-Expression -Command $('$nodeConfiguration[$i].' + $storageType + 'Storage.vdiskSize = [Int]$' + $storageType + 'Size' + $i + '.Text')
        }
        Invoke-Expression -Command $('$nodeConfiguration[$i].network.vswitchName = $vswitch' + $i + '.SelectedValue')
        Invoke-Expression -Command $('$nodeConfiguration[$i].network.vswitchType = $esxiHosts[$nodeConfiguration[$i].esxiHostName].vSwitches | ?{$_.dropDownIndex -eq $vswitch' + $i + '.SelectedIndex} | %{$_.vswitchType}')
        $nodeConfiguration[$i].network.portGroupName = $portGroupName.Text
        $nodeConfiguration[$i].network.vlanId = [Int]$vlanId.text
        $nodeConfigurations += $nodeConfiguration[$i]
        SetInfoPanel -type info -message $("Deploying Node " + $i)
        
        if($i -eq 1)
        {
            Invoke-Expression -Command $('$deploymentStatus' + $i + '.Text = ''Deploying''')
            Invoke-Expression -Command $('$deploymentStatus' + $i + '.Foreground = ''BLUE''')
            CreateNutanixCeNodeVm -nodeConfigurationObject $nodeConfiguration[$i]
        }
        else
        {
            Invoke-Expression -Command $('$deploymentStatus' + $($i-1) + '.Text = ''Cloning From''')
            Invoke-Expression -Command $('$deploymentStatus' + $i + '.Text = ''Cloning To''')
            Invoke-Expression -Command $('$deploymentStatus' + $i + '.Foreground = ''BLUE''')
            CloneNutanixCeNodeVm -sourceNodeConfigurationObject $nodeConfiguration[$i-1] -newNodeConfigurationObject $nodeConfiguration[$i]
            ConfigureSsdAndHddForNutanixCeNode -nodeConfigurationObject $nodeConfiguration[$i-1]
            Start-VM $nodeConfiguration[$i-1].vmName
            Invoke-Expression -Command $('$deploymentStatus' + $($i-1) + '.Text = ''Deployed''')
            Invoke-Expression -Command $('$deploymentStatus' + $($i-1) + '.Foreground = ''GREEN''')
            Invoke-Expression -Command $('$openVmConsole' + $($i-1) + '.IsEnabled = $true')
        }

        if($i -eq $numberOfNodes)
        {
            ConfigureSsdAndHddForNutanixCeNode -nodeConfigurationObject $nodeConfiguration[$i]
            Start-VM $nodeConfiguration[$i].vmName
    
            Invoke-Expression -Command $('$deploymentStatus' + $i + '.Text = ''Deployed''')
            Invoke-Expression -Command $('$deploymentStatus' + $i + '.Foreground = ''GREEN''')
            Invoke-Expression -Command $('$openVmConsole' + $i + '.IsEnabled = $true')
        }

    }
    SetInfoPanel -type info -message $("All Nodes Deployed.  Open VM Console for each node to complete Nutanix CE installation.")
}      

Function CloneNutanixCeNodeVm
{
    Param(
        [Parameter(Mandatory=$True)][PSObject]$sourceNodeConfigurationObject,
        [Parameter(Mandatory=$True)][PSObject]$newNodeConfigurationObject
    )
    
    CreatePortGroupOnEsxiHost -nodeConfigurationObject $newNodeConfigurationObject

    New-VM -VM $sourceNodeConfigurationObject.vmName -Name $newNodeConfigurationObject.vmName -VMHost $newNodeConfigurationObject.esxiHostName -Datastore $newNodeConfigurationObject.acropolisStorage.datastore
}


Function ConfigureSsdAndHddForNutanixCeNode
{
#  SSD (emulated) and HDD disks are added after the VM creation and/or cloning operation.
#  The SSD can be located on any datastore and is emulated via a configuration parameter.

    Param(

        [Parameter(Mandatory=$True)][PSObject]$nodeConfigurationObject
    )

    $nodeVmObj = Get-VM $nodeConfigurationObject.vmName
    $hddVdiskObj = $nodeVmObj | New-HardDisk -CapacityGB $nodeConfigurationObject.hddStorage.vdiskSize -ThinProvisioned -Datastore $nodeConfigurationObject.hddStorage.datastore
    $scsiControllerObj = $hddVdiskObj | New-ScsiController -Type ParaVirtual
	$hddVdiskObj = Get-HardDisk -VM $nodeVmObj | ?{[Int]$_.capacityGB -eq $nodeConfigurationObject.hddStorage.vdiskSize}
    $ssdVdiskObj = $nodeVmObj | New-HardDisk -Controller $scsiControllerObj -CapacityGB $nodeConfigurationObject.ssdStorage.vdiskSize -ThinProvisioned -Datastore $nodeConfigurationObject.ssdStorage.datastore
    
    $scsiId = $("scsi" + ($ssdVdiskObj.ExtensionData.ControllerKey.ToString().Substring($ssdVdiskObj.ExtensionData.ControllerKey.ToString().Length - 1)) + ':' + [String]$ssdVdiskObj.ExtensionData.UnitNumber)
    $ssdOption = New-Object VMware.Vim.OptionValue
    $ssdOption.Key = $($scsiId + ".virtualSSD")
    $ssdOption.Value = 1
    
    $vmConfigSpec = New-Object VMware.Vim.VirtualMachineConfigSpec
    $vmConfigSpec.ExtraConfig += $ssdOption
    $nodeVmObj.ExtensionData.ReconfigVM($vmConfigSpec)
}

Function CheckPortGroupExistsOnHost
{
# Checks the pre-populated host attributes to determine whether the port group exists on that host.

    Param(
    [String]$esxiHostName,
    [String]$portGroupName
    )
	if($portGroupName)
	{
		if($esxiHosts[$esxiHostName].portGroups -contains $portGroupName)
		{
			Return $true
		}
		else
		{
			Return $false
		}
	}
	else
	{
		Return $false
	}
}

Function CreatePortGroupOnEsxiHost
{
# Creates a new standard virtual port group on a given host or a virtual distributed port group on a distributed vswitch.
# In order to support nested virtualization, the promiscuous mode and forged transmits must be enabled on the target port group.
# If the port group already exist, the function returns a reference to the existing port group.

    Param(

        [Parameter(Mandatory=$True)][PSObject]$nodeConfigurationObject
    )
    
    $createdNewPortGroup = $false
    
    if(((Get-VMHost $nodeConfigurationObject.esxiHostName).ExtensionData.Network | %{ Get-View -Id $_ } | %{$_.Name}) -notcontains $nodeConfigurationObject.network.portGroupName)
    {
        if($nodeConfigurationObject.network.vSwitchType -eq 'Standard')
        {
            
            $newPortGroupObj = New-VirtualPortGroup -Name $nodeConfigurationObject.network.portgroupName -VirtualSwitch $(Get-VirtualSwitch -Name $nodeConfigurationObject.network.vswitchName -VMHost $nodeConfigurationObject.esxiHostName) -VLanId $nodeConfigurationObject.network.vlanId
            $hostPortGroupSpec = $newPortGroupObj.ExtensionData.Spec
            $nestedHvNetworkSecurityPolicy = New-Object VMware.Vim.HostNetworkSecurityPolicy
            $nestedHvNetworkSecurityPolicy.AllowPromiscuous = $true
            $nestedHvNetworkSecurityPolicy.ForgedTransmits = $true
            $hostPortGroupSpec.Policy.Security = $nestedHvNetworkSecurityPolicy
            $hostNetworkSystem = Get-View ((Get-VMHost $nodeConfigurationObject.esxiHostName).ExtensionData.ConfigManager.NetworkSystem)
            $hostNetworkSystem.UpdatePortGroup($newPortGroupObj.Name,$hostPortGroupSpec)
            $createdNewPortGroup = $true

        }
        elseif($nodeConfigurationObject.network.vSwitchType -eq 'Distributed')
        {
            
            #Create New Port Group on Distributed vSwitch
            #Set Promiscuous Mode  and Forged Transmits
            $newPortGroupObj = New-VDPortGroup -Name $nodeConfigurationObject.network.portgroupName -VDSwitch $nodeConfigurationObject.network.vswitchName -NumPorts 8 -VLanId $nodeConfigurationObject.network.vlanId
            $portGroupConfigSpec = New-Object VMware.Vim.DVPortgroupConfigSpec
            $portConfig = New-Object VMware.Vim.VMwareDVSPortSetting
            $securityPolicy = New-Object VMware.Vim.DVSSecurityPolicy
            $securityPolicy.AllowPromiscuous = New-Object VMware.Vim.BoolPolicy
            $securityPolicy.AllowPromiscuous.Value = $true
            $securityPolicy.ForgedTransmits = New-Object VMware.Vim.BoolPolicy
            $securityPolicy.ForgedTransmits.Value = $true
            $portConfig.SecurityPolicy = $securityPolicy
            $portGroupConfigSpec.DefaultPortConfig = $portConfig
            $portGroupConfigSpec.ConfigVersion = $newPortGroupObj.ExtensionData.Config.ConfigVersion
			$newPortGroupObj.ExtensionData.ReconfigureDVPortGroup($portGroupConfigSpec)
            $createdNewPortGroup = $true

        }
    }
    else
    {
		if($nodeConfigurationObject.network.vSwitchType -eq 'Standard')
		{
			$newPortGroupObj = Get-VirtualPortGroup -Name $nodeConfigurationObject.network.portGroupName -VMHost $nodeConfigurationObject.esxiHostName
		}
		elseif($nodeConfigurationObject.network.vSwitchType -eq 'Distributed')
		{
			$newPortGroupObj = Get-VDPortGroup -Name $nodeConfigurationObject.network.portGroupName
		}
    }

    Return $newPortGroupObj
}


Function CreateNutanixCeNodeVm
{
# Creates a new VM with the Nutanix CE disk image.
# Configures the new VM to be capable of running a nested hypervisor.


    Param(

        [Parameter(Mandatory=$True)][PSObject]$nodeConfigurationObject
    )

    $newPortGroupObj = CreatePortGroupOnEsxiHost -nodeConfigurationObject $nodeConfigurationObject

    $datastore = Get-View -ViewType Datastore -Filter @{Name=$nodeConfigurationObject.acropolisStorage.datastore} | Get-VIObjectByVIView
    New-PSDrive -Location $datastore -Name $nodeConfigurationObject.acropolisStorage.datastore -PSProvider VimDatastore -Root "\"
    $vmDatastoreFolder = [System.IO.Path]::Combine($($datastore.Name + ':'),$nodeConfigurationObject.vmName)

    $vmdkName = $($nodeConfigurationObject.vmName + '_acropolis_home.vmdk')
    $vmdkFlatName = $($nodeConfigurationObject.vmName + '_acropolis_home-flat.vmdk')
        
    $newVmdkContents = @"
# Disk DescriptorFile
version=4
encoding="UTF-8"
CID=4470c879
parentCID=ffffffffpa
isNativeSnapshot="no"
createType="vmfs"
# Extent description
"@ + "`nRW 14540800 VMFS """ + $vmdkFlatName + """`n" + @"
# The Disk Data Base
#DDB

ddb.adapterType = "lsilogic"
ddb.geometry.cylinders = "905"
ddb.geometry.heads = "255"
ddb.geometry.sectors = "63"
ddb.longContentID = "ac2a7619c0a01d87476fe8124470c879"
ddb.uuid = "60 00 C2 9b 69 2f c9 76-74 c4 07 9e 10 87 3b f9"
ddb.virtualHWVersion = "10"
"@

    $newVmdkContents.Split("`n") | ForEach-Object -Begin{$outputTextFileContents = ""} -Process {$outputTextFileContents += $_ + "`n"}
    $workingDir = [System.IO.Path]::GetDirectoryName($pathToCeImage.Text)
    $localPathToVmdk = ([System.IO.Path]::Combine($workingDir,$vmdkName))
    [System.IO.File]::WriteAllText($localPathToVmdk,$outputTextFileContents,[System.Text.Encoding]::ASCII)
    $newVmObj = New-VM -Name $nodeConfigurationObject.vmName -VMHost $nodeConfigurationObject.esxiHostName -NumCpu $nodeConfigurationObject.numCpu -MemoryGB $nodeConfigurationObject.ramGB -Datastore $datastore -DiskGB 1 -DiskStorageFormat Thin -Portgroup $newPortGroupObj -GuestId centos64Guest -WarningAction SilentlyContinue
    $defaultHd = $newVmObj | Get-HardDisk
    $pathToVmStorageFolder = $defaultHd.ExtensionData.Backing.Filename.Split("/") | Select -First 1
    $defaultHd | Remove-HardDisk -DeletePermanently -Confirm:$false
	$nodeConfigurationObject.acropolisStorage.pathToVmdk = $($pathToVmStorageFolder + "/" + $vmdkName)
    $nodeConfigurationObject.acropolisStorage.pathToFlatVmdk = $($pathToVmStorageFolder + "/" + $vmdkFlatName)
	$psDrivePathToVmdk = $([System.IO.Path]::Combine($($datastore.Name + ':'),$($nodeConfigurationObject.acropolisStorage.pathToVmdk.Replace('/','\').Split('] ') | Select -Last 1)))
	$psDrivePathToFlatVmdk = $([System.IO.Path]::Combine($($datastore.Name + ':'),$($nodeConfigurationObject.acropolisStorage.pathToFlatVmdk.Replace('/','\').Split('] ') | Select -Last 1)))
    Copy-DatastoreItem -Item $localPathToVmdk -Destination $psDrivePathToVmdk
    Copy-DatastoreItem -Item $pathToCeImage.Text -Destination $psDrivePathToFlatVmdk
    $newVmObj | New-HardDisk -DiskPath $nodeConfigurationObject.acropolisStorage.pathToVmdk
    Get-ScsiController -VM $newVmObj | Set-ScsiController -Type VirtualLsiLogicSAS
    $vmConfigSpec = New-Object VMware.Vim.VirtualMachineConfigSpec
    $featMaskHvOption = New-Object VMware.Vim.OptionValue
    $featMaskHvOption.Key = "featMask.vm.hv.capable"
    $featMaskHvOption.Value = "Min:1"
    $vmConfigSpec.ExtraConfig += $featMaskHvOption
	$vmConfigSpec.NestedHVEnabled = $true
    $newVmObj.ExtensionData.ReconfigVM($vmConfigSpec)
}
#endregion

#region Static Variable Declaration

$defaultSsdSize = 200
$defaultHddSize = 500
$defaultNumCpu = 4
$defaultRamGB = 16

$xaml = [XML]$xamlCode
$xamlReader = New-Object System.Xml.XmlNodeReader $xaml

# Load assemblies with .NET components used in the script
Add-Type -AssemblyName PresentationFramework -IgnoreWarnings
Add-Type -AssemblyName System.Windows.Forms -IgnoreWarnings

$mainform = [Windows.Markup.XamlReader]::Load($xamlReader)


$mainform.DataContext = $windowDataContext

$xaml.SelectNodes("//*[@Name]") | %{Set-Variable -Name $_.Name -Value $mainform.FindName($_.Name)}

$nodeConfiguration = @{}

 <# Build Node Configuration as PSCustomObject
        
            
            VM
                Hostname
                Name
                Number of CPUs
                RAM GB
            Datastores
                Acropolis
                    vDisk Name
                SSD
                    Datastore
                    Path to vDisk
                    Size
                HDD
                    Datastore
                    Path to vDisk
                    Size
            Network
                vSwitch Name
                vSwitch Type (Standard or Distributed)
                Port Group Name
                VLAN ID
#>

for($i=1; $i -le 4; $i++)
{
    
    $currentNodeConfiguration = [PSCustomObject]@{
        nodeNumber=$null;
        esxiHostName=$null;
        vmName=$null;
        numCpu=$null;
        ramGB=$null;
        acropolisStorage=[PSCustomObject]@{
            datastore=$null;
            pathToVmdk=$null;
            pathToFlatVmdk=$null
        }
        ssdStorage=[PSCustomObject]@{
            datastore=$null;
            pathToVmdk=$null;
            vdiskSize=$null
        }
        hddStorage=[PSCustomObject]@{
            datastore=$null;
            pathToVmdk=$null;
            vdiskSize=$null
        }
        network=[PSCustomObject]@{
            vswitchName=$null;
            vswitchType=$null;
            portGroupName=$null;
            vlanId=$null
        }
    }
    $nodeConfiguration.Add($i,$currentNodeConfiguration)
}

#endregion

#region Event Handlers

$browseForCeImage.Add_Click({
    $pathToCeImage.Text = OpenFileBrowseDialog
    if($pathToCeImage.Text.Length -eq 0)
    {
        $pathToCeImage.Background = "Pink"
    }
    else
    {
        $pathToCeImage.Background = "White"
    }
    CheckIfDeployable
})

$connectToVcenter.Add_Click({
    ConnectToVcenterButtonClicked
})

1,3,4 | %{ $nodesToDeploy.Items.Add($_) | out-null }

$numCpu.Text = $defaultNumCpu
$ramGB.Text = $defaultRamGB

for($i=1; $i -le 4; $i++)
{
    Invoke-Expression -Command $('$ssdSize' + $i + '.Text = $defaultSsdSize')
    Invoke-Expression -Command $('$hddSize' + $i + '.Text = $defaultHddSize')
}


$esxiHostName1.Add_SelectionChanged({
	PopulateNodeParametersBasedOnSelectedEsxiHost -nodeNumber 1
	ValidatePortGroupNameInput
})

$esxiHostName2.Add_SelectionChanged({
	PopulateNodeParametersBasedOnSelectedEsxiHost -nodeNumber 2
	ValidatePortGroupNameInput
})

$esxiHostName3.Add_SelectionChanged({
	PopulateNodeParametersBasedOnSelectedEsxiHost -nodeNumber 3
	ValidatePortGroupNameInput
})

$esxiHostName4.Add_SelectionChanged({
	PopulateNodeParametersBasedOnSelectedEsxiHost -nodeNumber 4
	ValidatePortGroupNameInput
})

$useSameDatastore1.Add_Checked({
    $ssdDatastore1.SelectedIndex = $acropolisHomeDatastore1.SelectedIndex
    $ssdDatastore1.IsEnabled = $false
    $hddDatastore1.SelectedIndex = $acropolisHomeDatastore1.SelectedIndex
    $hddDatastore1.IsEnabled = $false

})

$useSameDatastore1.Add_UnChecked({
    $ssdDatastore1.IsEnabled = $true
    $hddDatastore1.IsEnabled = $true
})

$useSameDatastore2.Add_Checked({
    $ssdDatastore2.SelectedIndex = $acropolisHomeDatastore2.SelectedIndex
    $ssdDatastore2.IsEnabled = $false
    $hddDatastore2.SelectedIndex = $acropolisHomeDatastore2.SelectedIndex
    $hddDatastore2.IsEnabled = $false

})

$useSameDatastore2.Add_UnChecked({
    $ssdDatastore2.IsEnabled = $true
    $hddDatastore2.IsEnabled = $true
})

$useSameDatastore3.Add_Checked({
    $ssdDatastore3.SelectedIndex = $acropolisHomeDatastore3.SelectedIndex
    $ssdDatastore3.IsEnabled = $false
    $hddDatastore3.SelectedIndex = $acropolisHomeDatastore3.SelectedIndex
    $hddDatastore3.IsEnabled = $false

})

$useSameDatastore3.Add_UnChecked({
    $ssdDatastore3.IsEnabled = $true
    $hddDatastore3.IsEnabled = $true
})

$useSameDatastore4.Add_Checked({
    $ssdDatastore4.SelectedIndex = $acropolisHomeDatastore4.SelectedIndex
    $ssdDatastore4.IsEnabled = $false
    $hddDatastore4.SelectedIndex = $acropolisHomeDatastore4.SelectedIndex
    $hddDatastore4.IsEnabled = $false

})

$useSameDatastore4.Add_UnChecked({
    $ssdDatastore4.IsEnabled = $true
    $hddDatastore4.IsEnabled = $true
})




$vcenterServerName.Add_KeyUp({
    if ($vcenterServerName.Text.Length -gt 0)
    {
        $vcenterServerName.Background="White"
    }
    else
    {
        $vcenterServerName.Background="Pink"
    }

})

$vcenterServerName.Add_LostKeyboardFocus({
    if ($vcenterServerName.Text.Length -gt 0)
    {
        $vcenterServerName.Background="White"
    }
    else
    {
        $vcenterServerName.Background="Pink"
    }
})


$vcenterServerUsername.Add_KeyUp({
    

    if ($vcenterServerUsername.Text.Length -gt 0)
    {
        $vcenterServerUsername.Background="White"
    }
    else
    {
        $vcenterServerUsername.Background="Pink"
    }
})

$vcenterServerUsername.Add_LostKeyboardFocus({
    if ($vcenterServerUsername.Text.Length -gt 0)
    {
        $vcenterServerUsername.Background="White"
    }
    else
    {
        $vcenterServerUsername.Background="Pink"
    }
})


$vcenterServerPassword.Add_KeyUp({
    if ($vcenterServerPassword.Password.Length -gt 0)
    {
        $vcenterServerPassword.Background="White"
    }
    else
    {
        $vcenterServerPassword.Background="Pink"
    }
})

$vcenterServerPassword.Add_LostKeyboardFocus({
    if ($vcenterServerPassword.Password.Length -gt 0)
    {
        $vcenterServerPassword.Background="White"
    }
    else
    {
        $vcenterServerPassword.Background="Pink"
    }
})

$portGroupName.Add_KeyUp({
    if ($portGroupName.Text.Length -gt 0)
    {
        $portGroupName.Background="White"
    }
    else
    {
        $portGroupName.Background="Pink"
    }
    CheckIfDeployable
})

$portGroupName.Add_LostKeyboardFocus({
    if ($portGroupName.Text.Length -gt 0 -and (ValidatePortGroupNameInput))
    {
        $portGroupName.Background="White"
    }
    else
    {
        $portGroupName.Background="Pink"
    }
    CheckIfDeployable
})

$vmNameBase.Add_KeyUp({
    if ($vmNameBase.Text.Length -gt 0)
    {
        $vmNameBase.Background="White"
    }
    else
    {
        $vmNameBase.Background="Pink"
    }
    CheckIfDeployable
})

$vmNameBase.Add_LostKeyboardFocus({
    if ($vmNameBase.Text.Length -gt 0)
    {
        $vmNameBase.Background="White"
    }
    else
    {
        $vmNameBase.Background="Pink"
    }
    CheckIfDeployable
})



$acropolisHomeDatastore1.Add_SelectionChanged({
    if ($useSameDatastore1.IsChecked)
    {
        $ssdDatastore1.SelectedIndex = $acropolisHomeDatastore1.SelectedIndex
        $hddDatastore1.SelectedIndex = $acropolisHomeDatastore1.SelectedIndex
    }
    CheckIfDeployable
})

$acropolisHomeDatastore2.Add_SelectionChanged({
    if ($useSameDatastore2.IsChecked)
    {
        $ssdDatastore2.SelectedIndex = $acropolisHomeDatastore2.SelectedIndex
        $hddDatastore2.SelectedIndex = $acropolisHomeDatastore2.SelectedIndex
    }
    CheckIfDeployable
})

$acropolisHomeDatastore3.Add_SelectionChanged({
    if ($useSameDatastore3.IsChecked)
    {
        $ssdDatastore3.SelectedIndex = $acropolisHomeDatastore3.SelectedIndex
        $hddDatastore3.SelectedIndex = $acropolisHomeDatastore3.SelectedIndex
    }
    CheckIfDeployable
})

$acropolisHomeDatastore4.Add_SelectionChanged({
    if ($useSameDatastore4.IsChecked)
    {
        $ssdDatastore4.SelectedIndex = $acropolisHomeDatastore4.SelectedIndex
        $hddDatastore4.SelectedIndex = $acropolisHomeDatastore4.SelectedIndex
    }
    CheckIfDeployable
})

$numCpu.Add_LostKeyboardFocus({
    if ([int]$numCpu.Text -lt $defaultNumCpu)
    {
        $numCpu.Background = "Pink"
        SetInfoPanel -type error -message "Minimum of 4 vCPUs"
    }
    else
    {
        $numCpu.Background = "White"
        SetInfoPanel -default
    }
    CheckIfDeployable
})

$ramGB.Add_LostKeyboardFocus({
    if ([int]$ramGB.Text -lt $defaultNumCpu)
    {
        $ramGB.Background = "Pink"
        SetInfoPanel -type error -message "Minimum of 16GB RAM"
    }
    else
    {
        $ramGB.Background = "White"
        SetInfoPanel -default
    }
    CheckIfDeployable
})

$nodesToDeploy.Add_SelectionChanged({
    ProcessNodesToDeploySelection
    CheckIfDeployable
})

$trunkPortGroup.Add_Checked({
    $vlanId.Text = 4095
    $vlanId.Background = "White"
    $vlanId.IsEnabled = $false
    CheckIfDeployable
})

$trunkPortGroup.Add_UnChecked({
    $vlanId.IsEnabled = $true
    CheckIfDeployable
})

$vlanId.Add_LostKeyboardFocus({
    ValidateVlanId
    CheckIfDeployable
})

$deployButton.Add_Click({
    DeployNodes
})

$openVmConsole1.Add_Click({
    Open-VMConsoleWindow -VM $nodeConfiguration[1].vmName
})

$openVmConsole2.Add_Click({
    Open-VMConsoleWindow -VM $nodeConfiguration[2].vmName
})

$openVmConsole3.Add_Click({
    Open-VMConsoleWindow -VM $nodeConfiguration[3].vmName
})

$openVmConsole4.Add_Click({
    Open-VMConsoleWindow -VM $nodeConfiguration[4].vmName
})


#endregion

#region Show GUI

$mainform.ShowDialog()

#endregion
