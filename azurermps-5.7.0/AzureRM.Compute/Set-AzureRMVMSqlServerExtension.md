---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: c3a146b99119ab94bf98176d202cda52e1dc5704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566215"
---
# <span data-ttu-id="92ed9-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="92ed9-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="92ed9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="92ed9-103">Задает расширение Azure SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="92ed9-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92ed9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92ed9-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="92ed9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92ed9-105">DESCRIPTION</span></span>
<span data-ttu-id="92ed9-106">Командлет **Set-AzureRmVMSqlServerExtension** задает серверное расширение AzureSQL на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="92ed9-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="92ed9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92ed9-107">EXAMPLES</span></span>

### <span data-ttu-id="92ed9-108">Пример 1: Настройка автоматических параметров исправлений на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="92ed9-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="92ed9-109">Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="92ed9-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="92ed9-110">Эта команда хранит конфигурацию в переменной $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="92ed9-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="92ed9-111">Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 с помощью командлета Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="92ed9-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="92ed9-112">Команда передает этот объект в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="92ed9-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="92ed9-113">Текущий командлет задает параметры автоматического исправления в $AutoPatchingConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92ed9-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="92ed9-114">Команда передает виртуальную машину командлету Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="92ed9-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="92ed9-115">Пример 2: Настройка параметров автоматического резервного копирования на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="92ed9-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="92ed9-116">Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="92ed9-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="92ed9-117">Эта команда хранит конфигурацию в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="92ed9-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="92ed9-118">Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 и передает ее в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="92ed9-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="92ed9-119">Текущий командлет задает параметры автоматического резервного копирования в $AutoBackupConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92ed9-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="92ed9-120">Команда передает виртуальную машину командлету Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="92ed9-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="92ed9-121">Пример 3: отключение расширения SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="92ed9-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="92ed9-122">Эта команда получает виртуальную машину с именем VirtualMachine08 на Service03, а затем передает ее в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="92ed9-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="92ed9-123">Команда отключает расширение виртуальной машины SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="92ed9-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="92ed9-124">Пример 4: удаление расширения SQL Server на определенной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="92ed9-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="92ed9-125">Эта команда получает виртуальную машину с именем VirtualMachine08 на Service03, а затем передает ее в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="92ed9-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="92ed9-126">Команда удаляет расширение виртуальной машины SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="92ed9-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="92ed9-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92ed9-127">PARAMETERS</span></span>

### <span data-ttu-id="92ed9-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="92ed9-128">-AutoBackupSettings</span></span>
<span data-ttu-id="92ed9-129">Задает параметры автоматического резервного копирования SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92ed9-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="92ed9-130">Чтобы создать объект **AutoBackupSettings** , используйте командлет New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="92ed9-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ed9-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="92ed9-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="92ed9-132">Задает параметры автоматического исправления SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92ed9-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="92ed9-133">Чтобы создать объект **AutoPatchingSettings** , используйте командлет New-AzureVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="92ed9-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ed9-134">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="92ed9-134">-KeyVaultCredentialSettings</span></span>
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ed9-135">-Location</span><span class="sxs-lookup"><span data-stu-id="92ed9-135">-Location</span></span>
<span data-ttu-id="92ed9-136">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92ed9-136">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ed9-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92ed9-137">-Name</span></span>
<span data-ttu-id="92ed9-138">Указывает имя сервера SQL Server, на котором находится расширение.</span><span class="sxs-lookup"><span data-stu-id="92ed9-138">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="92ed9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92ed9-139">-ResourceGroupName</span></span>
<span data-ttu-id="92ed9-140">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92ed9-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ed9-141">-Version</span><span class="sxs-lookup"><span data-stu-id="92ed9-141">-Version</span></span>
<span data-ttu-id="92ed9-142">Указывает версию расширения SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92ed9-142">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ed9-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="92ed9-143">-VMName</span></span>
<span data-ttu-id="92ed9-144">Указывает имя виртуальной машины, на которой этот командлет задает расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92ed9-144">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92ed9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ed9-145">CommonParameters</span></span>
<span data-ttu-id="92ed9-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92ed9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ed9-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92ed9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ed9-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92ed9-148">INPUTS</span></span>

### <span data-ttu-id="92ed9-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="92ed9-149">None</span></span>
<span data-ttu-id="92ed9-150">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="92ed9-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92ed9-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92ed9-151">OUTPUTS</span></span>

## <span data-ttu-id="92ed9-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="92ed9-152">NOTES</span></span>

## <span data-ttu-id="92ed9-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92ed9-153">RELATED LINKS</span></span>

[<span data-ttu-id="92ed9-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92ed9-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="92ed9-155">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="92ed9-155">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="92ed9-156">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="92ed9-156">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="92ed9-157">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="92ed9-157">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="92ed9-158">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="92ed9-158">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="92ed9-159">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92ed9-159">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


