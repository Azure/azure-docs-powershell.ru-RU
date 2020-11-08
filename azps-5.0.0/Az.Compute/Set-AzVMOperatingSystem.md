---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247493"
---
# <span data-ttu-id="bf188-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bf188-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="bf188-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf188-102">SYNOPSIS</span></span>
<span data-ttu-id="bf188-103">Настройка свойств операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf188-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="bf188-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf188-104">SYNTAX</span></span>

### <span data-ttu-id="bf188-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf188-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf188-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="bf188-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf188-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="bf188-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf188-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="bf188-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf188-109">Linux</span><span class="sxs-lookup"><span data-stu-id="bf188-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf188-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf188-110">DESCRIPTION</span></span>
<span data-ttu-id="bf188-111">Командлет **Set-AzVMOperatingSystem** задает свойства операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf188-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="bf188-112">Вы можете задать учетные данные для входа, имя компьютера и тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bf188-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="bf188-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf188-113">EXAMPLES</span></span>

### <span data-ttu-id="bf188-114">Пример 1: Настройка свойств операционной системы для новых виртуальных машин</span><span class="sxs-lookup"><span data-stu-id="bf188-114">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="bf188-115">Первая команда преобразует пароль в защищенную строку, а затем сохраняет его в переменной $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="bf188-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="bf188-116">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="bf188-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="bf188-117">Вторая команда создает учетные данные пользователя FullerP и пароль, хранящийся в $SecurePassword, а затем сохраняет учетные данные в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="bf188-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="bf188-118">Для получения дополнительных сведений введите `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="bf188-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="bf188-119">Третья команда получает группу доступности с именем AvailabilitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bf188-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="bf188-120">Четвертая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bf188-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bf188-121">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bf188-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bf188-122">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bf188-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="bf188-123">Следующие четыре команды назначают значения переменных для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="bf188-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="bf188-124">Так как вы можете указать эти строки непосредственно в команде **Set-AzVMOperatingSystem** , этот подход используется только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf188-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="bf188-125">Однако вы можете использовать такой подход в сценариях.</span><span class="sxs-lookup"><span data-stu-id="bf188-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="bf188-126">Последняя команда задает свойства операционной системы для виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bf188-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="bf188-127">В команде используются учетные данные, хранящиеся в $Credential.</span><span class="sxs-lookup"><span data-stu-id="bf188-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="bf188-128">Команда использует переменные, назначенные в предыдущих командах, для некоторых параметров.</span><span class="sxs-lookup"><span data-stu-id="bf188-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="bf188-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf188-129">PARAMETERS</span></span>

### <span data-ttu-id="bf188-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="bf188-130">-ComputerName</span></span>
<span data-ttu-id="bf188-131">Указывает имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="bf188-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="bf188-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="bf188-132">-Credential</span></span>
<span data-ttu-id="bf188-133">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="bf188-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="bf188-134">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="bf188-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="bf188-135">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="bf188-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="bf188-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="bf188-136">-CustomData</span></span>
<span data-ttu-id="bf188-137">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="bf188-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="bf188-138">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bf188-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="bf188-139">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="bf188-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="bf188-140">**Примечание. не следует передавать секреты и пароли в свойстве customData**</span><span class="sxs-lookup"><span data-stu-id="bf188-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="bf188-141">Это свойство невозможно обновить после создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf188-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="bf188-142">пользовательские учетные записи передаются в ВМ для сохранения в файле. Дополнительные сведения можно найти [в разделе Пользовательские данные на виртуальных машинах Azure](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) .</span><span class="sxs-lookup"><span data-stu-id="bf188-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="bf188-143">Если вы используете облачную инициализацию для виртуальной машины Linux, ознакомьтесь со сведениями о [настройке виртуальной машины Linux во время создания с помощью облака-init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) .</span><span class="sxs-lookup"><span data-stu-id="bf188-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

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

### <span data-ttu-id="bf188-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf188-144">-DefaultProfile</span></span>
<span data-ttu-id="bf188-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf188-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf188-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="bf188-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="bf188-147">Указывает на то, что этот командлет отключает проверку подлинности пароля.</span><span class="sxs-lookup"><span data-stu-id="bf188-147">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="bf188-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="bf188-148">-DisableVMAgent</span></span>
<span data-ttu-id="bf188-149">Отключите агент подготовки ВМ.</span><span class="sxs-lookup"><span data-stu-id="bf188-149">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="bf188-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bf188-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="bf188-151">Указывает на то, что этот командлет включает функцию автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="bf188-151">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="bf188-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="bf188-152">-Linux</span></span>
<span data-ttu-id="bf188-153">Указывает, что тип операционной системы — Linux.</span><span class="sxs-lookup"><span data-stu-id="bf188-153">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="bf188-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="bf188-154">-PatchMode</span></span>
<span data-ttu-id="bf188-155">Задает режим исправлений на виртуальной машине IaaS.</span><span class="sxs-lookup"><span data-stu-id="bf188-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="bf188-156">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bf188-156">Possible values are:</span></span><br>
<span data-ttu-id="bf188-157">**Вручную** — вы управляете приложением патчей для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf188-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="bf188-158">Это можно сделать, применяя пакеты исправлений вручную в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bf188-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="bf188-159">В этом режиме автоматическое обновление отключено. Свойство WindowsConfiguration. enableAutomaticUpdates должно быть ложным</span><span class="sxs-lookup"><span data-stu-id="bf188-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="bf188-160">**AutomaticByOS** — виртуальная машина будет автоматически ОБНОВЛЯТЬСЯ операционной системой.</span><span class="sxs-lookup"><span data-stu-id="bf188-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="bf188-161">Свойство WindowsConfiguration. enableAutomaticUpdates должно быть истинным.</span><span class="sxs-lookup"><span data-stu-id="bf188-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="bf188-162">**AutomaticByPlatform** — виртуальная машина будет автоматически ОБНОВЛЯТЬСЯ операционной системой.</span><span class="sxs-lookup"><span data-stu-id="bf188-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="bf188-163">Свойства provisionVMAgent и WindowsConfiguration. enableAutomaticUpdates должны быть истинными</span><span class="sxs-lookup"><span data-stu-id="bf188-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

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

### <span data-ttu-id="bf188-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="bf188-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="bf188-165">Указывает на то, что для параметров требуется установка агента виртуальной машины на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bf188-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="bf188-166">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="bf188-166">-TimeZone</span></span>
<span data-ttu-id="bf188-167">Указывает часовой пояс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf188-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="bf188-168">Например, \" тихоокеанское время \" .</span><span class="sxs-lookup"><span data-stu-id="bf188-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="bf188-169">Возможные значения могут быть [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) значениями из часовых поясов, возвращаемых [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="bf188-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="bf188-170">-VM</span><span class="sxs-lookup"><span data-stu-id="bf188-170">-VM</span></span>
<span data-ttu-id="bf188-171">Указывает локальный объект виртуальной машины, на котором нужно задать свойства операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bf188-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="bf188-172">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="bf188-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="bf188-173">Создайте объект виртуальной машины с помощью командлета New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="bf188-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="bf188-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="bf188-174">-Windows</span></span>
<span data-ttu-id="bf188-175">Указывает на то, что тип операционной системы — Windows.</span><span class="sxs-lookup"><span data-stu-id="bf188-175">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="bf188-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="bf188-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="bf188-177">Задает универсальный код ресурса (URI) для сертификата WinRM.</span><span class="sxs-lookup"><span data-stu-id="bf188-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="bf188-178">Это необходимо для хранения в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="bf188-178">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="bf188-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="bf188-179">-WinRMHttp</span></span>
<span data-ttu-id="bf188-180">Указывает, что эта операционная система использует HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="bf188-180">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="bf188-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="bf188-181">-WinRMHttps</span></span>
<span data-ttu-id="bf188-182">Указывает, что эта операционная система использует HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="bf188-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="bf188-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf188-183">CommonParameters</span></span>
<span data-ttu-id="bf188-184">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf188-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf188-185">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf188-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf188-186">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf188-186">INPUTS</span></span>

### <span data-ttu-id="bf188-187">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bf188-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="bf188-188">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bf188-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bf188-189">System. String</span><span class="sxs-lookup"><span data-stu-id="bf188-189">System.String</span></span>

### <span data-ttu-id="bf188-190">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="bf188-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="bf188-191">System. URI</span><span class="sxs-lookup"><span data-stu-id="bf188-191">System.Uri</span></span>

## <span data-ttu-id="bf188-192">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf188-192">OUTPUTS</span></span>

### <span data-ttu-id="bf188-193">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bf188-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bf188-194">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf188-194">NOTES</span></span>

## <span data-ttu-id="bf188-195">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf188-195">RELATED LINKS</span></span>

[<span data-ttu-id="bf188-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf188-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bf188-197">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="bf188-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


