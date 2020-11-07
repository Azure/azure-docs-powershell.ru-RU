---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 4093e236f84d7587586ba30c8bd4653c4ba7358f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911324"
---
# <span data-ttu-id="f28f2-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f28f2-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="f28f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f28f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f28f2-103">Задает расширение Azure SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f28f2-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="f28f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f28f2-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f28f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f28f2-105">DESCRIPTION</span></span>
<span data-ttu-id="f28f2-106">Командлет **Set-AzVMSqlServerExtension** задает серверное расширение AzureSQL на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f28f2-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="f28f2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f28f2-107">EXAMPLES</span></span>

### <span data-ttu-id="f28f2-108">Пример 1: Настройка автоматических параметров исправлений на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="f28f2-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="f28f2-109">Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="f28f2-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="f28f2-110">Эта команда хранит конфигурацию в переменной $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="f28f2-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="f28f2-111">Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 с помощью командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f28f2-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="f28f2-112">Команда передает этот объект в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f28f2-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="f28f2-113">Текущий командлет задает параметры автоматического исправления в $AutoPatchingConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f28f2-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="f28f2-114">Команда передает виртуальную машину командлету Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f28f2-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="f28f2-115">Пример 2: Настройка параметров автоматического резервного копирования на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="f28f2-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="f28f2-116">Первая команда создает объект конфигурации с помощью командлета **New-AzureVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="f28f2-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="f28f2-117">Эта команда хранит конфигурацию в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="f28f2-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="f28f2-118">Вторая команда получает виртуальную машину с именем VirtualMachine11 в службе с именем Service02 и передает ее в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="f28f2-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="f28f2-119">Текущий командлет задает параметры автоматического резервного копирования в $AutoBackupConfig для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f28f2-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="f28f2-120">Команда передает виртуальную машину командлету Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f28f2-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="f28f2-121">Пример 3: отключение расширения SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="f28f2-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="f28f2-122">Эта команда получает виртуальную машину с именем VirtualMachine08 на Service03, а затем передает ее в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="f28f2-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="f28f2-123">Команда отключает расширение виртуальной машины SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f28f2-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="f28f2-124">Пример 4: удаление расширения SQL Server на определенной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="f28f2-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="f28f2-125">Эта команда получает виртуальную машину с именем VirtualMachine08 на Service03, а затем передает ее в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="f28f2-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="f28f2-126">Команда удаляет расширение виртуальной машины SQL Server на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f28f2-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="f28f2-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f28f2-127">PARAMETERS</span></span>

### <span data-ttu-id="f28f2-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="f28f2-128">-AutoBackupSettings</span></span>
<span data-ttu-id="f28f2-129">Задает параметры автоматического резервного копирования SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f28f2-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="f28f2-130">Чтобы создать объект **AutoBackupSettings** , используйте командлет New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="f28f2-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="f28f2-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="f28f2-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="f28f2-132">Задает параметры автоматического исправления SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f28f2-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="f28f2-133">Чтобы создать объект **AutoPatchingSettings** , используйте командлет New-AzureVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="f28f2-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="f28f2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28f2-134">-DefaultProfile</span></span>
<span data-ttu-id="f28f2-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f28f2-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f28f2-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="f28f2-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="f28f2-137">-Location</span><span class="sxs-lookup"><span data-stu-id="f28f2-137">-Location</span></span>
<span data-ttu-id="f28f2-138">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f28f2-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f28f2-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f28f2-139">-Name</span></span>
<span data-ttu-id="f28f2-140">Указывает имя сервера SQL Server, на котором находится расширение.</span><span class="sxs-lookup"><span data-stu-id="f28f2-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="f28f2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28f2-141">-ResourceGroupName</span></span>
<span data-ttu-id="f28f2-142">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f28f2-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f28f2-143">-Version</span><span class="sxs-lookup"><span data-stu-id="f28f2-143">-Version</span></span>
<span data-ttu-id="f28f2-144">Указывает версию расширения SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f28f2-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="f28f2-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="f28f2-145">-VMName</span></span>
<span data-ttu-id="f28f2-146">Указывает имя виртуальной машины, на которой этот командлет задает расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f28f2-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="f28f2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28f2-147">CommonParameters</span></span>
<span data-ttu-id="f28f2-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f28f2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28f2-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f28f2-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28f2-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f28f2-150">INPUTS</span></span>

### <span data-ttu-id="f28f2-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="f28f2-151">None</span></span>
<span data-ttu-id="f28f2-152">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f28f2-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f28f2-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f28f2-153">OUTPUTS</span></span>

### <span data-ttu-id="f28f2-154">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f28f2-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f28f2-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="f28f2-155">NOTES</span></span>

## <span data-ttu-id="f28f2-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f28f2-156">RELATED LINKS</span></span>

[<span data-ttu-id="f28f2-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f28f2-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f28f2-158">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f28f2-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="f28f2-159">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="f28f2-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="f28f2-160">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="f28f2-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="f28f2-161">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f28f2-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="f28f2-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f28f2-162">Update-AzVM</span></span>](./Update-AzVM.md)


