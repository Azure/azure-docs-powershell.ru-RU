---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398246"
---
# <span data-ttu-id="470a8-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="470a8-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="470a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="470a8-102">SYNOPSIS</span></span>
<span data-ttu-id="470a8-103">Задает расширение Azure SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="470a8-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="470a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="470a8-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="470a8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="470a8-105">DESCRIPTION</span></span>
<span data-ttu-id="470a8-106">Для виртуальной машины задается расширение AzureSQL Server с использованием cmdlet **Set-AzVMSqlServerExtension.**</span><span class="sxs-lookup"><span data-stu-id="470a8-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="470a8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="470a8-107">EXAMPLES</span></span>

### <span data-ttu-id="470a8-108">Пример 1. Настройка параметров автоматического исправления на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="470a8-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="470a8-109">Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="470a8-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="470a8-110">Команда сохраняет конфигурацию в переменной $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="470a8-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="470a8-111">Вторая команда получает виртуальную машину VirtualMachine11 в службе Service02 с Get-AzVM командлетом.</span><span class="sxs-lookup"><span data-stu-id="470a8-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="470a8-112">Эта команда передает этот объект текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="470a8-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="470a8-113">Текущий cmdlet задает параметры автоматического исправления в $AutoPatchingConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="470a8-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="470a8-114">Эта команда передает виртуальную машину к Update-AzVM командлету.</span><span class="sxs-lookup"><span data-stu-id="470a8-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="470a8-115">Пример 2. Настройка параметров автоматического резервного копирования на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="470a8-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="470a8-116">Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoBackupConfig.**</span><span class="sxs-lookup"><span data-stu-id="470a8-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="470a8-117">Команда сохраняет конфигурацию в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="470a8-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="470a8-118">Вторая команда получает виртуальную машину с именем VirtualMa в службе Service02 и передает ее текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="470a8-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="470a8-119">Текущий cmdlet задает параметры автоматического резервного копирования в $AutoBackupConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="470a8-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="470a8-120">Эта команда передает виртуальную машину к Update-AzVM командлету.</span><span class="sxs-lookup"><span data-stu-id="470a8-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="470a8-121">Пример 3. Отключение расширения SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="470a8-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="470a8-122">Эта команда получает виртуальную машину с именем VirtualMachine08 в службе Service03 и передает ее текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="470a8-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="470a8-123">Эта команда отключает расширение SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="470a8-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="470a8-124">Пример 4. Удалить расширение SQL Server на определенной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="470a8-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="470a8-125">Эта команда получает виртуальную машину с именем VirtualMachine08 в службе Service03 и передает ее текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="470a8-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="470a8-126">Эта команда выгрузит расширение SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="470a8-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="470a8-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="470a8-127">PARAMETERS</span></span>

### <span data-ttu-id="470a8-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="470a8-128">-AutoBackupSettings</span></span>
<span data-ttu-id="470a8-129">Параметры автоматического SQL Server параметры резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="470a8-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="470a8-130">Чтобы создать объект **AutoBackupSettings,** используйте New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="470a8-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="470a8-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="470a8-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="470a8-132">Определяет параметры автоматического SQL Server исправлений.</span><span class="sxs-lookup"><span data-stu-id="470a8-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="470a8-133">Чтобы создать объект **AutoPatchingSettings,** используйте New-AzureVMSqlServerAutoPatchingConfig..</span><span class="sxs-lookup"><span data-stu-id="470a8-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="470a8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470a8-134">-DefaultProfile</span></span>
<span data-ttu-id="470a8-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="470a8-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="470a8-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="470a8-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="470a8-137">-Location</span><span class="sxs-lookup"><span data-stu-id="470a8-137">-Location</span></span>
<span data-ttu-id="470a8-138">Определяет расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="470a8-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="470a8-139">-Name</span><span class="sxs-lookup"><span data-stu-id="470a8-139">-Name</span></span>
<span data-ttu-id="470a8-140">Указывает имя имени SQL Server расширения.</span><span class="sxs-lookup"><span data-stu-id="470a8-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="470a8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="470a8-141">-ResourceGroupName</span></span>
<span data-ttu-id="470a8-142">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="470a8-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="470a8-143">-Версия</span><span class="sxs-lookup"><span data-stu-id="470a8-143">-Version</span></span>
<span data-ttu-id="470a8-144">Определяет версию расширения SQL Server.</span><span class="sxs-lookup"><span data-stu-id="470a8-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="470a8-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="470a8-145">-VMName</span></span>
<span data-ttu-id="470a8-146">Указывает имя виртуальной машины, на которой этот SQL Server расширения.</span><span class="sxs-lookup"><span data-stu-id="470a8-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="470a8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470a8-147">CommonParameters</span></span>
<span data-ttu-id="470a8-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470a8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470a8-149">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470a8-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470a8-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="470a8-150">INPUTS</span></span>

### <span data-ttu-id="470a8-151">Нет</span><span class="sxs-lookup"><span data-stu-id="470a8-151">None</span></span>
<span data-ttu-id="470a8-152">Этот cmdlet не принимает входные данные.</span><span class="sxs-lookup"><span data-stu-id="470a8-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="470a8-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="470a8-153">OUTPUTS</span></span>

### <span data-ttu-id="470a8-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="470a8-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="470a8-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="470a8-155">NOTES</span></span>

## <span data-ttu-id="470a8-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="470a8-156">RELATED LINKS</span></span>

[<span data-ttu-id="470a8-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="470a8-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="470a8-158">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="470a8-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="470a8-159">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="470a8-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="470a8-160">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="470a8-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="470a8-161">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="470a8-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="470a8-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="470a8-162">Update-AzVM</span></span>](./Update-AzVM.md)


