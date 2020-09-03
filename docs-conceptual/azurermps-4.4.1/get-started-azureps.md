---
title: Начало работы с модулем Azure PowerShell | Документация Майкрософт
description: ''
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 44cca63bbea555f754d2625b13187c294647eef2
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89238660"
---
# <a name="getting-started-with-azure-powershell"></a><span data-ttu-id="6c0ca-102">Начало работы с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c0ca-102">Getting started with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="6c0ca-103">Модуль Azure PowerShell предназначен для администрирования ресурсов Azure из командной строки, а также для создания скриптов автоматизации, которые работают с Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="6c0ca-104">Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере и использовать в любом сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span> <span data-ttu-id="6c0ca-105">Эта статья поможет приступить к работе с модулем и объяснит основные принципы его работы.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-105">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

## <a name="connect"></a><span data-ttu-id="6c0ca-106">Подключение</span><span class="sxs-lookup"><span data-stu-id="6c0ca-106">Connect</span></span>

<span data-ttu-id="6c0ca-107">Самый простой способ начать работу — [запустить службу Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="6c0ca-107">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="6c0ca-108">Запустите Cloud Shell с верхней панели навигации портала Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-108">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Значок оболочки](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="6c0ca-110">Выберите нужную подписку и создайте учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-110">Choose the subscription you want to use and create a storage account.</span></span>

   ![Создание учетной записи хранения](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="6c0ca-112">Когда хранилище будет создано, Cloud Shell откроет сеанс PowerShell в браузере.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-112">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Использование Cloud Shell с PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="6c0ca-114">Вы также можете установить Azure PowerShell для локального использования в сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-114">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="6c0ca-115">Установите Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c0ca-115">Install Azure PowerShell</span></span>

<span data-ttu-id="6c0ca-116">Сначала установите последнюю версию модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-116">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="6c0ca-117">Сведения о последнем выпуске см. в [заметках о выпуске](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6c0ca-117">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="6c0ca-118">[Установите Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="6c0ca-118">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="6c0ca-119">Чтобы проверить установку, выполните `Get-InstalledModule AzureRM -AllVersions` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-119">To verify the installation was successful, run `Get-InstalledModule AzureRM -AllVersions` from your command line.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="6c0ca-120">Вход в Azure</span><span class="sxs-lookup"><span data-stu-id="6c0ca-120">Sign in to Azure</span></span>

<span data-ttu-id="6c0ca-121">Войдите в интерактивном режиме:</span><span class="sxs-lookup"><span data-stu-id="6c0ca-121">Sign on interactively:</span></span>

1. <span data-ttu-id="6c0ca-122">Введите `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-122">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="6c0ca-123">Появится диалоговое окно с запросом на ввод учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="6c0ca-124">С помощью параметра -EnvironmentName можно пройти проверку подлинности в Azure для Китая или Azure для Германии.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-124">Option '-EnvironmentName' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="6c0ca-125">Пример: Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="6c0ca-125">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="6c0ca-126">Введите электронный адрес и пароль, связанные с вашей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="6c0ca-127">Azure выполняет проверку подлинности и сохраняет учетные данные, а затем закрывает окно.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="6c0ca-128">После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для доступа к ресурсам в подписке и управления ими.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="6c0ca-129">Создание группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6c0ca-129">Create a resource group</span></span>

<span data-ttu-id="6c0ca-130">Теперь, когда все настроено, вы можете создавать ресурсы в Azure с помощью Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-130">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="6c0ca-131">Сначала создайте группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-131">First, create a Resource Group.</span></span> <span data-ttu-id="6c0ca-132">Группы ресурсов в Azure позволяют управлять разными ресурсами, которые вы хотите логически сгруппировать.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-132">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="6c0ca-133">Например, вы можете создать группу ресурсов для приложения или проекта, а затем добавить в эту группу виртуальную машину, базу данных и службу CDN.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-133">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="6c0ca-134">Создайте группу ресурсов с именем MyResourceGroup в регионе Azure "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="6c0ca-134">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="6c0ca-135">Используйте для этого следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6c0ca-135">To do so type the following command:</span></span>

```powershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a><span data-ttu-id="6c0ca-136">Создание виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="6c0ca-136">Create a Windows Virtual Machine</span></span>

<span data-ttu-id="6c0ca-137">Теперь, когда у вас есть группа ресурсов, создайте в ней виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-137">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="6c0ca-138">Чтобы создать виртуальную машину, сначала нужно создать необходимые ресурсы и назначить их в качестве конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-138">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="6c0ca-139">Затем эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-139">Then we can use that configuration to create the VM.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="6c0ca-140">Создание необходимых сетевых ресурсов</span><span class="sxs-lookup"><span data-stu-id="6c0ca-140">Create the required network resources</span></span>

<span data-ttu-id="6c0ca-141">Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-141">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="6c0ca-142">Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-142">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="6c0ca-143">Создайте группу безопасности сети для защиты доступа к общедоступному адресу.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-143">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="6c0ca-144">Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-144">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="6c0ca-145">Создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6c0ca-145">Create the virtual machine</span></span>

<span data-ttu-id="6c0ca-146">Сначала укажите учетные данные для операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-146">First we need a set of credentials for the OS.</span></span>

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="6c0ca-147">Теперь, когда у вас есть необходимые ресурсы, можно создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-147">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="6c0ca-148">На этом шаге создайте объект конфигурации виртуальной машины. Потом эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-148">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="6c0ca-149">Команда `New-AzureRmVM` выводит результаты, когда виртуальная машина создана и готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-149">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="6c0ca-150">Теперь войдите в созданную виртуальную машину Windows Server, используя удаленный рабочий стол и общедоступный IP-адрес этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-150">Now sign in to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="6c0ca-151">Следующая команда отображает общедоступный IP-адрес, созданный в предыдущем скрипте.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-151">The following command displays the public IP address created in the previous script.</span></span>

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="6c0ca-152">Если вы работаете на компьютере Windows, вы можете отобразить IP-адрес, выполнив команду mstsc в командной строке:</span><span class="sxs-lookup"><span data-stu-id="6c0ca-152">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="6c0ca-153">Для входа укажите те же учетные данные (имя пользователя и пароль), которые вы использовали при создании виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-153">Supply the same username/password combination you used when creating the VM to sign in.</span></span>

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="6c0ca-154">Создание виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="6c0ca-154">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="6c0ca-155">Чтобы создать виртуальную машину Linux, сначала нужно создать необходимые ресурсы и назначить их в качестве конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-155">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="6c0ca-156">Затем эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-156">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="6c0ca-157">Предполагается, что вы уже создали группу ресурсов, как описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-157">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="6c0ca-158">Кроме того, вам потребуется открытый ключ SSH `id_rsa.pub` в каталоге формата SSH вашего профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-158">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="6c0ca-159">Создание необходимых сетевых ресурсов</span><span class="sxs-lookup"><span data-stu-id="6c0ca-159">Create the required network resources</span></span>

<span data-ttu-id="6c0ca-160">Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-160">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="6c0ca-161">Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-161">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="6c0ca-162">Создайте группу безопасности сети для защиты доступа к общедоступному адресу.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-162">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="6c0ca-163">Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-163">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="6c0ca-164">Создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6c0ca-164">Create the virtual machine</span></span>

<span data-ttu-id="6c0ca-165">Теперь, когда у вас есть необходимые ресурсы, можно создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-165">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="6c0ca-166">На этом шаге создайте объект конфигурации виртуальной машины. Потом эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-166">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="6c0ca-167">Вы можете войти на созданную виртуальную машину Linux, используя SSH и общедоступный IP-адрес этой виртуальной машины:</span><span class="sxs-lookup"><span data-stu-id="6c0ca-167">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="6c0ca-168">Создание других ресурсов в Azure</span><span class="sxs-lookup"><span data-stu-id="6c0ca-168">Creating other resources in Azure</span></span>

<span data-ttu-id="6c0ca-169">Вы узнали, как создавать группы ресурсов, а также виртуальные машины Linux и Windows Server.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-169">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="6c0ca-170">Но вы также можете создать в Azure много других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-170">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="6c0ca-171">Например, чтобы создать подсистему балансировки нагрузки Azure, которую можно затем связать с новой виртуальной машиной, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6c0ca-171">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="6c0ca-172">Также для своей инфраструктуры вы можете создать новую частную виртуальную сеть, используя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6c0ca-172">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="6c0ca-173">Преимущество Azure и Azure PowerShell заключается в том, что их можно использовать для создания как облачной инфраструктуры, так и управляемых служб платформы.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-173">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="6c0ca-174">Управляемые службы платформы также можно объединять с инфраструктурой, создавая еще более мощные решения.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-174">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="6c0ca-175">Например, используя Azure PowerShell, вы можете создать службу приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-175">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="6c0ca-176">Служба приложений Azure — это управляемая служба платформы, на которой можно размещать веб-приложения, не беспокоясь об инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-176">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="6c0ca-177">Создав службу приложений Azure, вы можете создать два новых веб-приложения Azure с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="6c0ca-177">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="6c0ca-178">Отображение списка развернутых ресурсов</span><span class="sxs-lookup"><span data-stu-id="6c0ca-178">Listing deployed resources</span></span>

<span data-ttu-id="6c0ca-179">Чтобы вывести список ресурсов, работающих в Azure, используйте командлет `Get-AzureRmResource`.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-179">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="6c0ca-180">В следующем примере показаны ресурсы, входящие в созданную группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-180">The following example shows the resources we just created in the new resource group.</span></span>

```powershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="6c0ca-181">Удаление ресурсов</span><span class="sxs-lookup"><span data-stu-id="6c0ca-181">Deleting resources</span></span>

<span data-ttu-id="6c0ca-182">Чтобы очистить учетную запись Azure, необходимо удалить ресурсы, созданные в этом примере.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-182">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="6c0ca-183">Используйте командлеты `Remove-AzureRm*` для удаления ресурсов, которые больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-183">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="6c0ca-184">Чтобы удалить виртуальную машину Windows, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6c0ca-184">To remove the Windows VM we created, using the following command:</span></span>

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="6c0ca-185">Вам будет предложено подтвердить удаление указанных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-185">You will be prompted to confirm that you want to remove the resource.</span></span>

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6c0ca-186">Также можно удалить несколько ресурсов одновременно.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-186">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="6c0ca-187">Например, следующая команда удаляет всю группу ресурсов MyResourceGroup, связанную со всеми примерами в этом руководстве по началу работы.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-187">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="6c0ca-188">Эта команда удаляет группу ресурсов и все ресурсы, которые группа содержит.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-188">This removes the resource group and all of the resources in it.</span></span>

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6c0ca-189">Это может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="6c0ca-189">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="6c0ca-190">Получение примеров</span><span class="sxs-lookup"><span data-stu-id="6c0ca-190">Get samples</span></span>

<span data-ttu-id="6c0ca-191">Дополнительные сведения о способах использования Azure PowerShell см. в примерах популярных сценариев для [виртуальных машин Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [виртуальных машин Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [веб-приложений](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) и [баз данных SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="6c0ca-191">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="6c0ca-192">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6c0ca-192">Next steps</span></span>

* [<span data-ttu-id="6c0ca-193">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c0ca-193">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="6c0ca-194">Управление подписками Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c0ca-194">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="6c0ca-195">Создание субъектов-служб в Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c0ca-195">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="6c0ca-196">Ознакомьтесь с заметками о выпуске, касающимися миграции с более ранней версии: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="6c0ca-196">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="6c0ca-197">Помощь от сообщества:</span><span class="sxs-lookup"><span data-stu-id="6c0ca-197">Get help from the community:</span></span>
  * [<span data-ttu-id="6c0ca-198">Форум Azure на MSDN</span><span class="sxs-lookup"><span data-stu-id="6c0ca-198">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="6c0ca-199">Stackoverflow</span><span class="sxs-lookup"><span data-stu-id="6c0ca-199">stackoverflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
