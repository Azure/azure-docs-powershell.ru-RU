---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507714"
---
# <span data-ttu-id="1592f-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1592f-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="1592f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1592f-102">SYNOPSIS</span></span>
<span data-ttu-id="1592f-103">Получает базовый объект политики хранения.</span><span class="sxs-lookup"><span data-stu-id="1592f-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="1592f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1592f-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1592f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1592f-105">DESCRIPTION</span></span>
<span data-ttu-id="1592f-106">Проектлет **Get-AzRecoveryServicesBackupRetentionPolicyObject** получает основание **AzureRMRecoveryServicesRetentionPolicyObject.**</span><span class="sxs-lookup"><span data-stu-id="1592f-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="1592f-107">Этот объект не сохраняется в системе.</span><span class="sxs-lookup"><span data-stu-id="1592f-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="1592f-108">Это временный объект, с помощью New-AzRecoveryServicesBackupProtectionPolicy можно создавать новую политику резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="1592f-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="1592f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1592f-109">EXAMPLES</span></span>

### <span data-ttu-id="1592f-110">Пример 1. Создание политики защиты резервного копирования</span><span class="sxs-lookup"><span data-stu-id="1592f-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="1592f-111">Первая команда получает объект политики хранения, а затем сохраняет его в переменной $RetPol хранения.</span><span class="sxs-lookup"><span data-stu-id="1592f-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="1592f-112">Вторая команда задает длительность объекта политики хранения 365 дней.</span><span class="sxs-lookup"><span data-stu-id="1592f-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="1592f-113">Третья команда получает объект политики расписания и сохраняет его в переменной $SchPol календаря.</span><span class="sxs-lookup"><span data-stu-id="1592f-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="1592f-114">Последняя команда создает политику защиты резервной копии с помощью политики хранения и расписания, созданной с помощью предыдущих команд.</span><span class="sxs-lookup"><span data-stu-id="1592f-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="1592f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1592f-115">PARAMETERS</span></span>

### <span data-ttu-id="1592f-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1592f-116">-BackupManagementType</span></span>
<span data-ttu-id="1592f-117">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1592f-117">The class of resources being protected.</span></span> <span data-ttu-id="1592f-118">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="1592f-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1592f-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1592f-119">AzureVM</span></span> 
- <span data-ttu-id="1592f-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="1592f-120">AzureWorkload</span></span>
- <span data-ttu-id="1592f-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="1592f-121">AzureStorage</span></span>

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

### <span data-ttu-id="1592f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1592f-122">-DefaultProfile</span></span>
<span data-ttu-id="1592f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1592f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1592f-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1592f-124">-WorkloadType</span></span>
<span data-ttu-id="1592f-125">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="1592f-125">Workload type of the resource.</span></span> <span data-ttu-id="1592f-126">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="1592f-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1592f-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1592f-127">AzureVM</span></span> 
- <span data-ttu-id="1592f-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="1592f-128">AzureFiles</span></span>
- <span data-ttu-id="1592f-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="1592f-129">MSSQL</span></span>

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

### <span data-ttu-id="1592f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1592f-130">CommonParameters</span></span>
<span data-ttu-id="1592f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1592f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1592f-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1592f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1592f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1592f-133">INPUTS</span></span>

### <span data-ttu-id="1592f-134">Нет</span><span class="sxs-lookup"><span data-stu-id="1592f-134">None</span></span>

## <span data-ttu-id="1592f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1592f-135">OUTPUTS</span></span>

### <span data-ttu-id="1592f-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="1592f-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="1592f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1592f-137">NOTES</span></span>

## <span data-ttu-id="1592f-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1592f-138">RELATED LINKS</span></span>

[<span data-ttu-id="1592f-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="1592f-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="1592f-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1592f-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


