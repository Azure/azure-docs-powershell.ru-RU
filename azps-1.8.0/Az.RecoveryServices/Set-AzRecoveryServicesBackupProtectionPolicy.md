---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1f7dcd013bb91b8ba209cf3f7b031a90f7bb49cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729605"
---
# <span data-ttu-id="1a8da-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a8da-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1a8da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a8da-102">SYNOPSIS</span></span>
<span data-ttu-id="1a8da-103">Изменение политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="1a8da-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="1a8da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a8da-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a8da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a8da-105">DESCRIPTION</span></span>
<span data-ttu-id="1a8da-106">Командлет **Set-AzBackupProtectionPolicy** изменяет существующую политику защиты резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="1a8da-106">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="1a8da-107">Вы можете изменить расписание архивации и компоненты политики хранения.</span><span class="sxs-lookup"><span data-stu-id="1a8da-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="1a8da-108">Все внесенные изменения повлияют на резервное копирование и хранение элементов, связанных с политикой.</span><span class="sxs-lookup"><span data-stu-id="1a8da-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="1a8da-109">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="1a8da-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1a8da-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a8da-110">EXAMPLES</span></span>

### <span data-ttu-id="1a8da-111">Пример 1: изменение политики защиты резервной копии</span><span class="sxs-lookup"><span data-stu-id="1a8da-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="1a8da-112">Первая команда получает базовый объект SchedulePolicy, а затем сохраняет его в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="1a8da-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="1a8da-113">Вторая команда удаляет все запланированные значения времени выполнения из политики расписания в $SchPol.</span><span class="sxs-lookup"><span data-stu-id="1a8da-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="1a8da-114">Третья команда использует командлет Get-Date, чтобы получить текущую дату и время, а затем сохраняет их в переменной $DT.</span><span class="sxs-lookup"><span data-stu-id="1a8da-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="1a8da-115">Четвертая команда добавляет дату и время в $DT к времени выполнения расписания для политики расписания.</span><span class="sxs-lookup"><span data-stu-id="1a8da-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="1a8da-116">Пятое приложение получает базовый объект политики хранения и сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="1a8da-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="1a8da-117">Шестая команда задает продолжительность хранения в 365 дней.</span><span class="sxs-lookup"><span data-stu-id="1a8da-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="1a8da-118">Седьмая команда получает политику защиты резервного копирования с именем NewPolicy и сохраняет ее в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="1a8da-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="1a8da-119">Последняя команда изменяет политику защиты резервных копий в $Pol с помощью политики расписания в $SchPol и политики хранения в $RetPol.</span><span class="sxs-lookup"><span data-stu-id="1a8da-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="1a8da-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a8da-120">PARAMETERS</span></span>

### <span data-ttu-id="1a8da-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a8da-121">-DefaultProfile</span></span>
<span data-ttu-id="1a8da-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a8da-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a8da-123">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="1a8da-123">-Policy</span></span>
<span data-ttu-id="1a8da-124">Задает политику защиты резервного копирования, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1a8da-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="1a8da-125">Чтобы получить объект **BackupProtectionPolicy** , используйте командлет Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="1a8da-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="1a8da-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a8da-126">-RetentionPolicy</span></span>
<span data-ttu-id="1a8da-127">Указывает базовую политику хранения.</span><span class="sxs-lookup"><span data-stu-id="1a8da-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="1a8da-128">Чтобы получить объект **RetentionPolicy** , используйте командлет Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="1a8da-128">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8da-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="1a8da-129">-SchedulePolicy</span></span>
<span data-ttu-id="1a8da-130">Указывает базовый объект политики расписания.</span><span class="sxs-lookup"><span data-stu-id="1a8da-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="1a8da-131">Чтобы получить объект **SchedulePolicy** , используйте объект Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="1a8da-131">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8da-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1a8da-132">-VaultId</span></span>
<span data-ttu-id="1a8da-133">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="1a8da-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1a8da-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a8da-134">-Confirm</span></span>
<span data-ttu-id="1a8da-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1a8da-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a8da-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a8da-136">-WhatIf</span></span>
<span data-ttu-id="1a8da-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1a8da-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a8da-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a8da-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a8da-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a8da-139">CommonParameters</span></span>
<span data-ttu-id="1a8da-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a8da-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a8da-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a8da-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a8da-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a8da-142">INPUTS</span></span>

### <span data-ttu-id="1a8da-143">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1a8da-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="1a8da-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1a8da-144">System.String</span></span>

## <span data-ttu-id="1a8da-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a8da-145">OUTPUTS</span></span>

### <span data-ttu-id="1a8da-146">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="1a8da-146">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="1a8da-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a8da-147">NOTES</span></span>

## <span data-ttu-id="1a8da-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a8da-148">RELATED LINKS</span></span>

[<span data-ttu-id="1a8da-149">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a8da-149">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1a8da-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1a8da-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="1a8da-151">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a8da-151">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1a8da-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a8da-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


