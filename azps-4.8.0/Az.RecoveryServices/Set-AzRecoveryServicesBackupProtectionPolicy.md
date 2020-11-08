---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f9cd7064c1949639526f2e7b84f01fb6355b584f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244020"
---
# <span data-ttu-id="92233-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92233-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="92233-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92233-102">SYNOPSIS</span></span>
<span data-ttu-id="92233-103">Изменение политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="92233-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="92233-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92233-104">SYNTAX</span></span>

### <span data-ttu-id="92233-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="92233-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92233-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="92233-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92233-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92233-107">DESCRIPTION</span></span>
<span data-ttu-id="92233-108">Командлет **Set-AzRecoveryServicesBackupProtectionPolicy** изменяет существующую политику защиты резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="92233-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="92233-109">Вы можете изменить расписание архивации и компоненты политики хранения.</span><span class="sxs-lookup"><span data-stu-id="92233-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="92233-110">Все внесенные изменения повлияют на резервное копирование и хранение элементов, связанных с политикой.</span><span class="sxs-lookup"><span data-stu-id="92233-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="92233-111">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="92233-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="92233-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92233-112">EXAMPLES</span></span>

### <span data-ttu-id="92233-113">Пример 1: изменение политики защиты резервной копии</span><span class="sxs-lookup"><span data-stu-id="92233-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="92233-114">Первая команда получает базовый объект SchedulePolicy, а затем сохраняет его в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="92233-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="92233-115">Вторая команда удаляет все запланированные значения времени выполнения из политики расписания в $SchPol.</span><span class="sxs-lookup"><span data-stu-id="92233-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="92233-116">Третья команда использует командлет Get-Date, чтобы получить текущую дату и время, а затем сохраняет их в переменной $DT.</span><span class="sxs-lookup"><span data-stu-id="92233-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="92233-117">Четвертая команда добавляет дату и время в $DT к времени выполнения расписания для политики расписания.</span><span class="sxs-lookup"><span data-stu-id="92233-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="92233-118">Пятое приложение получает базовый объект политики хранения и сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="92233-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="92233-119">Шестая команда задает продолжительность хранения в 365 дней.</span><span class="sxs-lookup"><span data-stu-id="92233-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="92233-120">Седьмая команда получает политику защиты резервного копирования с именем NewPolicy и сохраняет ее в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="92233-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="92233-121">Восьма и девятка задает параметры группы ресурсов, связанные с политикой, в которой хранятся точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="92233-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="92233-122">Последняя команда изменяет политику защиты резервных копий в $Pol с помощью политики расписания в $SchPol и политики хранения в $RetPol.</span><span class="sxs-lookup"><span data-stu-id="92233-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="92233-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92233-123">PARAMETERS</span></span>

### <span data-ttu-id="92233-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92233-124">-DefaultProfile</span></span>
<span data-ttu-id="92233-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92233-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92233-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="92233-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="92233-127">Параметр Switch, указывающий, следует ли повторять обновление политики для неудачных элементов.</span><span class="sxs-lookup"><span data-stu-id="92233-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="92233-128">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="92233-128">-Policy</span></span>
<span data-ttu-id="92233-129">Задает политику защиты резервного копирования, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92233-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="92233-130">Чтобы получить объект **BackupProtectionPolicy** , используйте командлет Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="92233-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="92233-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="92233-131">-RetentionPolicy</span></span>
<span data-ttu-id="92233-132">Указывает базовую политику хранения.</span><span class="sxs-lookup"><span data-stu-id="92233-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="92233-133">Чтобы получить объект **RetentionPolicy** , используйте командлет Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="92233-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="92233-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="92233-134">-SchedulePolicy</span></span>
<span data-ttu-id="92233-135">Указывает базовый объект политики расписания.</span><span class="sxs-lookup"><span data-stu-id="92233-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="92233-136">Чтобы получить объект **SchedulePolicy** , используйте объект Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="92233-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="92233-137">-VaultId</span><span class="sxs-lookup"><span data-stu-id="92233-137">-VaultId</span></span>
<span data-ttu-id="92233-138">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="92233-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="92233-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92233-139">-Confirm</span></span>
<span data-ttu-id="92233-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92233-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92233-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92233-141">-WhatIf</span></span>
<span data-ttu-id="92233-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92233-142">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="92233-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92233-143">CommonParameters</span></span>
<span data-ttu-id="92233-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92233-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92233-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92233-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92233-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92233-146">INPUTS</span></span>

### <span data-ttu-id="92233-147">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="92233-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="92233-148">System. String</span><span class="sxs-lookup"><span data-stu-id="92233-148">System.String</span></span>

## <span data-ttu-id="92233-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92233-149">OUTPUTS</span></span>

### <span data-ttu-id="92233-150">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="92233-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="92233-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="92233-151">NOTES</span></span>

## <span data-ttu-id="92233-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92233-152">RELATED LINKS</span></span>

[<span data-ttu-id="92233-153">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92233-153">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="92233-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="92233-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="92233-155">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92233-155">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="92233-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92233-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


