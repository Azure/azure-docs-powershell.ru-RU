---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: cc65ea2b2f050eb356d5be22c935aebb131f5cfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564108"
---
# <span data-ttu-id="95b07-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="95b07-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="95b07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95b07-102">SYNOPSIS</span></span>
<span data-ttu-id="95b07-103">Получает базовый объект политики расписания.</span><span class="sxs-lookup"><span data-stu-id="95b07-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95b07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95b07-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95b07-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95b07-105">DESCRIPTION</span></span>
<span data-ttu-id="95b07-106">Командлет **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** получает базовый **AzureRMRecoveryServicesSchedulePolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="95b07-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="95b07-107">Этот объект не сохраняется в системе.</span><span class="sxs-lookup"><span data-stu-id="95b07-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="95b07-108">Это временный объект, который можно управлять и использовать с помощью командлета New-AzureRmRecoveryServicesBackupProtectionPolicy для создания новой политики защиты резервной копии.</span><span class="sxs-lookup"><span data-stu-id="95b07-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="95b07-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95b07-109">EXAMPLES</span></span>

### <span data-ttu-id="95b07-110">Пример 1: Настройка частоты расписания для еженедельно</span><span class="sxs-lookup"><span data-stu-id="95b07-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="95b07-111">Первая команда получает объект политики хранения, а затем сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="95b07-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="95b07-112">Вторая команда получает объект политики расписания, а затем сохраняет его в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="95b07-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="95b07-113">Третья команда изменяет частоту для политики расписания на Weekly.</span><span class="sxs-lookup"><span data-stu-id="95b07-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="95b07-114">Последняя команда создает политику защиты резервных копий с помощью обновленного расписания.</span><span class="sxs-lookup"><span data-stu-id="95b07-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="95b07-115">Пример 2: Настройка времени резервного копирования</span><span class="sxs-lookup"><span data-stu-id="95b07-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="95b07-116">Первая команда получает объект политики расписания и сохраняет ее в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="95b07-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="95b07-117">Вторая команда удаляет все запланированные значения времени выполнения из $SchPol.</span><span class="sxs-lookup"><span data-stu-id="95b07-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="95b07-118">Третья команда возвращает текущую дату и время, а затем сохраняет ее в переменной $DT.</span><span class="sxs-lookup"><span data-stu-id="95b07-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="95b07-119">Четвертая команда заменяет время выполнения по расписанию на текущее время.</span><span class="sxs-lookup"><span data-stu-id="95b07-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="95b07-120">Вы можете создавать резервные копии для AzureVM только один раз в день, поэтому для сброса времени резервного копирования необходимо заменить первоначальное расписание.</span><span class="sxs-lookup"><span data-stu-id="95b07-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="95b07-121">Последняя команда создает политику защиты резервного копирования с помощью нового расписания.</span><span class="sxs-lookup"><span data-stu-id="95b07-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="95b07-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95b07-122">PARAMETERS</span></span>

### <span data-ttu-id="95b07-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="95b07-123">-BackupManagementType</span></span>
<span data-ttu-id="95b07-124">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="95b07-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="95b07-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="95b07-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95b07-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="95b07-126">AzureVM</span></span> 
- <span data-ttu-id="95b07-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="95b07-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="95b07-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="95b07-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b07-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b07-129">-DefaultProfile</span></span>
<span data-ttu-id="95b07-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95b07-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b07-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="95b07-131">-WorkloadType</span></span>
<span data-ttu-id="95b07-132">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="95b07-132">Specifies the workload type.</span></span>
<span data-ttu-id="95b07-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="95b07-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95b07-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="95b07-134">AzureVM</span></span> 
- <span data-ttu-id="95b07-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="95b07-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="95b07-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="95b07-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b07-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b07-137">CommonParameters</span></span>
<span data-ttu-id="95b07-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95b07-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b07-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b07-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b07-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95b07-140">INPUTS</span></span>

### <span data-ttu-id="95b07-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="95b07-141">None</span></span>

## <span data-ttu-id="95b07-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95b07-142">OUTPUTS</span></span>

### <span data-ttu-id="95b07-143">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="95b07-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="95b07-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="95b07-144">NOTES</span></span>

## <span data-ttu-id="95b07-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95b07-145">RELATED LINKS</span></span>

[<span data-ttu-id="95b07-146">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="95b07-146">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="95b07-147">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="95b07-147">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


