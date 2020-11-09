---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245707"
---
# <span data-ttu-id="d6be4-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="d6be4-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="d6be4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6be4-102">SYNOPSIS</span></span>
<span data-ttu-id="d6be4-103">Получает базовый объект политики расписания.</span><span class="sxs-lookup"><span data-stu-id="d6be4-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="d6be4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6be4-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6be4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6be4-105">DESCRIPTION</span></span>
<span data-ttu-id="d6be4-106">Командлет **Get-AzRecoveryServicesBackupSchedulePolicyObject** получает базовый **AzureRMRecoveryServicesSchedulePolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="d6be4-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="d6be4-107">Этот объект не сохраняется в системе.</span><span class="sxs-lookup"><span data-stu-id="d6be4-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="d6be4-108">Это временный объект, который можно управлять и использовать с помощью командлета New-AzRecoveryServicesBackupProtectionPolicy для создания новой политики защиты резервной копии.</span><span class="sxs-lookup"><span data-stu-id="d6be4-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="d6be4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6be4-109">EXAMPLES</span></span>

### <span data-ttu-id="d6be4-110">Пример 1: Настройка частоты расписания для еженедельно</span><span class="sxs-lookup"><span data-stu-id="d6be4-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="d6be4-111">Первая команда получает объект политики хранения, а затем сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="d6be4-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="d6be4-112">Вторая команда получает объект политики расписания, а затем сохраняет его в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="d6be4-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="d6be4-113">Третья команда изменяет частоту для политики расписания на Weekly.</span><span class="sxs-lookup"><span data-stu-id="d6be4-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="d6be4-114">Последняя команда создает политику защиты резервных копий с помощью обновленного расписания.</span><span class="sxs-lookup"><span data-stu-id="d6be4-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="d6be4-115">Пример 2: Настройка времени резервного копирования</span><span class="sxs-lookup"><span data-stu-id="d6be4-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="d6be4-116">Первая команда получает объект политики расписания и сохраняет ее в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="d6be4-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="d6be4-117">Вторая команда удаляет все запланированные значения времени выполнения из $SchPol.</span><span class="sxs-lookup"><span data-stu-id="d6be4-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="d6be4-118">Третья команда возвращает текущую дату и время, а затем сохраняет ее в переменной $DT.</span><span class="sxs-lookup"><span data-stu-id="d6be4-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="d6be4-119">Четвертая команда заменяет время выполнения по расписанию на текущее время.</span><span class="sxs-lookup"><span data-stu-id="d6be4-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="d6be4-120">Вы можете создавать резервные копии для AzureVM только один раз в день, поэтому для сброса времени резервного копирования необходимо заменить первоначальное расписание.</span><span class="sxs-lookup"><span data-stu-id="d6be4-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="d6be4-121">Последняя команда создает политику защиты резервного копирования с помощью нового расписания.</span><span class="sxs-lookup"><span data-stu-id="d6be4-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="d6be4-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6be4-122">PARAMETERS</span></span>

### <span data-ttu-id="d6be4-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d6be4-123">-BackupManagementType</span></span>
<span data-ttu-id="d6be4-124">Класс защищаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6be4-124">The class of resources being protected.</span></span> <span data-ttu-id="d6be4-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d6be4-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6be4-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d6be4-126">AzureVM</span></span> 
- <span data-ttu-id="d6be4-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="d6be4-127">AzureStorage</span></span>
- <span data-ttu-id="d6be4-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="d6be4-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6be4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6be4-129">-DefaultProfile</span></span>
<span data-ttu-id="d6be4-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6be4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6be4-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d6be4-131">-WorkloadType</span></span>
<span data-ttu-id="d6be4-132">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="d6be4-132">Workload type of the resource.</span></span> <span data-ttu-id="d6be4-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d6be4-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6be4-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d6be4-134">AzureVM</span></span> 
- <span data-ttu-id="d6be4-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="d6be4-135">AzureFiles</span></span>
- <span data-ttu-id="d6be4-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="d6be4-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6be4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6be4-137">CommonParameters</span></span>
<span data-ttu-id="d6be4-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6be4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6be4-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6be4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6be4-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6be4-140">INPUTS</span></span>

### <span data-ttu-id="d6be4-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="d6be4-141">None</span></span>

## <span data-ttu-id="d6be4-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6be4-142">OUTPUTS</span></span>

### <span data-ttu-id="d6be4-143">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="d6be4-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="d6be4-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6be4-144">NOTES</span></span>

## <span data-ttu-id="d6be4-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6be4-145">RELATED LINKS</span></span>

[<span data-ttu-id="d6be4-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6be4-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d6be4-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6be4-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

