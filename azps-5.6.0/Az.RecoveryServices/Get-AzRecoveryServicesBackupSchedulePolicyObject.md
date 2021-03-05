---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 5bf91aafffb1c6fd650b5fd88f343897afc6c5d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979432"
---
# <span data-ttu-id="4c234-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="4c234-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="4c234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c234-102">SYNOPSIS</span></span>
<span data-ttu-id="4c234-103">Возвращает базовый объект политики расписания.</span><span class="sxs-lookup"><span data-stu-id="4c234-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="4c234-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4c234-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c234-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c234-105">DESCRIPTION</span></span>
<span data-ttu-id="4c234-106">Cmdlet **Get-AzRecoveryServicesBackupSchedulePolicyObject** получает основание **AzureRMRecoveryServicesSchedulePolicyObject.**</span><span class="sxs-lookup"><span data-stu-id="4c234-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="4c234-107">Этот объект не сохраняется в системе.</span><span class="sxs-lookup"><span data-stu-id="4c234-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="4c234-108">Это временный объект, с помощью New-AzRecoveryServicesBackupProtectionPolicy можно создать новую политику защиты резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="4c234-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="4c234-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4c234-109">EXAMPLES</span></span>

### <span data-ttu-id="4c234-110">Пример 1. Запланировать периодичность расписания на еженедельное время</span><span class="sxs-lookup"><span data-stu-id="4c234-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="4c234-111">Первая команда получает объект политики хранения, а затем сохраняет его в переменной $RetPol хранения.</span><span class="sxs-lookup"><span data-stu-id="4c234-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="4c234-112">Вторая команда получает объект политики расписания, а затем сохраняет его в $SchPol переменной.</span><span class="sxs-lookup"><span data-stu-id="4c234-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="4c234-113">Третья команда изменяет частоту для политики расписания на еженедельную.</span><span class="sxs-lookup"><span data-stu-id="4c234-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="4c234-114">Последняя команда создает политику защиты резервного копирования с обновленным расписанием.</span><span class="sxs-lookup"><span data-stu-id="4c234-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="4c234-115">Пример 2. Настройка времени резервного копирования</span><span class="sxs-lookup"><span data-stu-id="4c234-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="4c234-116">Первая команда получает объект политики расписания, а затем сохраняет его в $SchPol переменной.</span><span class="sxs-lookup"><span data-stu-id="4c234-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="4c234-117">Вторая команда удаляет все запланированное время $SchPol.</span><span class="sxs-lookup"><span data-stu-id="4c234-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="4c234-118">Третья команда получает текущую дату и время, а затем сохраняет их в $DT переменной.</span><span class="sxs-lookup"><span data-stu-id="4c234-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="4c234-119">Четвертая команда заменяет запланированное время запуска текущим временем.</span><span class="sxs-lookup"><span data-stu-id="4c234-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="4c234-120">Вы можете архивировать AzureVM только один раз в день, поэтому для сброса времени резервного копирования необходимо заменить исходное расписание.</span><span class="sxs-lookup"><span data-stu-id="4c234-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="4c234-121">Последняя команда создает политику защиты резервного копирования с использованием нового расписания.</span><span class="sxs-lookup"><span data-stu-id="4c234-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="4c234-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c234-122">PARAMETERS</span></span>

### <span data-ttu-id="4c234-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="4c234-123">-BackupManagementType</span></span>
<span data-ttu-id="4c234-124">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c234-124">The class of resources being protected.</span></span> <span data-ttu-id="4c234-125">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="4c234-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c234-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4c234-126">AzureVM</span></span> 
- <span data-ttu-id="4c234-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="4c234-127">AzureStorage</span></span>
- <span data-ttu-id="4c234-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="4c234-128">AzureWorkload</span></span>

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

### <span data-ttu-id="4c234-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c234-129">-DefaultProfile</span></span>
<span data-ttu-id="4c234-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c234-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c234-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="4c234-131">-WorkloadType</span></span>
<span data-ttu-id="4c234-132">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c234-132">Workload type of the resource.</span></span> <span data-ttu-id="4c234-133">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="4c234-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c234-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4c234-134">AzureVM</span></span> 
- <span data-ttu-id="4c234-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="4c234-135">AzureFiles</span></span>
- <span data-ttu-id="4c234-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="4c234-136">MSSQL</span></span>


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

### <span data-ttu-id="4c234-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c234-137">CommonParameters</span></span>
<span data-ttu-id="4c234-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c234-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c234-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c234-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c234-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c234-140">INPUTS</span></span>

### <span data-ttu-id="4c234-141">Нет</span><span class="sxs-lookup"><span data-stu-id="4c234-141">None</span></span>

## <span data-ttu-id="4c234-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c234-142">OUTPUTS</span></span>

### <span data-ttu-id="4c234-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="4c234-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="4c234-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4c234-144">NOTES</span></span>

## <span data-ttu-id="4c234-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c234-145">RELATED LINKS</span></span>

[<span data-ttu-id="4c234-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4c234-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4c234-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4c234-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


