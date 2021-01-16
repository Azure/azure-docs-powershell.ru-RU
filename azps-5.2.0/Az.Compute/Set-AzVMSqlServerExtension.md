---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393932"
---
# <span data-ttu-id="d5314-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d5314-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="d5314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5314-102">SYNOPSIS</span></span>
<span data-ttu-id="d5314-103">Задает расширение Azure SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d5314-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="d5314-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5314-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5314-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5314-105">DESCRIPTION</span></span>
<span data-ttu-id="d5314-106">Для виртуальной машины задается расширение AzureSQL Server с использованием cmdlet **Set-AzVMSqlServerExtension.**</span><span class="sxs-lookup"><span data-stu-id="d5314-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="d5314-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5314-107">EXAMPLES</span></span>

### <span data-ttu-id="d5314-108">Пример 1. Настройка параметров автоматического исправления на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="d5314-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="d5314-109">Первая команда создает объект конфигурации с помощью командлета **New-AzVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="d5314-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="d5314-110">Команда сохраняет конфигурацию в переменной $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="d5314-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="d5314-111">Вторая команда получает виртуальную машину VirtualMachine11 в службе Service02 с Get-AzVM командлетом.</span><span class="sxs-lookup"><span data-stu-id="d5314-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="d5314-112">Эта команда передает этот объект текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d5314-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d5314-113">Текущий cmdlet задает параметры автоматического исправления в $AutoPatchingConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d5314-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="d5314-114">Эта команда передает виртуальную машину к Update-AzVM командлету.</span><span class="sxs-lookup"><span data-stu-id="d5314-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="d5314-115">Пример 2. Настройка параметров автоматического резервного копирования на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="d5314-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="d5314-116">Первая команда создает объект конфигурации с помощью командлета **New-AzVMSqlServerAutoBackupConfig.**</span><span class="sxs-lookup"><span data-stu-id="d5314-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="d5314-117">Команда сохраняет конфигурацию в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="d5314-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="d5314-118">Вторая команда получает виртуальную машину с именем VirtualMa в службе Service02 и передает ее текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="d5314-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="d5314-119">Текущий cmdlet задает параметры автоматического резервного копирования в $AutoBackupConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d5314-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="d5314-120">Эта команда передает виртуальную машину к Update-AzVM командлету.</span><span class="sxs-lookup"><span data-stu-id="d5314-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="d5314-121">Пример 3. Отключение расширения SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="d5314-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="d5314-122">Эта команда получает виртуальную машину с именем VirtualMachine08 в службе Service03 и передает ее текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="d5314-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="d5314-123">Эта команда отключает расширение SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d5314-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="d5314-124">Пример 4. Удалить расширение SQL Server на определенной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="d5314-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="d5314-125">Эта команда получает виртуальную машину с именем VirtualMachine08 в службе Service03 и передает ее текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="d5314-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="d5314-126">Эта команда выгрузит расширение SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d5314-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="d5314-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5314-127">PARAMETERS</span></span>

### <span data-ttu-id="d5314-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="d5314-128">-AutoBackupSettings</span></span>
<span data-ttu-id="d5314-129">Параметры автоматического SQL Server параметры резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d5314-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="d5314-130">Чтобы создать объект **AutoBackupSettings,** используйте New-AzVMSqlServerAutoBackupConfig..</span><span class="sxs-lookup"><span data-stu-id="d5314-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5314-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="d5314-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="d5314-132">Определяет параметры автоматического SQL Server исправлений.</span><span class="sxs-lookup"><span data-stu-id="d5314-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="d5314-133">Чтобы создать объект **AutoPatchingSettings,** используйте New-AzVMSqlServerAutoPatchingConfig..</span><span class="sxs-lookup"><span data-stu-id="d5314-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5314-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5314-134">-DefaultProfile</span></span>
<span data-ttu-id="d5314-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5314-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5314-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="d5314-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5314-137">-Location</span><span class="sxs-lookup"><span data-stu-id="d5314-137">-Location</span></span>
<span data-ttu-id="d5314-138">Определяет расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d5314-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5314-139">-Name</span><span class="sxs-lookup"><span data-stu-id="d5314-139">-Name</span></span>
<span data-ttu-id="d5314-140">Указывает имя имени SQL Server расширения.</span><span class="sxs-lookup"><span data-stu-id="d5314-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="d5314-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5314-141">-ResourceGroupName</span></span>
<span data-ttu-id="d5314-142">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d5314-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d5314-143">-Версия</span><span class="sxs-lookup"><span data-stu-id="d5314-143">-Version</span></span>
<span data-ttu-id="d5314-144">Определяет версию расширения SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d5314-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5314-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="d5314-145">-VMName</span></span>
<span data-ttu-id="d5314-146">Задает имя виртуальной машины, на которой этот SQL Server расширения.</span><span class="sxs-lookup"><span data-stu-id="d5314-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5314-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5314-147">CommonParameters</span></span>
<span data-ttu-id="d5314-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5314-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5314-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5314-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5314-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5314-150">INPUTS</span></span>

### <span data-ttu-id="d5314-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d5314-151">System.String</span></span>

### <span data-ttu-id="d5314-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="d5314-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="d5314-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="d5314-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="d5314-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="d5314-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="d5314-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5314-155">OUTPUTS</span></span>

### <span data-ttu-id="d5314-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d5314-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d5314-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5314-157">NOTES</span></span>

## <span data-ttu-id="d5314-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5314-158">RELATED LINKS</span></span>

[<span data-ttu-id="d5314-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d5314-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d5314-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d5314-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="d5314-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="d5314-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="d5314-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="d5314-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="d5314-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d5314-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="d5314-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d5314-164">Update-AzVM</span></span>](./Update-AzVM.md)

