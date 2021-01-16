---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409292"
---
# <span data-ttu-id="d9da4-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d9da4-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="d9da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9da4-102">SYNOPSIS</span></span>
<span data-ttu-id="d9da4-103">Изменяет политику защиты от резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d9da4-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="d9da4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d9da4-104">SYNTAX</span></span>

### <span data-ttu-id="d9da4-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="d9da4-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9da4-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="d9da4-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9da4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9da4-107">DESCRIPTION</span></span>
<span data-ttu-id="d9da4-108">**Cmdlet Set-AzRecoveryServicesBackupProtectionPolicy** изменяет существующую политику защиты резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="d9da4-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="d9da4-109">Вы можете изменить расписание резервного копирования и компоненты политики хранения.</span><span class="sxs-lookup"><span data-stu-id="d9da4-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="d9da4-110">Любые внесенные изменения влияют на резервное копирование и хранение элементов, связанных с политикой.</span><span class="sxs-lookup"><span data-stu-id="d9da4-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="d9da4-111">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="d9da4-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d9da4-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d9da4-112">EXAMPLES</span></span>

### <span data-ttu-id="d9da4-113">Пример 1. Изменение политики защиты от резервного копирования</span><span class="sxs-lookup"><span data-stu-id="d9da4-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="d9da4-114">Ниже подробно описаны действия по изменению политики защиты.</span><span class="sxs-lookup"><span data-stu-id="d9da4-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="d9da4-115">Получите базовые schedulePolicyObject и Base RetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="d9da4-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="d9da4-116">Храните их в определенной переменной.</span><span class="sxs-lookup"><span data-stu-id="d9da4-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="d9da4-117">Заданы различные параметры объекта календарного плана и политики хранения в рамках своих требований.</span><span class="sxs-lookup"><span data-stu-id="d9da4-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="d9da4-118">Например, в примере выше настроена еженедельная политика защиты.</span><span class="sxs-lookup"><span data-stu-id="d9da4-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="d9da4-119">Следовательно, мы изменили периодичность расписания на "Еженедельно", а также обновили время его запуска.</span><span class="sxs-lookup"><span data-stu-id="d9da4-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="d9da4-120">В объекте политики хранения были обновлены еженедельные сроки хранения и установлен правильный флажок "Включено еженедельное расписание".</span><span class="sxs-lookup"><span data-stu-id="d9da4-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="d9da4-121">Если вы хотите задать политику на день, установите для флажка "Ежедневное расписание включено" значение true и задав соответствующие значения для других параметров объекта.</span><span class="sxs-lookup"><span data-stu-id="d9da4-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="d9da4-122">Получите политику защиты резервного копирования, которую вы хотите изменить, и храните ее в переменной.</span><span class="sxs-lookup"><span data-stu-id="d9da4-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="d9da4-123">В примере выше мы извлекли политику резервного копирования с именем TestPolicy, которую мы хотели изменить.</span><span class="sxs-lookup"><span data-stu-id="d9da4-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="d9da4-124">Измените политику защиты резервного копирования, восстановленную на шаге 3, используя измененный объект политики расписания и объект политики хранения.</span><span class="sxs-lookup"><span data-stu-id="d9da4-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="d9da4-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9da4-125">PARAMETERS</span></span>

### <span data-ttu-id="d9da4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9da4-126">-DefaultProfile</span></span>
<span data-ttu-id="d9da4-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9da4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9da4-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="d9da4-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="d9da4-129">Параметр переключения, указывающий, нужно ли повторно обновлять политику для сбойных элементов.</span><span class="sxs-lookup"><span data-stu-id="d9da4-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9da4-130">-Политика</span><span class="sxs-lookup"><span data-stu-id="d9da4-130">-Policy</span></span>
<span data-ttu-id="d9da4-131">Определяет политику защиты резервного копирования, которая изменяется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9da4-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="d9da4-132">Чтобы получить объект **BackupProtectionPolicy,** используйте Get-AzRecoveryServicesBackupProtectionPolicy..</span><span class="sxs-lookup"><span data-stu-id="d9da4-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9da4-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d9da4-133">-RetentionPolicy</span></span>
<span data-ttu-id="d9da4-134">Определяет базовую политику хранения.</span><span class="sxs-lookup"><span data-stu-id="d9da4-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="d9da4-135">Чтобы получить объект **RetentionPolicy,** используйте Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="d9da4-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9da4-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="d9da4-136">-SchedulePolicy</span></span>
<span data-ttu-id="d9da4-137">Указывает объект политики базового расписания.</span><span class="sxs-lookup"><span data-stu-id="d9da4-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="d9da4-138">Чтобы получить объект **SchedulePolicy,** используйте Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="d9da4-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9da4-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d9da4-139">-VaultId</span></span>
<span data-ttu-id="d9da4-140">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d9da4-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d9da4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9da4-141">-Confirm</span></span>
<span data-ttu-id="d9da4-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9da4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9da4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9da4-143">-WhatIf</span></span>
<span data-ttu-id="d9da4-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9da4-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="d9da4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9da4-145">CommonParameters</span></span>
<span data-ttu-id="d9da4-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9da4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9da4-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9da4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9da4-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9da4-148">INPUTS</span></span>

### <span data-ttu-id="d9da4-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="d9da4-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="d9da4-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d9da4-150">System.String</span></span>

## <span data-ttu-id="d9da4-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d9da4-151">OUTPUTS</span></span>

### <span data-ttu-id="d9da4-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="d9da4-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d9da4-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d9da4-153">NOTES</span></span>

## <span data-ttu-id="d9da4-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9da4-154">RELATED LINKS</span></span>

[<span data-ttu-id="d9da4-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d9da4-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d9da4-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d9da4-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="d9da4-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d9da4-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d9da4-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d9da4-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


