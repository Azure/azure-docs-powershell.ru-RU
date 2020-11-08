---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076038"
---
# <span data-ttu-id="c298f-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c298f-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="c298f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c298f-102">SYNOPSIS</span></span>
<span data-ttu-id="c298f-103">Настраивает расширение диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c298f-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="c298f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c298f-104">SYNTAX</span></span>

### <span data-ttu-id="c298f-105">SetDiagnosticsExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c298f-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c298f-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="c298f-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c298f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c298f-107">DESCRIPTION</span></span>
<span data-ttu-id="c298f-108">Командлет **Set-AzureVMDiagnosticsExtension** настраивает расширение диагностики Microsoft Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c298f-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="c298f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c298f-109">EXAMPLES</span></span>

### <span data-ttu-id="c298f-110">Пример 1: создание виртуальной машины с применением расширения диагностики Azure</span><span class="sxs-lookup"><span data-stu-id="c298f-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="c298f-111">Эти команды включают расширение диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c298f-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="c298f-112">Пример 2: Включение расширения диагностики Azure на существующей виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="c298f-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="c298f-113">Первая команда использует командлет **Get-AzureVM** для получения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c298f-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="c298f-114">Вторая команда использует командлет **Set-AzureVMDiagnosticsExtension** , чтобы обновить конфигурацию виртуальной машины, чтобы включить в нее расширение диагностики Azure.</span><span class="sxs-lookup"><span data-stu-id="c298f-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="c298f-115">Последняя команда применяет обновленную конфигурацию к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c298f-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="c298f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c298f-116">PARAMETERS</span></span>

### <span data-ttu-id="c298f-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="c298f-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="c298f-118">Указывает путь конфигурации диагностики.</span><span class="sxs-lookup"><span data-stu-id="c298f-118">Specifies a path for the diagnostics configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c298f-119">-Отключение</span><span class="sxs-lookup"><span data-stu-id="c298f-119">-Disable</span></span>
<span data-ttu-id="c298f-120">Указывает, что этот командлет отключает расширение диагностики на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c298f-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c298f-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c298f-121">-InformationAction</span></span>
<span data-ttu-id="c298f-122">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="c298f-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c298f-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c298f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c298f-124">Продолжал</span><span class="sxs-lookup"><span data-stu-id="c298f-124">Continue</span></span>
- <span data-ttu-id="c298f-125">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="c298f-125">Ignore</span></span>
- <span data-ttu-id="c298f-126">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c298f-126">Inquire</span></span>
- <span data-ttu-id="c298f-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c298f-127">SilentlyContinue</span></span>
- <span data-ttu-id="c298f-128">Остановить</span><span class="sxs-lookup"><span data-stu-id="c298f-128">Stop</span></span>
- <span data-ttu-id="c298f-129">Рвать</span><span class="sxs-lookup"><span data-stu-id="c298f-129">Suspend</span></span>

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

### <span data-ttu-id="c298f-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c298f-130">-InformationVariable</span></span>
<span data-ttu-id="c298f-131">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="c298f-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c298f-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="c298f-132">-Profile</span></span>
<span data-ttu-id="c298f-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c298f-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c298f-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c298f-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c298f-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="c298f-135">-ReferenceName</span></span>
<span data-ttu-id="c298f-136">Указывает имя ссылки для расширения диагностики.</span><span class="sxs-lookup"><span data-stu-id="c298f-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c298f-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="c298f-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="c298f-138">Указывает конечную точку учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c298f-138">Specifies a storage account endpoint.</span></span>

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

### <span data-ttu-id="c298f-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c298f-139">-StorageAccountKey</span></span>
<span data-ttu-id="c298f-140">Указывает ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c298f-140">Specifies a storage account key.</span></span>

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

### <span data-ttu-id="c298f-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c298f-141">-StorageAccountName</span></span>
<span data-ttu-id="c298f-142">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c298f-142">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="c298f-143">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c298f-143">-StorageContext</span></span>
<span data-ttu-id="c298f-144">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c298f-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c298f-145">-Version</span><span class="sxs-lookup"><span data-stu-id="c298f-145">-Version</span></span>
<span data-ttu-id="c298f-146">Задает версию расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c298f-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c298f-147">-VM</span><span class="sxs-lookup"><span data-stu-id="c298f-147">-VM</span></span>
<span data-ttu-id="c298f-148">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c298f-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c298f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c298f-149">CommonParameters</span></span>
<span data-ttu-id="c298f-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c298f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c298f-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c298f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c298f-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c298f-152">INPUTS</span></span>

## <span data-ttu-id="c298f-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c298f-153">OUTPUTS</span></span>

## <span data-ttu-id="c298f-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="c298f-154">NOTES</span></span>

## <span data-ttu-id="c298f-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c298f-155">RELATED LINKS</span></span>

[<span data-ttu-id="c298f-156">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c298f-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="c298f-157">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c298f-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="c298f-158">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c298f-158">Update-AzureVM</span></span>](./Update-AzureVM.md)


