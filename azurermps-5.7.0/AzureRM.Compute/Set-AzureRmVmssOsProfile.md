---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: ee9649d7a2a88dd3a91f428201ddc66d1a6562da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734467"
---
# <span data-ttu-id="86003-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="86003-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="86003-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86003-102">SYNOPSIS</span></span>
<span data-ttu-id="86003-103">Задает свойства профиля операционной системы VMSS.</span><span class="sxs-lookup"><span data-stu-id="86003-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86003-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86003-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86003-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86003-105">DESCRIPTION</span></span>
<span data-ttu-id="86003-106">Командлет **Set-AzureRmVmssOsProfile** задает для параметров профиля виртуальной машины параметры, заданные в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="86003-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="86003-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86003-107">EXAMPLES</span></span>

### <span data-ttu-id="86003-108">Пример 1: Настройка свойств профиля операционной системы для VMSS</span><span class="sxs-lookup"><span data-stu-id="86003-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="86003-109">Эта команда задает свойства профиля операционной системы для виртуальных машин, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="86003-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="86003-110">Команда задает префикс имени компьютера для всех экземпляров виртуальных машин в VMSS для проверки и предоставляет имя пользователя и пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="86003-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="86003-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86003-111">PARAMETERS</span></span>

### <span data-ttu-id="86003-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="86003-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="86003-113">Указывает объект автоматического содержимого.</span><span class="sxs-lookup"><span data-stu-id="86003-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="86003-114">Для создания объекта можно использовать Add-AzureRmVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="86003-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="86003-115">-AdminPassword</span></span>
<span data-ttu-id="86003-116">Указывает пароль администратора, который будет использоваться для всех экземпляров виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="86003-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="86003-117">-AdminUsername</span></span>
<span data-ttu-id="86003-118">Указывает имя учетной записи администратора, которое будет использоваться для всех экземпляров виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="86003-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="86003-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="86003-120">Задает префикс имени компьютера для всех экземпляров виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="86003-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="86003-121">Имена компьютеров должны содержать от 1 до 15 символов.</span><span class="sxs-lookup"><span data-stu-id="86003-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="86003-122">-CustomData</span></span>
<span data-ttu-id="86003-123">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="86003-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="86003-124">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="86003-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="86003-125">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="86003-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-126">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="86003-126">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="86003-127">Указывает на то, что этот командлет отключает проверку подлинности пароля.</span><span class="sxs-lookup"><span data-stu-id="86003-127">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-128">-Прослушиватель</span><span class="sxs-lookup"><span data-stu-id="86003-128">-Listener</span></span>
<span data-ttu-id="86003-129">Указывает прослушиватели удаленного управления Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="86003-129">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="86003-130">Это позволяет использовать удаленную оболочку Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="86003-130">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="86003-131">Для создания прослушивателя можно использовать командлет Add-AzureRmVmssWinRMListener.</span><span class="sxs-lookup"><span data-stu-id="86003-131">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-132">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="86003-132">-PublicKey</span></span>
<span data-ttu-id="86003-133">Определяет объект открытого ключа Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="86003-133">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="86003-134">Для создания объекта можно использовать командлет Add-AzureRmVMSshPublicKey.</span><span class="sxs-lookup"><span data-stu-id="86003-134">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-135">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="86003-135">-Secret</span></span>
<span data-ttu-id="86003-136">Указывает секретный объект, который содержит ссылки на сертификаты для размещения на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="86003-136">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="86003-137">Вы можете использовать командлет Add-AzureRmVmssSecret для создания секретного объекта.</span><span class="sxs-lookup"><span data-stu-id="86003-137">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-138">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="86003-138">-TimeZone</span></span>
<span data-ttu-id="86003-139">Указывает часовой пояс для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="86003-139">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-140">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="86003-140">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="86003-141">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="86003-141">Specifies the VMSS object.</span></span>
<span data-ttu-id="86003-142">Для создания объекта можно использовать командлет New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="86003-142">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-143">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="86003-143">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="86003-144">Указывает, включены ли для виртуальных машин в VMSS автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="86003-144">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-145">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="86003-145">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="86003-146">Указывает, должен ли агент виртуальной машины быть подготовлен на виртуальных машинах в VMSS.</span><span class="sxs-lookup"><span data-stu-id="86003-146">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86003-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86003-147">-Confirm</span></span>
<span data-ttu-id="86003-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86003-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86003-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86003-149">-WhatIf</span></span>
<span data-ttu-id="86003-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86003-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86003-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86003-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86003-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86003-152">CommonParameters</span></span>
<span data-ttu-id="86003-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86003-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86003-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86003-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86003-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86003-155">INPUTS</span></span>

### <span data-ttu-id="86003-156">Ничего</span><span class="sxs-lookup"><span data-stu-id="86003-156">None</span></span>
<span data-ttu-id="86003-157">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="86003-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86003-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86003-158">OUTPUTS</span></span>

### <span data-ttu-id="86003-159">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="86003-159">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="86003-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="86003-160">NOTES</span></span>

## <span data-ttu-id="86003-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86003-161">RELATED LINKS</span></span>

[<span data-ttu-id="86003-162">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="86003-162">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="86003-163">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="86003-163">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="86003-164">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="86003-164">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="86003-165">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="86003-165">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="86003-166">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="86003-166">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


