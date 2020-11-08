---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244260"
---
# <span data-ttu-id="886d2-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="886d2-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="886d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="886d2-102">SYNOPSIS</span></span>
<span data-ttu-id="886d2-103">Создание политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="886d2-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="886d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="886d2-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="886d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="886d2-105">DESCRIPTION</span></span>
<span data-ttu-id="886d2-106">Командлет **New-AzRecoveryServicesBackupProtectionPolicy** создает политику защиты резервного копирования в хранилище.</span><span class="sxs-lookup"><span data-stu-id="886d2-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="886d2-107">Политика защиты связана по крайней мере с одной политикой хранения.</span><span class="sxs-lookup"><span data-stu-id="886d2-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="886d2-108">Политика хранения определяет, как долго будет храниться резервная копия Azure.</span><span class="sxs-lookup"><span data-stu-id="886d2-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="886d2-109">Вы можете использовать командлет Get-AzRecoveryServicesBackupRetentionPolicyObject, чтобы получить политику хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="886d2-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="886d2-110">Вы также можете использовать командлет Get-AzRecoveryServicesBackupSchedulePolicyObject для получения политики расписания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="886d2-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="886d2-111">Объекты **SchedulePolicy** и **RetentionPolicy** используются в качестве входных данных для командлета **New-AzRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="886d2-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="886d2-112">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="886d2-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="886d2-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="886d2-113">EXAMPLES</span></span>

### <span data-ttu-id="886d2-114">Пример 1: Создание политики защиты резервных копий</span><span class="sxs-lookup"><span data-stu-id="886d2-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="886d2-115">Первая команда получает базовый **SchedulePolicyObject** и сохраняет ее в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="886d2-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="886d2-116">Вторая команда удаляет все запланированные значения времени выполнения из политики расписания в $SchPol.</span><span class="sxs-lookup"><span data-stu-id="886d2-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="886d2-117">Третья команда использует командлет Get-Date, чтобы получить текущую дату и время.</span><span class="sxs-lookup"><span data-stu-id="886d2-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="886d2-118">Четвертая команда добавляет текущую дату и время в $Dt как запланированное время выполнения для политики расписания.</span><span class="sxs-lookup"><span data-stu-id="886d2-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="886d2-119">Пятая команда получает базовый объект **RetentionPolicy** , а затем сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="886d2-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="886d2-120">Шестая команда задает для политики продолжительность хранения 365 дней.</span><span class="sxs-lookup"><span data-stu-id="886d2-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="886d2-121">Последняя команда создает объект **BackupProtectionPolicy** на основе политики расписания и хранения, созданной предыдущими командами.</span><span class="sxs-lookup"><span data-stu-id="886d2-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="886d2-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="886d2-122">Example 2</span></span>

<span data-ttu-id="886d2-123">Создание политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="886d2-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="886d2-124">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="886d2-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="886d2-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="886d2-125">PARAMETERS</span></span>

### <span data-ttu-id="886d2-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="886d2-126">-BackupManagementType</span></span>
<span data-ttu-id="886d2-127">Класс защищаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="886d2-127">The class of resources being protected.</span></span> <span data-ttu-id="886d2-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="886d2-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="886d2-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="886d2-129">AzureVM</span></span> 
- <span data-ttu-id="886d2-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="886d2-130">AzureStorage</span></span>
- <span data-ttu-id="886d2-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="886d2-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="886d2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="886d2-132">-DefaultProfile</span></span>
<span data-ttu-id="886d2-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="886d2-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="886d2-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="886d2-134">-Name</span></span>
<span data-ttu-id="886d2-135">Указывает имя политики.</span><span class="sxs-lookup"><span data-stu-id="886d2-135">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886d2-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="886d2-136">-RetentionPolicy</span></span>
<span data-ttu-id="886d2-137">Указывает базовый объект **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="886d2-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="886d2-138">Вы можете использовать командлет Get-AzRecoveryServicesBackupRetentionPolicyObject, чтобы получить объект **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="886d2-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="886d2-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="886d2-139">-SchedulePolicy</span></span>
<span data-ttu-id="886d2-140">Указывает базовый объект **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="886d2-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="886d2-141">Вы можете использовать командлет Get-AzRecoveryServicesBackupSchedulePolicyObject, чтобы получить объект **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="886d2-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="886d2-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="886d2-142">-VaultId</span></span>
<span data-ttu-id="886d2-143">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="886d2-143">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="886d2-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="886d2-144">-WorkloadType</span></span>
<span data-ttu-id="886d2-145">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="886d2-145">Workload type of the resource.</span></span> <span data-ttu-id="886d2-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="886d2-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="886d2-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="886d2-147">AzureVM</span></span> 
- <span data-ttu-id="886d2-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="886d2-148">AzureFiles</span></span>
- <span data-ttu-id="886d2-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="886d2-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="886d2-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="886d2-150">-Confirm</span></span>
<span data-ttu-id="886d2-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="886d2-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="886d2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="886d2-152">-WhatIf</span></span>
<span data-ttu-id="886d2-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="886d2-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="886d2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="886d2-154">CommonParameters</span></span>
<span data-ttu-id="886d2-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="886d2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="886d2-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="886d2-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="886d2-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="886d2-157">INPUTS</span></span>

### <span data-ttu-id="886d2-158">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. WorkloadType</span><span class="sxs-lookup"><span data-stu-id="886d2-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="886d2-159">System. Nullable "1 [[Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты: Models. BackupManagementType, Microsoft. Azure. Backup. командлеты, Version = 1.0.0.0, Culture</span><span class="sxs-lookup"><span data-stu-id="886d2-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="886d2-160">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="886d2-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="886d2-161">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="886d2-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="886d2-162">System. String</span><span class="sxs-lookup"><span data-stu-id="886d2-162">System.String</span></span>

## <span data-ttu-id="886d2-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="886d2-163">OUTPUTS</span></span>

### <span data-ttu-id="886d2-164">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="886d2-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="886d2-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="886d2-165">NOTES</span></span>

## <span data-ttu-id="886d2-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="886d2-166">RELATED LINKS</span></span>

[<span data-ttu-id="886d2-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="886d2-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="886d2-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="886d2-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="886d2-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="886d2-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="886d2-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="886d2-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="886d2-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="886d2-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="886d2-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="886d2-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


