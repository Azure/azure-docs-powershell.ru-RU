---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 5a60320736e65fae83547bbf9b2825979f73601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558908"
---
# <span data-ttu-id="63fed-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="63fed-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="63fed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63fed-102">SYNOPSIS</span></span>
<span data-ttu-id="63fed-103">Изменение политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="63fed-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63fed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63fed-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63fed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63fed-105">DESCRIPTION</span></span>
<span data-ttu-id="63fed-106">Командлет **Set-AzureRmBackupProtectionPolicy** изменяет существующую политику защиты резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="63fed-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="63fed-107">Вы можете изменить расписание архивации и компоненты политики хранения.</span><span class="sxs-lookup"><span data-stu-id="63fed-107">You can modify the Backup schedule and retention policy components.</span></span>

<span data-ttu-id="63fed-108">Все внесенные изменения повлияют на резервное копирование и хранение элементов, связанных с политикой.</span><span class="sxs-lookup"><span data-stu-id="63fed-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>

<span data-ttu-id="63fed-109">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="63fed-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="63fed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63fed-110">EXAMPLES</span></span>

### <span data-ttu-id="63fed-111">Пример 1: изменение политики защиты резервной копии</span><span class="sxs-lookup"><span data-stu-id="63fed-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="63fed-112">Первая команда получает базовый объект SchedulePolicy, а затем сохраняет его в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="63fed-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="63fed-113">Вторая команда удаляет все запланированные значения времени выполнения из политики расписания в $SchPol.</span><span class="sxs-lookup"><span data-stu-id="63fed-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="63fed-114">Третья команда использует командлет Get-Date, чтобы получить текущую дату и время, а затем сохраняет их в переменной $DT.</span><span class="sxs-lookup"><span data-stu-id="63fed-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="63fed-115">Четвертая команда добавляет дату и время в $DT к времени выполнения расписания для политики расписания.</span><span class="sxs-lookup"><span data-stu-id="63fed-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>

<span data-ttu-id="63fed-116">Пятое приложение получает базовый объект политики хранения и сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="63fed-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="63fed-117">Шестая команда задает продолжительность хранения в 365 дней.</span><span class="sxs-lookup"><span data-stu-id="63fed-117">The sixth command sets the retention duration to 365 days.</span></span>

<span data-ttu-id="63fed-118">Седьмая команда получает политику защиты резервного копирования с именем NewPolicy и сохраняет ее в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="63fed-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="63fed-119">Последняя команда изменяет политику защиты резервных копий в $Pol с помощью политики расписания в $SchPol и политики хранения в $RetPol.</span><span class="sxs-lookup"><span data-stu-id="63fed-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="63fed-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63fed-120">PARAMETERS</span></span>

### <span data-ttu-id="63fed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fed-121">-DefaultProfile</span></span>
<span data-ttu-id="63fed-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63fed-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63fed-123">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="63fed-123">-Policy</span></span>
<span data-ttu-id="63fed-124">Задает политику защиты резервного копирования, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="63fed-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="63fed-125">Чтобы получить объект **BackupProtectionPolicy** , используйте командлет Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="63fed-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63fed-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="63fed-126">-RetentionPolicy</span></span>
<span data-ttu-id="63fed-127">Указывает базовую политику хранения.</span><span class="sxs-lookup"><span data-stu-id="63fed-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="63fed-128">Чтобы получить объект **RetentionPolicy** , используйте командлет Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="63fed-128">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fed-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="63fed-129">-SchedulePolicy</span></span>
<span data-ttu-id="63fed-130">Указывает базовый объект политики расписания.</span><span class="sxs-lookup"><span data-stu-id="63fed-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="63fed-131">Чтобы получить объект **SchedulePolicy** , используйте объект Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="63fed-131">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fed-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63fed-132">-Confirm</span></span>
<span data-ttu-id="63fed-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63fed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63fed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63fed-134">-WhatIf</span></span>
<span data-ttu-id="63fed-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63fed-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63fed-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63fed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63fed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fed-137">CommonParameters</span></span>
<span data-ttu-id="63fed-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63fed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fed-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fed-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fed-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63fed-140">INPUTS</span></span>

### <span data-ttu-id="63fed-141">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="63fed-141">PolicyBase</span></span>
<span data-ttu-id="63fed-142">Параметр "Policy" принимает значение типа "PolicyBase" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="63fed-142">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="63fed-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63fed-143">OUTPUTS</span></span>

### <span data-ttu-id="63fed-144">System. Collections. Generic. List "1 [Microsoft. Azure. командлеты. RecoveryServices. Backup. JobBase]</span><span class="sxs-lookup"><span data-stu-id="63fed-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="63fed-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="63fed-145">NOTES</span></span>

## <span data-ttu-id="63fed-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63fed-146">RELATED LINKS</span></span>

[<span data-ttu-id="63fed-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="63fed-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="63fed-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="63fed-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="63fed-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="63fed-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="63fed-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="63fed-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


