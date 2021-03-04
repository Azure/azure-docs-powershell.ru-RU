---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: bb1c63b41d27f92991a3504cdd5c2fd8fe547298
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958051"
---
# <span data-ttu-id="16c60-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="16c60-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="16c60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c60-102">SYNOPSIS</span></span>
<span data-ttu-id="16c60-103">Получает базовый объект политики хранения.</span><span class="sxs-lookup"><span data-stu-id="16c60-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="16c60-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16c60-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16c60-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c60-105">DESCRIPTION</span></span>
<span data-ttu-id="16c60-106">Cmdlet **Get-AzRecoveryServicesBackupRetentionPolicyObject** получает основание **AzureRMRecoveryServicesRetentionPolicyObject.**</span><span class="sxs-lookup"><span data-stu-id="16c60-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="16c60-107">Этот объект не сохраняется в системе.</span><span class="sxs-lookup"><span data-stu-id="16c60-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="16c60-108">Это временный объект, с помощью New-AzRecoveryServicesBackupProtectionPolicy можно создавать новую политику резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="16c60-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="16c60-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16c60-109">EXAMPLES</span></span>

### <span data-ttu-id="16c60-110">Пример 1. Создание политики защиты резервного копирования</span><span class="sxs-lookup"><span data-stu-id="16c60-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="16c60-111">Первая команда получает объект политики хранения, а затем сохраняет его в переменной $RetPol хранения.</span><span class="sxs-lookup"><span data-stu-id="16c60-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="16c60-112">Вторая команда задает длительность объекта политики хранения, которая составляет 365 дней.</span><span class="sxs-lookup"><span data-stu-id="16c60-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="16c60-113">Третья команда получает объект политики расписания и сохраняет его в переменной $SchPol календаря.</span><span class="sxs-lookup"><span data-stu-id="16c60-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="16c60-114">Последняя команда создает политику защиты резервной копии с помощью политики хранения и расписания, созданной с помощью предыдущих команд.</span><span class="sxs-lookup"><span data-stu-id="16c60-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="16c60-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16c60-115">PARAMETERS</span></span>

### <span data-ttu-id="16c60-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="16c60-116">-BackupManagementType</span></span>
<span data-ttu-id="16c60-117">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16c60-117">The class of resources being protected.</span></span> <span data-ttu-id="16c60-118">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="16c60-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16c60-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="16c60-119">AzureVM</span></span> 
- <span data-ttu-id="16c60-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="16c60-120">AzureWorkload</span></span>
- <span data-ttu-id="16c60-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="16c60-121">AzureStorage</span></span>

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

### <span data-ttu-id="16c60-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c60-122">-DefaultProfile</span></span>
<span data-ttu-id="16c60-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16c60-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16c60-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="16c60-124">-WorkloadType</span></span>
<span data-ttu-id="16c60-125">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="16c60-125">Workload type of the resource.</span></span> <span data-ttu-id="16c60-126">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="16c60-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16c60-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="16c60-127">AzureVM</span></span> 
- <span data-ttu-id="16c60-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="16c60-128">AzureFiles</span></span>
- <span data-ttu-id="16c60-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="16c60-129">MSSQL</span></span>

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

### <span data-ttu-id="16c60-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c60-130">CommonParameters</span></span>
<span data-ttu-id="16c60-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c60-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c60-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16c60-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c60-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16c60-133">INPUTS</span></span>

### <span data-ttu-id="16c60-134">Нет</span><span class="sxs-lookup"><span data-stu-id="16c60-134">None</span></span>

## <span data-ttu-id="16c60-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16c60-135">OUTPUTS</span></span>

### <span data-ttu-id="16c60-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="16c60-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="16c60-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16c60-137">NOTES</span></span>

## <span data-ttu-id="16c60-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16c60-138">RELATED LINKS</span></span>

[<span data-ttu-id="16c60-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="16c60-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="16c60-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="16c60-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


