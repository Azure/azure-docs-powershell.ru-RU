---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912305"
---
# <span data-ttu-id="bb12f-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bb12f-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="bb12f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb12f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb12f-103">Задает расширение Azure SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bb12f-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="bb12f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb12f-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb12f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb12f-105">DESCRIPTION</span></span>
<span data-ttu-id="bb12f-106">Командлет **Set-AzVMSqlServerExtension** задает серверное расширение AzureSQL на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bb12f-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="bb12f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb12f-107">EXAMPLES</span></span>

### <span data-ttu-id="bb12f-108">Пример 1: Настройка автоматических параметров исправлений на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="bb12f-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="bb12f-109">Первая команда создает объект конфигурации с помощью командлета **New-AzVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="bb12f-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="bb12f-110">Эта команда хранит конфигурацию в переменной $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="bb12f-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="bb12f-111">Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 с помощью командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="bb12f-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="bb12f-112">Команда передает этот объект в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="bb12f-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bb12f-113">Текущий командлет задает параметры автоматического исправления в $AutoPatchingConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bb12f-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="bb12f-114">Команда передает виртуальную машину командлету Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="bb12f-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="bb12f-115">Пример 2: Настройка параметров автоматического резервного копирования на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="bb12f-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="bb12f-116">Первая команда создает объект конфигурации с помощью командлета **New-AzVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="bb12f-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="bb12f-117">Эта команда хранит конфигурацию в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="bb12f-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="bb12f-118">Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 и передает ее в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="bb12f-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bb12f-119">Текущий командлет задает параметры автоматического резервного копирования в $AutoBackupConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bb12f-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="bb12f-120">Команда передает виртуальную машину командлету Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="bb12f-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="bb12f-121">Пример 3: отключение расширения SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="bb12f-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="bb12f-122">Эта команда получает виртуальную машину с именем VirtualMachine08 на Service03, а затем передает ее в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="bb12f-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bb12f-123">Команда отключает расширение виртуальной машины SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bb12f-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="bb12f-124">Пример 4: удаление расширения SQL Server на определенной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="bb12f-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="bb12f-125">Эта команда получает виртуальную машину с именем VirtualMachine08 на Service03, а затем передает ее в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="bb12f-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="bb12f-126">Команда удаляет расширение виртуальной машины SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bb12f-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="bb12f-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb12f-127">PARAMETERS</span></span>

### <span data-ttu-id="bb12f-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="bb12f-128">-AutoBackupSettings</span></span>
<span data-ttu-id="bb12f-129">Задает параметры автоматического резервного копирования SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bb12f-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="bb12f-130">Чтобы создать объект **AutoBackupSettings** , используйте командлет New-AzVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="bb12f-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="bb12f-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="bb12f-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="bb12f-132">Задает параметры автоматического исправления SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bb12f-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="bb12f-133">Чтобы создать объект **AutoPatchingSettings** , используйте командлет New-AzVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="bb12f-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="bb12f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb12f-134">-DefaultProfile</span></span>
<span data-ttu-id="bb12f-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb12f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb12f-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="bb12f-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="bb12f-137">-Location</span><span class="sxs-lookup"><span data-stu-id="bb12f-137">-Location</span></span>
<span data-ttu-id="bb12f-138">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bb12f-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="bb12f-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb12f-139">-Name</span></span>
<span data-ttu-id="bb12f-140">Указывает имя сервера SQL Server, на котором находится расширение.</span><span class="sxs-lookup"><span data-stu-id="bb12f-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="bb12f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb12f-141">-ResourceGroupName</span></span>
<span data-ttu-id="bb12f-142">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bb12f-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bb12f-143">-Version</span><span class="sxs-lookup"><span data-stu-id="bb12f-143">-Version</span></span>
<span data-ttu-id="bb12f-144">Указывает версию расширения SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bb12f-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="bb12f-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="bb12f-145">-VMName</span></span>
<span data-ttu-id="bb12f-146">Указывает имя виртуальной машины, на которой этот командлет задает расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bb12f-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="bb12f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb12f-147">CommonParameters</span></span>
<span data-ttu-id="bb12f-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb12f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb12f-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb12f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb12f-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb12f-150">INPUTS</span></span>

### <span data-ttu-id="bb12f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="bb12f-151">System.String</span></span>

### <span data-ttu-id="bb12f-152">Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="bb12f-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="bb12f-153">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="bb12f-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="bb12f-154">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="bb12f-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="bb12f-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb12f-155">OUTPUTS</span></span>

### <span data-ttu-id="bb12f-156">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bb12f-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bb12f-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb12f-157">NOTES</span></span>

## <span data-ttu-id="bb12f-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb12f-158">RELATED LINKS</span></span>

[<span data-ttu-id="bb12f-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bb12f-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bb12f-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bb12f-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="bb12f-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="bb12f-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="bb12f-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="bb12f-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="bb12f-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bb12f-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="bb12f-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bb12f-164">Update-AzVM</span></span>](./Update-AzVM.md)


