---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: 45deca60451f79dd0d20a0b1238f32e91d8ef2ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564639"
---
# <span data-ttu-id="fcea0-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="fcea0-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="fcea0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fcea0-102">SYNOPSIS</span></span>
<span data-ttu-id="fcea0-103">Задает свойства профиля операционной системы VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcea0-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcea0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fcea0-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcea0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcea0-105">DESCRIPTION</span></span>
<span data-ttu-id="fcea0-106">Командлет **Set-AzureRmVmssOsProfile** задает для параметров профиля виртуальной машины параметры, заданные в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="fcea0-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="fcea0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fcea0-107">EXAMPLES</span></span>

### <span data-ttu-id="fcea0-108">Пример 1: Настройка свойств профиля операционной системы для VMSS</span><span class="sxs-lookup"><span data-stu-id="fcea0-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="fcea0-109">Эта команда задает свойства профиля операционной системы для виртуальных машин, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="fcea0-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="fcea0-110">Команда задает префикс имени компьютера для всех экземпляров виртуальных машин в VMSS для проверки и предоставляет имя пользователя и пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="fcea0-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="fcea0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fcea0-111">PARAMETERS</span></span>

### <span data-ttu-id="fcea0-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="fcea0-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="fcea0-113">Указывает объект автоматического содержимого.</span><span class="sxs-lookup"><span data-stu-id="fcea0-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="fcea0-114">Для создания объекта можно использовать Add-AzureRmVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="fcea0-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="fcea0-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="fcea0-115">-AdminPassword</span></span>
<span data-ttu-id="fcea0-116">Указывает пароль администратора, который будет использоваться для всех экземпляров виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcea0-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="fcea0-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="fcea0-117">-AdminUsername</span></span>
<span data-ttu-id="fcea0-118">Указывает имя учетной записи администратора, которое будет использоваться для всех экземпляров виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcea0-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="fcea0-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="fcea0-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="fcea0-120">Задает префикс имени компьютера для всех экземпляров виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcea0-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="fcea0-121">Имена компьютеров должны содержать от 1 до 15 символов.</span><span class="sxs-lookup"><span data-stu-id="fcea0-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="fcea0-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="fcea0-122">-CustomData</span></span>
<span data-ttu-id="fcea0-123">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="fcea0-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="fcea0-124">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fcea0-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="fcea0-125">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="fcea0-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="fcea0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcea0-126">-DefaultProfile</span></span>
<span data-ttu-id="fcea0-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcea0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcea0-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="fcea0-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="fcea0-129">Указывает на то, что этот командлет отключает проверку подлинности пароля.</span><span class="sxs-lookup"><span data-stu-id="fcea0-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="fcea0-130">-Прослушиватель</span><span class="sxs-lookup"><span data-stu-id="fcea0-130">-Listener</span></span>
<span data-ttu-id="fcea0-131">Указывает прослушиватели удаленного управления Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="fcea0-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="fcea0-132">Это позволяет использовать удаленную оболочку Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fcea0-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="fcea0-133">Для создания прослушивателя можно использовать командлет Add-AzureRmVmssWinRMListener.</span><span class="sxs-lookup"><span data-stu-id="fcea0-133">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="fcea0-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="fcea0-134">-PublicKey</span></span>
<span data-ttu-id="fcea0-135">Определяет объект открытого ключа Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="fcea0-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="fcea0-136">Для создания объекта можно использовать командлет Add-AzureRmVMSshPublicKey.</span><span class="sxs-lookup"><span data-stu-id="fcea0-136">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="fcea0-137">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="fcea0-137">-Secret</span></span>
<span data-ttu-id="fcea0-138">Указывает секретный объект, который содержит ссылки на сертификаты для размещения на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fcea0-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="fcea0-139">Вы можете использовать командлет Add-AzureRmVmssSecret для создания секретного объекта.</span><span class="sxs-lookup"><span data-stu-id="fcea0-139">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="fcea0-140">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="fcea0-140">-TimeZone</span></span>
<span data-ttu-id="fcea0-141">Указывает часовой пояс для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fcea0-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="fcea0-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fcea0-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fcea0-143">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcea0-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="fcea0-144">Для создания объекта можно использовать командлет New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="fcea0-144">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="fcea0-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="fcea0-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="fcea0-146">Указывает, включены ли для виртуальных машин в VMSS автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="fcea0-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="fcea0-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="fcea0-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="fcea0-148">Указывает, должен ли агент виртуальной машины быть подготовлен на виртуальных машинах в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcea0-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="fcea0-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcea0-149">-Confirm</span></span>
<span data-ttu-id="fcea0-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fcea0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcea0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcea0-151">-WhatIf</span></span>
<span data-ttu-id="fcea0-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fcea0-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcea0-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fcea0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcea0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcea0-154">CommonParameters</span></span>
<span data-ttu-id="fcea0-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fcea0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcea0-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcea0-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcea0-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fcea0-157">INPUTS</span></span>

### <span data-ttu-id="fcea0-158">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fcea0-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fcea0-159">System. String</span><span class="sxs-lookup"><span data-stu-id="fcea0-159">System.String</span></span>

### <span data-ttu-id="fcea0-160">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fcea0-160">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="fcea0-161">Microsoft. Azure. Management. COMPUTE. Models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="fcea0-161">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="fcea0-162">Microsoft. Azure. Management. COMPUTE. Models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="fcea0-162">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="fcea0-163">Microsoft. Azure. Management. COMPUTE. Models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="fcea0-163">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="fcea0-164">Microsoft. Azure. Management. COMPUTE. Models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="fcea0-164">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="fcea0-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcea0-165">OUTPUTS</span></span>

### <span data-ttu-id="fcea0-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fcea0-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fcea0-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="fcea0-167">NOTES</span></span>

## <span data-ttu-id="fcea0-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcea0-168">RELATED LINKS</span></span>

[<span data-ttu-id="fcea0-169">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="fcea0-169">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="fcea0-170">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="fcea0-170">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="fcea0-171">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="fcea0-171">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="fcea0-172">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="fcea0-172">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="fcea0-173">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fcea0-173">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


