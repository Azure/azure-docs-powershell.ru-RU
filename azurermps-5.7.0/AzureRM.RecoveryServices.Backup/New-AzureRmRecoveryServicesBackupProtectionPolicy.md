---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9834236a72a68f64cc9b19d6576e56102f96b13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558912"
---
# <span data-ttu-id="dc083-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc083-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="dc083-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc083-102">SYNOPSIS</span></span>
<span data-ttu-id="dc083-103">Создание политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="dc083-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc083-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc083-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc083-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc083-105">DESCRIPTION</span></span>
<span data-ttu-id="dc083-106">Командлет **New-AzureRmRecoveryServicesBackupProtectionPolicy** создает политику защиты резервного копирования в хранилище.</span><span class="sxs-lookup"><span data-stu-id="dc083-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="dc083-107">Политика защиты связана по крайней мере с одной политикой хранения.</span><span class="sxs-lookup"><span data-stu-id="dc083-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="dc083-108">Политика хранения определяет, как долго будет храниться резервная копия Azure.</span><span class="sxs-lookup"><span data-stu-id="dc083-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="dc083-109">Вы можете использовать командлет Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, чтобы получить политику хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dc083-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="dc083-110">Вы также можете использовать командлет Get-AzureRmRecoveryServicesBackupSchedulePolicyObject для получения политики расписания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dc083-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="dc083-111">Объекты **SchedulePolicy** и **RetentionPolicy** используются в качестве входных данных для командлета **New-AzureRmRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="dc083-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="dc083-112">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="dc083-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="dc083-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc083-113">EXAMPLES</span></span>

### <span data-ttu-id="dc083-114">Пример 1: Создание политики защиты резервных копий</span><span class="sxs-lookup"><span data-stu-id="dc083-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="dc083-115">Первая команда получает базовый **SchedulePolicyObject** и сохраняет ее в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="dc083-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="dc083-116">Вторая команда удаляет все запланированные значения времени выполнения из политики расписания в $SchPol.</span><span class="sxs-lookup"><span data-stu-id="dc083-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="dc083-117">Третья команда использует командлет Get-Date, чтобы получить текущую дату и время.</span><span class="sxs-lookup"><span data-stu-id="dc083-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="dc083-118">Четвертая команда добавляет текущую дату и время в $Dt как запланированное время выполнения для политики расписания.</span><span class="sxs-lookup"><span data-stu-id="dc083-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="dc083-119">Пятая команда получает базовый объект **RetentionPolicy** , а затем сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="dc083-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="dc083-120">Шестая команда задает для политики продолжительность хранения 365 дней.</span><span class="sxs-lookup"><span data-stu-id="dc083-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="dc083-121">Последняя команда создает объект **BackupProtectionPolicy** на основе политики расписания и хранения, созданной предыдущими командами.</span><span class="sxs-lookup"><span data-stu-id="dc083-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="dc083-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc083-122">PARAMETERS</span></span>

### <span data-ttu-id="dc083-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="dc083-123">-BackupManagementType</span></span>
<span data-ttu-id="dc083-124">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="dc083-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="dc083-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dc083-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dc083-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="dc083-126">AzureVM</span></span> 
- <span data-ttu-id="dc083-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="dc083-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc083-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc083-128">-DefaultProfile</span></span>
<span data-ttu-id="dc083-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc083-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc083-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc083-130">-Name</span></span>
<span data-ttu-id="dc083-131">Указывает имя политики.</span><span class="sxs-lookup"><span data-stu-id="dc083-131">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc083-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc083-132">-RetentionPolicy</span></span>
<span data-ttu-id="dc083-133">Указывает базовый объект **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="dc083-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="dc083-134">Вы можете использовать командлет Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, чтобы получить объект **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="dc083-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc083-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="dc083-135">-SchedulePolicy</span></span>
<span data-ttu-id="dc083-136">Указывает базовый объект **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="dc083-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="dc083-137">Вы можете использовать командлет Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, чтобы получить объект **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="dc083-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc083-138">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="dc083-138">-WorkloadType</span></span>
<span data-ttu-id="dc083-139">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="dc083-139">Specifies the workload type.</span></span>
<span data-ttu-id="dc083-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dc083-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dc083-141">AzureVM</span><span class="sxs-lookup"><span data-stu-id="dc083-141">AzureVM</span></span> 
- <span data-ttu-id="dc083-142">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="dc083-142">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc083-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc083-143">-Confirm</span></span>
<span data-ttu-id="dc083-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc083-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc083-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc083-145">-WhatIf</span></span>
<span data-ttu-id="dc083-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc083-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc083-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc083-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc083-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc083-148">CommonParameters</span></span>
<span data-ttu-id="dc083-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc083-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc083-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc083-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc083-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc083-151">INPUTS</span></span>

### <span data-ttu-id="dc083-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="dc083-152">None</span></span>
<span data-ttu-id="dc083-153">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="dc083-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc083-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc083-154">OUTPUTS</span></span>

### <span data-ttu-id="dc083-155">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="dc083-155">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="dc083-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc083-156">NOTES</span></span>

## <span data-ttu-id="dc083-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc083-157">RELATED LINKS</span></span>

[<span data-ttu-id="dc083-158">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="dc083-158">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="dc083-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc083-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="dc083-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="dc083-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="dc083-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="dc083-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="dc083-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc083-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="dc083-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc083-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


