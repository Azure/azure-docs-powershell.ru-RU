---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393943"
---
# <span data-ttu-id="85404-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="85404-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="85404-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85404-102">SYNOPSIS</span></span>
<span data-ttu-id="85404-103">Задает свойства операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="85404-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="85404-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85404-104">SYNTAX</span></span>

### <span data-ttu-id="85404-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85404-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85404-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="85404-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85404-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="85404-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85404-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="85404-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85404-109">Linux</span><span class="sxs-lookup"><span data-stu-id="85404-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85404-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85404-110">DESCRIPTION</span></span>
<span data-ttu-id="85404-111">**Cmdlet Set-AzVMOperatingSystem** задает свойства операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="85404-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="85404-112">Вы можете указать учетные данные для входа, имя компьютера и тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="85404-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="85404-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85404-113">EXAMPLES</span></span>

### <span data-ttu-id="85404-114">Пример 1. Настройка свойств операционной системы для новых виртуальных машин</span><span class="sxs-lookup"><span data-stu-id="85404-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="85404-115">Первая команда преобразует пароль в безопасную строку, а затем сохраняет его в переменной $SecurePassword безопасности.</span><span class="sxs-lookup"><span data-stu-id="85404-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="85404-116">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="85404-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="85404-117">Вторая команда создает учетные данные для пользователя FullerP и пароль, хранимый в $SecurePassword, а затем сохраняет учетные данные в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="85404-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="85404-118">Для получения дополнительных сведений введите `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="85404-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="85404-119">Третья команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в $AvailabilitySet переменной.</span><span class="sxs-lookup"><span data-stu-id="85404-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="85404-120">Четвертая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="85404-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="85404-121">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="85404-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="85404-122">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="85404-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="85404-123">Следующие четыре команды присваивают значения переменным, которые нужно использовать в следующей команде:</span><span class="sxs-lookup"><span data-stu-id="85404-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="85404-124">Поскольку эти строки можно указать непосредственно в команде **Set-AzVMOperatingSystem,** этот подход используется только для учитаемости.</span><span class="sxs-lookup"><span data-stu-id="85404-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="85404-125">Однако в сценариях можно использовать такой подход.</span><span class="sxs-lookup"><span data-stu-id="85404-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="85404-126">Конечная команда задает свойства операционной системы для виртуальной машины, храняной в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="85404-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="85404-127">Для этой команды используются учетные данные, хранимые в $Credential.</span><span class="sxs-lookup"><span data-stu-id="85404-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="85404-128">Для некоторых параметров в команде используются переменные, заданные в предыдущих командах.</span><span class="sxs-lookup"><span data-stu-id="85404-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="85404-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85404-129">PARAMETERS</span></span>

### <span data-ttu-id="85404-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="85404-130">-ComputerName</span></span>
<span data-ttu-id="85404-131">Указывает имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="85404-131">Specifies the name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="85404-132">-Credential</span></span>
<span data-ttu-id="85404-133">Указывает имя пользователя и пароль виртуальной машины в качестве **объекта PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="85404-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="85404-134">Для получения учетных данных используйте Get-Credential управления.</span><span class="sxs-lookup"><span data-stu-id="85404-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="85404-135">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="85404-135">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="85404-136">-CustomData</span></span>
<span data-ttu-id="85404-137">Указывает строку пользовательских данных с кодом base-64.</span><span class="sxs-lookup"><span data-stu-id="85404-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="85404-138">Он декодироваться в двоичный массив, сохраненный в файле на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="85404-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="85404-139">Максимальная длина двоичного массива составляет 65 535 тол.</span><span class="sxs-lookup"><span data-stu-id="85404-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="85404-140">**Примечание. Не передавать секрет и пароли в настраиваемом свойствеData**</span><span class="sxs-lookup"><span data-stu-id="85404-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="85404-141">Это свойство невозможно обновить после создания VM-объекта.</span><span class="sxs-lookup"><span data-stu-id="85404-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="85404-142">CustomData передается в VM для с хранения в файле. Дополнительные сведения см. в дополнительных сведениях о пользовательских данных [в VMs Azure](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span><span class="sxs-lookup"><span data-stu-id="85404-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="85404-143">Чтобы узнать, как использовать cloud-init для Linux VM, см. использование [cloud-init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) для настройки Linux VM во время создания</span><span class="sxs-lookup"><span data-stu-id="85404-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85404-144">-DefaultProfile</span></span>
<span data-ttu-id="85404-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85404-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85404-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="85404-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="85404-147">Указывает на то, что этот cmdlet отключает проверку подлинности паролем.</span><span class="sxs-lookup"><span data-stu-id="85404-147">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="85404-148">-DisableVMAgent</span></span>
<span data-ttu-id="85404-149">Отключить агент VM для предоставления.</span><span class="sxs-lookup"><span data-stu-id="85404-149">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85404-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="85404-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="85404-151">Указывает на то, что этот cmdlet включает автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="85404-151">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="85404-152">-Linux</span></span>
<span data-ttu-id="85404-153">Указывает на то, что тип операционной системы — Linux.</span><span class="sxs-lookup"><span data-stu-id="85404-153">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="85404-154">-PatchMode</span></span>
<span data-ttu-id="85404-155">Определяет режим исправления в гостях на виртуальной машине IaaS.</span><span class="sxs-lookup"><span data-stu-id="85404-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="85404-156">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="85404-156">Possible values are:</span></span><br>
<span data-ttu-id="85404-157">**Вручную** — вы управляете применением исправлений на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="85404-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="85404-158">Для этого нужно вручную применить исправления внутри VM-управления.</span><span class="sxs-lookup"><span data-stu-id="85404-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="85404-159">В этом режиме автоматические обновления отключены. свойство WindowsConfiguration.enableAutomaticUpdates должно иметь ошибку</span><span class="sxs-lookup"><span data-stu-id="85404-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="85404-160">**AutomaticByOS** — виртуальная машинка будет автоматически обновлена операционной системами.</span><span class="sxs-lookup"><span data-stu-id="85404-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="85404-161">Свойство WindowsConfiguration.enableAutomaticUpdates должно быть истинным.</span><span class="sxs-lookup"><span data-stu-id="85404-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="85404-162">**AutomaticByPlatform** — виртуальная машину будет автоматически обновляться операционной системами.</span><span class="sxs-lookup"><span data-stu-id="85404-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="85404-163">Свойства provisionVMAgent и WindowsConfiguration.enableAutomaticUpdates должны быть истинными.</span><span class="sxs-lookup"><span data-stu-id="85404-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="85404-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="85404-165">Указывает на то, что в параметрах на виртуальной машине должен быть установлен агент виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="85404-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-166">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="85404-166">-TimeZone</span></span>
<span data-ttu-id="85404-167">Определяет часовой пояс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="85404-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="85404-168">Например, по \" тихоокеанскому времени. \"</span><span class="sxs-lookup"><span data-stu-id="85404-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="85404-169">Возможные значения могут [быть](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id из часовых поясов, возвращаемых [timeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="85404-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-170">-VM</span><span class="sxs-lookup"><span data-stu-id="85404-170">-VM</span></span>
<span data-ttu-id="85404-171">Определяет объект локальной виртуальной машины, для которого нужно настроить свойства операционной системы.</span><span class="sxs-lookup"><span data-stu-id="85404-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="85404-172">Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..</span><span class="sxs-lookup"><span data-stu-id="85404-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="85404-173">Создайте объект виртуальной машины с помощью New-AzVMConfig..</span><span class="sxs-lookup"><span data-stu-id="85404-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="85404-174">-Windows</span></span>
<span data-ttu-id="85404-175">Указывает на то, что типом операционной системы является Windows.</span><span class="sxs-lookup"><span data-stu-id="85404-175">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="85404-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="85404-177">URI сертификата WinRM.</span><span class="sxs-lookup"><span data-stu-id="85404-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="85404-178">Он должен храниться в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="85404-178">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="85404-179">-WinRMHttp</span></span>
<span data-ttu-id="85404-180">Указывает на то, что в этой операционной системе используется winRM HTTP.</span><span class="sxs-lookup"><span data-stu-id="85404-180">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="85404-181">-WinRMHttps</span></span>
<span data-ttu-id="85404-182">Указывает на то, что в этой операционной системе используется winRM HTTPS.</span><span class="sxs-lookup"><span data-stu-id="85404-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85404-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85404-183">CommonParameters</span></span>
<span data-ttu-id="85404-184">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85404-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85404-185">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85404-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85404-186">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85404-186">INPUTS</span></span>

### <span data-ttu-id="85404-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="85404-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="85404-188">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="85404-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="85404-189">System.String</span><span class="sxs-lookup"><span data-stu-id="85404-189">System.String</span></span>

### <span data-ttu-id="85404-190">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="85404-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="85404-191">System.Uri</span><span class="sxs-lookup"><span data-stu-id="85404-191">System.Uri</span></span>

## <span data-ttu-id="85404-192">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85404-192">OUTPUTS</span></span>

### <span data-ttu-id="85404-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="85404-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="85404-194">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85404-194">NOTES</span></span>

## <span data-ttu-id="85404-195">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85404-195">RELATED LINKS</span></span>

[<span data-ttu-id="85404-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="85404-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="85404-197">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="85404-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

