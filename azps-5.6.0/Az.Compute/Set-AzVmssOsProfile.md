---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 046812a0339a0dd33df140f29e00ec8b882c91cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958888"
---
# <span data-ttu-id="a0ce8-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="a0ce8-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="a0ce8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ce8-103">Задает свойства профиля операционной системы VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="a0ce8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a0ce8-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0ce8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0ce8-105">DESCRIPTION</span></span>
<span data-ttu-id="a0ce8-106">Для свойства профиля виртуальной машины **Set-AzVmssOsProfile** задаются свойства профиля виртуальной машины (Scale Set).</span><span class="sxs-lookup"><span data-stu-id="a0ce8-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="a0ce8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a0ce8-107">EXAMPLES</span></span>

### <span data-ttu-id="a0ce8-108">Пример 1. Настройка свойств профиля операционной системы для VMSS</span><span class="sxs-lookup"><span data-stu-id="a0ce8-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="a0ce8-109">Эта команда задает свойства профиля операционной системы для виртуальных машин, которые относятся к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="a0ce8-110">Эта команда задает префикс имени компьютера для всех экземпляров виртуальной машины в VMSS для проверки и задает имя пользователя и пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="a0ce8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0ce8-111">PARAMETERS</span></span>

### <span data-ttu-id="a0ce8-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="a0ce8-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="a0ce8-113">Определяет объект несмежного содержимого.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="a0ce8-114">С помощью Add-AzVMAdditionalUnattendContent можно создать объект.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="a0ce8-115">-AdminPassword</span></span>
<span data-ttu-id="a0ce8-116">Пароль администратора, который будет применяться для всех экземпляров виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="a0ce8-117">-AdminUsername</span></span>
<span data-ttu-id="a0ce8-118">Указывает имя учетной записи администратора, которая будет применяться для всех экземпляров виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="a0ce8-119">**Ограничение только для Windows:** Не может закончиться \" .\"</span><span class="sxs-lookup"><span data-stu-id="a0ce8-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="a0ce8-120">**Деостановимые значения** \" \"администратор, \" \" администратор, \" \" пользователь, \" \" пользователь1, \" \" проверка, \" \" пользователь2, \" \" тест1, \" \" пользователь3, \" \" администратор1, \" \" 1, \" 123, \" a , \" \" \" actuser, \" \" adm, \" \" \" admin2, \" aspnet, aspnet, \" \" \" backup, \" \" \" \" \" console, david, \" guest, \" \" \" \" owner, \" \" owner, root, \" \" server, \" sql, \" support , \" \" \" \" support_388945a0, \" sys, \" \" test2 , \" \" \" test3, \" \" user4, \" user5 \" .</span><span class="sxs-lookup"><span data-stu-id="a0ce8-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="a0ce8-121">**Минимальная длина (Linux):** 1 знак</span><span class="sxs-lookup"><span data-stu-id="a0ce8-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="a0ce8-122">**Максимальная длина (Linux):** 64 знака</span><span class="sxs-lookup"><span data-stu-id="a0ce8-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="a0ce8-123">**Максимальная длина (Windows):** 20 символов</span><span class="sxs-lookup"><span data-stu-id="a0ce8-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="a0ce8-124">Корневой доступ к Linux VM см. в теме "Использование корневых привилегий на виртуальных машинах [Linux" в Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="a0ce8-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="a0ce8-125">Список встроенных пользователей системы на Linux, которые не следует использовать в этом поле, см. в поле "Выбор имен пользователей [для Linux" в Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="a0ce8-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="a0ce8-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="a0ce8-127">Указывает префикс имени компьютера для всех экземпляров виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="a0ce8-128">Имена компьютеров должны иметь длину от 1 до 15 знаков.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-128">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="a0ce8-129">-CustomData</span></span>
<span data-ttu-id="a0ce8-130">Указывает строку пользовательских данных с кодом base-64.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="a0ce8-131">Он декодироваться в двоичный массив, сохраненный в файле на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="a0ce8-132">Максимальная длина двоичного массива составляет 65 535 тол.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="a0ce8-133">Чтобы узнать, как использовать cloud-init для своего VM-решения, см. в этой теме использование cloud-init для настройки [VM-решения Linux во](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)время создания.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="a0ce8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ce8-134">-DefaultProfile</span></span>
<span data-ttu-id="a0ce8-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0ce8-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="a0ce8-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="a0ce8-137">Указывает на то, что этот cmdlet отключает проверку подлинности паролем.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-137">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-138">-Listener</span><span class="sxs-lookup"><span data-stu-id="a0ce8-138">-Listener</span></span>
<span data-ttu-id="a0ce8-139">Указывает, Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="a0ce8-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="a0ce8-140">Это позволит использовать удаленные Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="a0ce8-141">Для создания Add-AzVmssWinRMListener можно использовать Add-AzVmssWinRMListener.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="a0ce8-142">-PublicKey</span></span>
<span data-ttu-id="a0ce8-143">Указывает объект открытого ключа Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="a0ce8-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="a0ce8-144">Для создания объекта Add-AzVMSshPublicKey можно использовать Add-AzVMSshPublicKey.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-145">-Секретная</span><span class="sxs-lookup"><span data-stu-id="a0ce8-145">-Secret</span></span>
<span data-ttu-id="a0ce8-146">Определяет секрет объекта, который содержит ссылки на сертификаты, которые нужно разместить на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="a0ce8-147">С помощью Add-AzVmssSecret можно создать объект секретов.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="a0ce8-148">-TimeZone</span></span>
<span data-ttu-id="a0ce8-149">Определяет часовой пояс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="a0ce8-150">Например, по \" тихоокеанскому \" времени.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="a0ce8-151">Возможные значения могут [быть](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id из часовых поясов, возвращаемых [timeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="a0ce8-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0ce8-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a0ce8-153">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="a0ce8-154">Для создания объекта New-AzVmssConfig можно использовать New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="a0ce8-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="a0ce8-156">Указывает, включены ли на виртуальных машинах виртуальные машины для автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="a0ce8-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="a0ce8-158">Указывает на то, следует ли заказать агент виртуальной машины на виртуальных машинах в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0ce8-159">-Confirm</span></span>
<span data-ttu-id="a0ce8-160">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0ce8-161">-WhatIf</span></span>
<span data-ttu-id="a0ce8-162">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0ce8-163">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ce8-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ce8-164">CommonParameters</span></span>
<span data-ttu-id="a0ce8-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ce8-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ce8-166">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0ce8-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ce8-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0ce8-167">INPUTS</span></span>

### <span data-ttu-id="a0ce8-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0ce8-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a0ce8-169">System.String</span><span class="sxs-lookup"><span data-stu-id="a0ce8-169">System.String</span></span>

### <span data-ttu-id="a0ce8-170">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a0ce8-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a0ce8-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span><span class="sxs-lookup"><span data-stu-id="a0ce8-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="a0ce8-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span><span class="sxs-lookup"><span data-stu-id="a0ce8-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="a0ce8-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span><span class="sxs-lookup"><span data-stu-id="a0ce8-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="a0ce8-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span><span class="sxs-lookup"><span data-stu-id="a0ce8-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="a0ce8-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0ce8-175">OUTPUTS</span></span>

### <span data-ttu-id="a0ce8-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="a0ce8-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a0ce8-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a0ce8-177">NOTES</span></span>

## <span data-ttu-id="a0ce8-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0ce8-178">RELATED LINKS</span></span>

[<span data-ttu-id="a0ce8-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="a0ce8-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="a0ce8-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="a0ce8-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="a0ce8-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="a0ce8-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="a0ce8-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="a0ce8-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="a0ce8-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a0ce8-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


