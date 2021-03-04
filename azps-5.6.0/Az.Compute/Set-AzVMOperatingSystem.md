---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990447"
---
# <span data-ttu-id="e1e74-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e1e74-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="e1e74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1e74-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e74-103">Задает свойства операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e1e74-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="e1e74-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1e74-104">SYNTAX</span></span>

### <span data-ttu-id="e1e74-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1e74-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e74-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="e1e74-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e74-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="e1e74-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e74-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="e1e74-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e74-109">Linux</span><span class="sxs-lookup"><span data-stu-id="e1e74-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1e74-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1e74-110">DESCRIPTION</span></span>
<span data-ttu-id="e1e74-111">**Cmdlet Set-AzVMOperatingSystem** задает свойства операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e1e74-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="e1e74-112">Вы можете указать учетные данные для входа, имя компьютера и тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e1e74-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="e1e74-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1e74-113">EXAMPLES</span></span>

### <span data-ttu-id="e1e74-114">Пример 1. Настройка свойств операционной системы для новой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="e1e74-114">Example 1: Set operating system properties for a new virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="e1e74-115">Первая команда преобразует пароль в безопасную строку, а затем сохраняет его в переменной $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="e1e74-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="e1e74-116">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e1e74-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="e1e74-117">Вторая команда создает учетные данные для пользователя FullerP и пароль, хранимый в $SecurePassword, а затем сохраняет учетные данные в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="e1e74-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="e1e74-118">Для получения дополнительных сведений введите `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="e1e74-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="e1e74-119">Третья команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в $AvailabilitySet переменной.</span><span class="sxs-lookup"><span data-stu-id="e1e74-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e1e74-120">Четвертая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="e1e74-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e1e74-121">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e1e74-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e1e74-122">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e1e74-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e1e74-123">Следующие четыре команды присваивают значения переменным, которые нужно использовать в следующей команде:</span><span class="sxs-lookup"><span data-stu-id="e1e74-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="e1e74-124">Поскольку эти строки можно указать непосредственно в команде **Set-AzVMOperatingSystem,** этот подход используется только для учитаемости.</span><span class="sxs-lookup"><span data-stu-id="e1e74-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="e1e74-125">Однако в сценариях можно использовать такой подход.</span><span class="sxs-lookup"><span data-stu-id="e1e74-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="e1e74-126">Конечная команда задает свойства операционной системы для виртуальной машины, храняной в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e1e74-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e1e74-127">Для этой команды используются учетные данные, хранимые в $Credential.</span><span class="sxs-lookup"><span data-stu-id="e1e74-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="e1e74-128">В этой команде используются переменные, заданные в предыдущих командах для некоторых параметров.</span><span class="sxs-lookup"><span data-stu-id="e1e74-128">The command uses variables assigned in previous commands for some parameters.</span></span>

### <span data-ttu-id="e1e74-129">Пример 2. Настройка свойств операционной системы для новой виртуальной машины с включенным исправлением</span><span class="sxs-lookup"><span data-stu-id="e1e74-129">Example 2: Set operating system properties for a new virtual machine with hot patching enabled</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

<span data-ttu-id="e1e74-130">Первая команда преобразует пароль в безопасную строку, а затем сохраняет его в переменной $SecurePassword безопасности.</span><span class="sxs-lookup"><span data-stu-id="e1e74-130">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="e1e74-131">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e1e74-131">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="e1e74-132">Вторая команда создает учетные данные для пользователя FullerP и пароль, хранимые в $SecurePassword, а затем сохраняет учетные данные в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="e1e74-132">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="e1e74-133">Для получения дополнительных сведений введите `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="e1e74-133">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="e1e74-134">Третья команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в $AvailabilitySet переменной.</span><span class="sxs-lookup"><span data-stu-id="e1e74-134">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e1e74-135">Четвертая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="e1e74-135">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e1e74-136">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e1e74-136">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e1e74-137">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e1e74-137">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e1e74-138">Следующие четыре команды присваивают значения переменным, которые нужно использовать в следующей команде:</span><span class="sxs-lookup"><span data-stu-id="e1e74-138">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="e1e74-139">Поскольку эти строки можно указать непосредственно в команде **Set-AzVMOperatingSystem,** этот подход используется только для учитаемости.</span><span class="sxs-lookup"><span data-stu-id="e1e74-139">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="e1e74-140">Однако в сценариях можно использовать такой подход.</span><span class="sxs-lookup"><span data-stu-id="e1e74-140">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="e1e74-141">Конечная команда задает свойства операционной системы для виртуальной машины, храняной в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e1e74-141">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e1e74-142">Для этой команды используются учетные данные, хранимые в $Credential.</span><span class="sxs-lookup"><span data-stu-id="e1e74-142">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="e1e74-143">В этой команде используются переменные, заданные в предыдущих командах для некоторых параметров.</span><span class="sxs-lookup"><span data-stu-id="e1e74-143">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="e1e74-144">Эта команда включает "Hotpatching" на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e1e74-144">The command enables Hotpatching on the virtual machine.</span></span>

### <span data-ttu-id="e1e74-145">Пример 3. Настройка свойств операционной системы для новой виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="e1e74-145">Example 3: Set operating system properties for a new Linux virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="e1e74-146">Первая команда преобразует пароль в безопасную строку, а затем сохраняет его в переменной $SecurePassword безопасности.</span><span class="sxs-lookup"><span data-stu-id="e1e74-146">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="e1e74-147">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e1e74-147">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="e1e74-148">Вторая команда создает учетные данные для пользователя FullerP и пароль, хранимые в $SecurePassword, а затем сохраняет учетные данные в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="e1e74-148">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="e1e74-149">Для получения дополнительных сведений введите `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="e1e74-149">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="e1e74-150">Третья команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в $AvailabilitySet переменной.</span><span class="sxs-lookup"><span data-stu-id="e1e74-150">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e1e74-151">Четвертая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="e1e74-151">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e1e74-152">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e1e74-152">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e1e74-153">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e1e74-153">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e1e74-154">Следующие две команды присваивают значения переменным, которые нужно использовать в следующей команде:</span><span class="sxs-lookup"><span data-stu-id="e1e74-154">The next two commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="e1e74-155">Конечная команда задает свойства операционной системы для виртуальной машины, храняной в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e1e74-155">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e1e74-156">Для этой команды используются учетные данные, хранимые в $Credential.</span><span class="sxs-lookup"><span data-stu-id="e1e74-156">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="e1e74-157">В этой команде используются переменные, заданные в предыдущих командах для некоторых параметров.</span><span class="sxs-lookup"><span data-stu-id="e1e74-157">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="e1e74-158">Эта команда задает для режима исправления на виртуальной машине значение AutomaticByPlatform.</span><span class="sxs-lookup"><span data-stu-id="e1e74-158">The command sets the patch mode value on the virtual machine to "AutomaticByPlatform".</span></span>

## <span data-ttu-id="e1e74-159">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1e74-159">PARAMETERS</span></span>

### <span data-ttu-id="e1e74-160">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="e1e74-160">-ComputerName</span></span>
<span data-ttu-id="e1e74-161">Указывает имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="e1e74-161">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="e1e74-162">-Credential</span><span class="sxs-lookup"><span data-stu-id="e1e74-162">-Credential</span></span>
<span data-ttu-id="e1e74-163">Указывает имя пользователя и пароль виртуальной машины в качестве **объекта PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="e1e74-163">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="e1e74-164">Для получения учетных данных используйте Get-Credential управления.</span><span class="sxs-lookup"><span data-stu-id="e1e74-164">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="e1e74-165">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="e1e74-165">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="e1e74-166">-CustomData</span><span class="sxs-lookup"><span data-stu-id="e1e74-166">-CustomData</span></span>
<span data-ttu-id="e1e74-167">Указывает строку, которая будет передана виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e1e74-167">Specifies a string to be passed to the virtual machine.</span></span> <span data-ttu-id="e1e74-168">Дополнительные сведения см. [в подмногах Azure Custom Data (Настраиваемые данные).](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)</span><span class="sxs-lookup"><span data-stu-id="e1e74-168">For more information see [Custom Data on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span></span>
<span data-ttu-id="e1e74-169">**Примечание. Хранить конфиденциальную информацию в пользовательских данных не рекомендуется.**</span><span class="sxs-lookup"><span data-stu-id="e1e74-169">**Note: It is not recommended to store sensitive information in custom data.**</span></span>


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

### <span data-ttu-id="e1e74-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e74-170">-DefaultProfile</span></span>
<span data-ttu-id="e1e74-171">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1e74-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1e74-172">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="e1e74-172">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="e1e74-173">Указывает на то, что этот cmdlet отключает проверку подлинности паролем.</span><span class="sxs-lookup"><span data-stu-id="e1e74-173">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="e1e74-174">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="e1e74-174">-DisableVMAgent</span></span>
<span data-ttu-id="e1e74-175">Отключить агент VM для предоставления.</span><span class="sxs-lookup"><span data-stu-id="e1e74-175">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="e1e74-176">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="e1e74-176">-EnableAutoUpdate</span></span>
<span data-ttu-id="e1e74-177">Указывает на то, что этот cmdlet включает автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="e1e74-177">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="e1e74-178">-EnableHotpatching</span><span class="sxs-lookup"><span data-stu-id="e1e74-178">-EnableHotpatching</span></span>
<span data-ttu-id="e1e74-179">Позволяет клиентам исправление своих VMs Azure без необходимости перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="e1e74-179">Enables customers to patch their Azure VMs without requiring a reboot.</span></span> <span data-ttu-id="e1e74-180">Для enableHotpatching для "provisionVMAgent" должно быть задано истинное, а для исправления должно быть задано "AutomaticByPlatform".</span><span class="sxs-lookup"><span data-stu-id="e1e74-180">For enableHotpatching, the 'provisionVMAgent' must be set to true and 'patchMode' must be set to 'AutomaticByPlatform'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1e74-181">-Linux</span><span class="sxs-lookup"><span data-stu-id="e1e74-181">-Linux</span></span>
<span data-ttu-id="e1e74-182">Указывает на то, что тип операционной системы — Linux.</span><span class="sxs-lookup"><span data-stu-id="e1e74-182">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="e1e74-183">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="e1e74-183">-PatchMode</span></span>
<span data-ttu-id="e1e74-184">Определяет режим исправления в гостях на виртуальной машине IaaS.</span><span class="sxs-lookup"><span data-stu-id="e1e74-184">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="e1e74-185">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="e1e74-185">Possible values are:</span></span><br>
<span data-ttu-id="e1e74-186">**Вручную** — вы управляете применением исправлений на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e1e74-186">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="e1e74-187">Для этого нужно вручную применить исправления внутри VM-управления.</span><span class="sxs-lookup"><span data-stu-id="e1e74-187">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="e1e74-188">В этом режиме автоматические обновления отключены. свойство WindowsConfiguration.enableAutomaticUpdates должно быть ложным.</span><span class="sxs-lookup"><span data-stu-id="e1e74-188">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="e1e74-189">**AutomaticByOS** — виртуальная машинка будет автоматически обновлена операционной системами.</span><span class="sxs-lookup"><span data-stu-id="e1e74-189">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="e1e74-190">Свойство WindowsConfiguration.enableAutomaticUpdates должно быть истинным.</span><span class="sxs-lookup"><span data-stu-id="e1e74-190">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="e1e74-191">**AutomaticByPlatform** — виртуальная машину будет автоматически обновляться операционной системами.</span><span class="sxs-lookup"><span data-stu-id="e1e74-191">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="e1e74-192">Свойства provisionVMAgent и WindowsConfiguration.enableAutomaticUpdates должны быть истинными.</span><span class="sxs-lookup"><span data-stu-id="e1e74-192">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1e74-193">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="e1e74-193">-ProvisionVMAgent</span></span>
<span data-ttu-id="e1e74-194">Указывает на то, что в параметрах на виртуальной машине должен быть установлен агент виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e1e74-194">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="e1e74-195">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="e1e74-195">-TimeZone</span></span>
<span data-ttu-id="e1e74-196">Определяет часовой пояс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e1e74-196">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="e1e74-197">Например, по \" тихоокеанскому \" времени.</span><span class="sxs-lookup"><span data-stu-id="e1e74-197">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="e1e74-198">Возможные значения могут [быть](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id из часовых поясов, возвращаемых [timeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="e1e74-198">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="e1e74-199">-VM</span><span class="sxs-lookup"><span data-stu-id="e1e74-199">-VM</span></span>
<span data-ttu-id="e1e74-200">Определяет объект локальной виртуальной машины, для которого нужно настроить свойства операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e1e74-200">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="e1e74-201">Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..</span><span class="sxs-lookup"><span data-stu-id="e1e74-201">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="e1e74-202">Создайте объект виртуальной машины с помощью New-AzVMConfig..</span><span class="sxs-lookup"><span data-stu-id="e1e74-202">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="e1e74-203">-Windows</span><span class="sxs-lookup"><span data-stu-id="e1e74-203">-Windows</span></span>
<span data-ttu-id="e1e74-204">Указывает на то, что типом операционной системы является Windows.</span><span class="sxs-lookup"><span data-stu-id="e1e74-204">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="e1e74-205">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="e1e74-205">-WinRMCertificateUrl</span></span>
<span data-ttu-id="e1e74-206">Определяет URI сертификата WinRM.</span><span class="sxs-lookup"><span data-stu-id="e1e74-206">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="e1e74-207">Он должен храниться в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="e1e74-207">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="e1e74-208">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="e1e74-208">-WinRMHttp</span></span>
<span data-ttu-id="e1e74-209">Указывает на то, что в этой операционной системе используется winRM HTTP.</span><span class="sxs-lookup"><span data-stu-id="e1e74-209">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="e1e74-210">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="e1e74-210">-WinRMHttps</span></span>
<span data-ttu-id="e1e74-211">Указывает на то, что в этой операционной системе используется winRM HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e1e74-211">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="e1e74-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e74-212">CommonParameters</span></span>
<span data-ttu-id="e1e74-213">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e74-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e74-214">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1e74-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e74-215">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1e74-215">INPUTS</span></span>

### <span data-ttu-id="e1e74-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="e1e74-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e1e74-217">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e1e74-217">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e1e74-218">System.String</span><span class="sxs-lookup"><span data-stu-id="e1e74-218">System.String</span></span>

### <span data-ttu-id="e1e74-219">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="e1e74-219">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="e1e74-220">System.Uri</span><span class="sxs-lookup"><span data-stu-id="e1e74-220">System.Uri</span></span>

## <span data-ttu-id="e1e74-221">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1e74-221">OUTPUTS</span></span>

### <span data-ttu-id="e1e74-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="e1e74-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e1e74-223">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1e74-223">NOTES</span></span>

## <span data-ttu-id="e1e74-224">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1e74-224">RELATED LINKS</span></span>

[<span data-ttu-id="e1e74-225">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e1e74-225">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e1e74-226">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e1e74-226">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


