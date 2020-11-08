---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075446"
---
# <span data-ttu-id="6109a-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="6109a-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="6109a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6109a-102">SYNOPSIS</span></span>
<span data-ttu-id="6109a-103">Задает расширения ресурсов для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6109a-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="6109a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6109a-104">SYNTAX</span></span>

### <span data-ttu-id="6109a-105">SetByExtensionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6109a-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6109a-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="6109a-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6109a-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="6109a-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6109a-108">SetByReferenceNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="6109a-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6109a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6109a-109">DESCRIPTION</span></span>
<span data-ttu-id="6109a-110">Командлет **Set-AzureVMExtension** задает расширения ресурсов для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6109a-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="6109a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6109a-111">EXAMPLES</span></span>

### <span data-ttu-id="6109a-112">Пример 1: создание виртуальной машины с примененными расширениями ресурсов</span><span class="sxs-lookup"><span data-stu-id="6109a-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="6109a-113">Эта команда создает виртуальную машину с примененными расширениями ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6109a-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="6109a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6109a-114">PARAMETERS</span></span>

### <span data-ttu-id="6109a-115">-Отключение</span><span class="sxs-lookup"><span data-stu-id="6109a-115">-Disable</span></span>
<span data-ttu-id="6109a-116">Указывает на то, что этот командлет отключает состояние расширения.</span><span class="sxs-lookup"><span data-stu-id="6109a-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="6109a-117">-ExtensionName</span></span>
<span data-ttu-id="6109a-118">Указывает имя расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6109a-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="6109a-119">-ForceUpdate</span></span>
<span data-ttu-id="6109a-120">Указывает на то, что этот командлет повторно применяет конфигурацию к расширению, когда конфигурация не была обновлена.</span><span class="sxs-lookup"><span data-stu-id="6109a-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6109a-121">-InformationAction</span></span>
<span data-ttu-id="6109a-122">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6109a-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6109a-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6109a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6109a-124">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6109a-124">Continue</span></span>
- <span data-ttu-id="6109a-125">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6109a-125">Ignore</span></span>
- <span data-ttu-id="6109a-126">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6109a-126">Inquire</span></span>
- <span data-ttu-id="6109a-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6109a-127">SilentlyContinue</span></span>
- <span data-ttu-id="6109a-128">Остановить</span><span class="sxs-lookup"><span data-stu-id="6109a-128">Stop</span></span>
- <span data-ttu-id="6109a-129">Рвать</span><span class="sxs-lookup"><span data-stu-id="6109a-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6109a-130">-InformationVariable</span></span>
<span data-ttu-id="6109a-131">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6109a-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="6109a-132">-PrivateConfigKey</span></span>
<span data-ttu-id="6109a-133">Задает закрытый ключ конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6109a-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="6109a-134">-PrivateConfigPath</span></span>
<span data-ttu-id="6109a-135">Указывает частный путь конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6109a-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6109a-136">-PrivateConfiguration</span></span>
<span data-ttu-id="6109a-137">Указывает частный текст конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6109a-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="6109a-138">-Profile</span></span>
<span data-ttu-id="6109a-139">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6109a-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6109a-140">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6109a-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="6109a-141">-PublicConfigKey</span></span>
<span data-ttu-id="6109a-142">Указывает открытый ключ конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6109a-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="6109a-143">-PublicConfigPath</span></span>
<span data-ttu-id="6109a-144">Указывает путь к общедоступной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6109a-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="6109a-145">-PublicConfiguration</span></span>
<span data-ttu-id="6109a-146">Указывает общедоступный текст конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6109a-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6109a-147">-Publisher</span></span>
<span data-ttu-id="6109a-148">Указывает издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="6109a-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-149">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="6109a-149">-ReferenceName</span></span>
<span data-ttu-id="6109a-150">Указывает имя ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="6109a-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="6109a-151">Это определяемая пользователем строка, которую можно использовать для ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="6109a-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="6109a-152">Вы должны указать его, когда расширение добавляется на виртуальную машину в первый раз.</span><span class="sxs-lookup"><span data-stu-id="6109a-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="6109a-153">При последующих обновлениях необходимо указать ранее использованный эталонный код при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="6109a-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="6109a-154">ReferenceName, назначенный расширению, возвращается с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="6109a-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-155">-Удаление</span><span class="sxs-lookup"><span data-stu-id="6109a-155">-Uninstall</span></span>
<span data-ttu-id="6109a-156">Указывает, что этот командлет удаляет расширение ресурса с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6109a-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-157">-Version</span><span class="sxs-lookup"><span data-stu-id="6109a-157">-Version</span></span>
<span data-ttu-id="6109a-158">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="6109a-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-159">-VM</span><span class="sxs-lookup"><span data-stu-id="6109a-159">-VM</span></span>
<span data-ttu-id="6109a-160">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6109a-160">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6109a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6109a-161">CommonParameters</span></span>
<span data-ttu-id="6109a-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6109a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6109a-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6109a-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6109a-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6109a-164">INPUTS</span></span>

## <span data-ttu-id="6109a-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6109a-165">OUTPUTS</span></span>

## <span data-ttu-id="6109a-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="6109a-166">NOTES</span></span>

## <span data-ttu-id="6109a-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6109a-167">RELATED LINKS</span></span>

[<span data-ttu-id="6109a-168">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="6109a-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="6109a-169">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="6109a-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="6109a-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6109a-170">Get-AzureVM</span></span>](./Get-AzureVM.md)


