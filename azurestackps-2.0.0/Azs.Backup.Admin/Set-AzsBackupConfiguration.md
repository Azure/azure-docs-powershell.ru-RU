---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911674"
---
# <span data-ttu-id="37a65-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a65-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="37a65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37a65-102">SYNOPSIS</span></span>
<span data-ttu-id="37a65-103">Обновите расположение резервной копии.</span><span class="sxs-lookup"><span data-stu-id="37a65-103">Update a backup location.</span></span>

## <span data-ttu-id="37a65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37a65-104">SYNTAX</span></span>

### <span data-ttu-id="37a65-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37a65-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="37a65-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="37a65-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="37a65-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37a65-107">DESCRIPTION</span></span>
<span data-ttu-id="37a65-108">Обновите расположение резервной копии.</span><span class="sxs-lookup"><span data-stu-id="37a65-108">Update a backup location.</span></span>

## <span data-ttu-id="37a65-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37a65-109">EXAMPLES</span></span>

### <span data-ttu-id="37a65-110">Пример 1: Настройка конфигурации резервной копии</span><span class="sxs-lookup"><span data-stu-id="37a65-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="37a65-111">Настройте параметры резервного копирования стеков Azure.</span><span class="sxs-lookup"><span data-stu-id="37a65-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="37a65-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37a65-112">PARAMETERS</span></span>

### <span data-ttu-id="37a65-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37a65-113">-AsJob</span></span>
<span data-ttu-id="37a65-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="37a65-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-115">-Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="37a65-115">-Backup</span></span>
<span data-ttu-id="37a65-116">Сведения о расположении резервной копии.</span><span class="sxs-lookup"><span data-stu-id="37a65-116">Information about the backup location.</span></span>
<span data-ttu-id="37a65-117">Для конструирования щелкните раздел заметок о свойствах резервного копирования и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="37a65-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="37a65-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="37a65-119">Интервал (в часах) для частоты, из-за которой планировщик выполняет резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="37a65-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="37a65-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="37a65-121">Срок хранения (в днях) для резервного копирования в месте хранения.</span><span class="sxs-lookup"><span data-stu-id="37a65-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a65-122">-DefaultProfile</span></span>
<span data-ttu-id="37a65-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37a65-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-124">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="37a65-124">-EncryptionCertPath</span></span>
<span data-ttu-id="37a65-125">Путь к файлу сертификата шифрования с открытым ключом (CER).</span><span class="sxs-lookup"><span data-stu-id="37a65-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="37a65-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="37a65-127">Значение true, если включен планировщик резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="37a65-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-128">-Location</span><span class="sxs-lookup"><span data-stu-id="37a65-128">-Location</span></span>
<span data-ttu-id="37a65-129">Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="37a65-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="37a65-130">-NoWait</span></span>
<span data-ttu-id="37a65-131">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="37a65-131">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-132">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="37a65-132">-Password</span></span>
<span data-ttu-id="37a65-133">Пароль для доступа к расположению.</span><span class="sxs-lookup"><span data-stu-id="37a65-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-134">-Path</span><span class="sxs-lookup"><span data-stu-id="37a65-134">-Path</span></span>
<span data-ttu-id="37a65-135">Путь к расположению обновления</span><span class="sxs-lookup"><span data-stu-id="37a65-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a65-136">-ResourceGroupName</span></span>
<span data-ttu-id="37a65-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37a65-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37a65-138">-SubscriptionId</span></span>
<span data-ttu-id="37a65-139">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37a65-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="37a65-140">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="37a65-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="37a65-141">-Tag</span></span>
<span data-ttu-id="37a65-142">Список пар "ключевые значения".</span><span class="sxs-lookup"><span data-stu-id="37a65-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="37a65-143">-UserName</span></span>
<span data-ttu-id="37a65-144">Имя пользователя для доступа к расположению.</span><span class="sxs-lookup"><span data-stu-id="37a65-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37a65-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37a65-145">-Confirm</span></span>
<span data-ttu-id="37a65-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37a65-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37a65-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37a65-147">-WhatIf</span></span>
<span data-ttu-id="37a65-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37a65-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37a65-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37a65-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37a65-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a65-150">CommonParameters</span></span>
<span data-ttu-id="37a65-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37a65-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a65-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37a65-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a65-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37a65-153">INPUTS</span></span>

### <span data-ttu-id="37a65-154">Microsoft. Azure. PowerShell. командлеты. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="37a65-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="37a65-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37a65-155">OUTPUTS</span></span>

### <span data-ttu-id="37a65-156">Microsoft. Azure. PowerShell. командлеты. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="37a65-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="37a65-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="37a65-157">NOTES</span></span>

<span data-ttu-id="37a65-158">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="37a65-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37a65-159">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37a65-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="37a65-160">BACKUP <IBackupLocation> : сведения о расположении резервной копии.</span><span class="sxs-lookup"><span data-stu-id="37a65-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="37a65-161">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="37a65-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="37a65-162">`[Tag <IResourceTags>]`: Список пар значений ключа.</span><span class="sxs-lookup"><span data-stu-id="37a65-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="37a65-163">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="37a65-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="37a65-164">`[BackupFrequencyInHours <Int32?>]`: Интервал в часах для частоты, из-за которой планировщик выполняет резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="37a65-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="37a65-165">`[BackupRetentionPeriodInDays <Int32?>]`: Срок хранения (в днях) для обратной связи в местоположении хранения.</span><span class="sxs-lookup"><span data-stu-id="37a65-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="37a65-166">`[EncryptionCertBase64 <String>]`: Необработанные данные base64 для сертификата шифрования резервной копии.</span><span class="sxs-lookup"><span data-stu-id="37a65-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="37a65-167">`[IsBackupSchedulerEnabled <Boolean?>]`: Значение true, если включен планировщик резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="37a65-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="37a65-168">`[Password <String>]`: Пароль для доступа к расположению.</span><span class="sxs-lookup"><span data-stu-id="37a65-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="37a65-169">`[Path <String>]`: Путь к расположению обновления</span><span class="sxs-lookup"><span data-stu-id="37a65-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="37a65-170">`[UserName <String>]`: Имя пользователя для доступа к расположению.</span><span class="sxs-lookup"><span data-stu-id="37a65-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="37a65-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37a65-171">RELATED LINKS</span></span>

