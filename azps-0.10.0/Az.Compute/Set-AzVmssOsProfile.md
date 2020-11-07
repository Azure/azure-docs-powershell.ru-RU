---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 98ebce4e139d230607da77536492d0ba40d0760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911313"
---
# <span data-ttu-id="00fe2-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="00fe2-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="00fe2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="00fe2-103">Задает свойства профиля операционной системы VMSS.</span><span class="sxs-lookup"><span data-stu-id="00fe2-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="00fe2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00fe2-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00fe2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="00fe2-106">Командлет **Set-AzVmssOsProfile** задает для параметров профиля виртуальной машины параметры, заданные в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="00fe2-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="00fe2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00fe2-107">EXAMPLES</span></span>

### <span data-ttu-id="00fe2-108">Пример 1: Настройка свойств профиля операционной системы для VMSS</span><span class="sxs-lookup"><span data-stu-id="00fe2-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="00fe2-109">Эта команда задает свойства профиля операционной системы для виртуальных машин, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="00fe2-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="00fe2-110">Команда задает префикс имени компьютера для всех экземпляров виртуальных машин в VMSS для проверки и предоставляет имя пользователя и пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="00fe2-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="00fe2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00fe2-111">PARAMETERS</span></span>

### <span data-ttu-id="00fe2-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="00fe2-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="00fe2-113">Указывает объект автоматического содержимого.</span><span class="sxs-lookup"><span data-stu-id="00fe2-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="00fe2-114">Для создания объекта можно использовать Add-AzVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="00fe2-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="00fe2-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="00fe2-115">-AdminPassword</span></span>
<span data-ttu-id="00fe2-116">Указывает пароль администратора, который будет использоваться для всех экземпляров виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="00fe2-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="00fe2-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="00fe2-117">-AdminUsername</span></span>
<span data-ttu-id="00fe2-118">Указывает имя учетной записи администратора, которое будет использоваться для всех экземпляров виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="00fe2-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="00fe2-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="00fe2-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="00fe2-120">Задает префикс имени компьютера для всех экземпляров виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="00fe2-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="00fe2-121">Имена компьютеров должны содержать от 1 до 15 символов.</span><span class="sxs-lookup"><span data-stu-id="00fe2-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="00fe2-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="00fe2-122">-CustomData</span></span>
<span data-ttu-id="00fe2-123">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="00fe2-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="00fe2-124">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="00fe2-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="00fe2-125">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="00fe2-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="00fe2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fe2-126">-DefaultProfile</span></span>
<span data-ttu-id="00fe2-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00fe2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fe2-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="00fe2-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="00fe2-129">Указывает на то, что этот командлет отключает проверку подлинности пароля.</span><span class="sxs-lookup"><span data-stu-id="00fe2-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="00fe2-130">-Прослушиватель</span><span class="sxs-lookup"><span data-stu-id="00fe2-130">-Listener</span></span>
<span data-ttu-id="00fe2-131">Указывает прослушиватели удаленного управления Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="00fe2-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="00fe2-132">Это позволяет использовать удаленную оболочку Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="00fe2-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="00fe2-133">Для создания прослушивателя можно использовать командлет Add-AzVmssWinRMListener.</span><span class="sxs-lookup"><span data-stu-id="00fe2-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="00fe2-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="00fe2-134">-PublicKey</span></span>
<span data-ttu-id="00fe2-135">Определяет объект открытого ключа Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="00fe2-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="00fe2-136">Для создания объекта можно использовать командлет Add-AzVMSshPublicKey.</span><span class="sxs-lookup"><span data-stu-id="00fe2-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="00fe2-137">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="00fe2-137">-Secret</span></span>
<span data-ttu-id="00fe2-138">Указывает секретный объект, который содержит ссылки на сертификаты для размещения на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="00fe2-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="00fe2-139">Вы можете использовать командлет Add-AzVmssSecret для создания секретного объекта.</span><span class="sxs-lookup"><span data-stu-id="00fe2-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="00fe2-140">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="00fe2-140">-TimeZone</span></span>
<span data-ttu-id="00fe2-141">Указывает часовой пояс для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="00fe2-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="00fe2-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="00fe2-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="00fe2-143">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="00fe2-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="00fe2-144">Для создания объекта можно использовать командлет New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="00fe2-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00fe2-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="00fe2-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="00fe2-146">Указывает, включены ли для виртуальных машин в VMSS автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="00fe2-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="00fe2-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="00fe2-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="00fe2-148">Указывает, должен ли агент виртуальной машины быть подготовлен на виртуальных машинах в VMSS.</span><span class="sxs-lookup"><span data-stu-id="00fe2-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="00fe2-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00fe2-149">-Confirm</span></span>
<span data-ttu-id="00fe2-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="00fe2-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00fe2-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fe2-151">-WhatIf</span></span>
<span data-ttu-id="00fe2-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="00fe2-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00fe2-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00fe2-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00fe2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fe2-154">CommonParameters</span></span>
<span data-ttu-id="00fe2-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00fe2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fe2-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00fe2-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fe2-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00fe2-157">INPUTS</span></span>

### <span data-ttu-id="00fe2-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="00fe2-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="00fe2-159">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="00fe2-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="00fe2-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00fe2-160">OUTPUTS</span></span>

### <span data-ttu-id="00fe2-161">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="00fe2-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="00fe2-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="00fe2-162">NOTES</span></span>

## <span data-ttu-id="00fe2-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00fe2-163">RELATED LINKS</span></span>

[<span data-ttu-id="00fe2-164">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="00fe2-164">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="00fe2-165">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="00fe2-165">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="00fe2-166">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="00fe2-166">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="00fe2-167">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="00fe2-167">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="00fe2-168">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="00fe2-168">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


