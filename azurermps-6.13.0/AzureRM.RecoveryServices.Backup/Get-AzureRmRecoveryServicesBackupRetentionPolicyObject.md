---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83eeeec861452407dae1a9d92e5bc900b98d6512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565802"
---
# <span data-ttu-id="6ebf7-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6ebf7-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="6ebf7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ebf7-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebf7-103">Получает базовый объект политики хранения.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ebf7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ebf7-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ebf7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ebf7-105">DESCRIPTION</span></span>
<span data-ttu-id="6ebf7-106">Командлет **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** получает базовый **AzureRMRecoveryServicesRetentionPolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="6ebf7-107">Этот объект не сохраняется в системе.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="6ebf7-108">Это временный объект, который можно управлять и использовать с помощью командлета New-AzureRmRecoveryServicesBackupProtectionPolicy для создания новой политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="6ebf7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ebf7-109">EXAMPLES</span></span>

### <span data-ttu-id="6ebf7-110">Пример 1: Создание политики защиты резервных копий</span><span class="sxs-lookup"><span data-stu-id="6ebf7-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="6ebf7-111">Первая команда получает объект политики хранения, а затем сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="6ebf7-112">Вторая команда задает продолжительность для объекта политики хранения в 365 дней.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="6ebf7-113">Третья команда получает объект политики расписания, а затем сохраняет его в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="6ebf7-114">Последняя команда создает политику защиты резервного копирования с использованием политики хранения и расписания, созданной с помощью предыдущих команд.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="6ebf7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ebf7-115">PARAMETERS</span></span>

### <span data-ttu-id="6ebf7-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6ebf7-116">-BackupManagementType</span></span>
<span data-ttu-id="6ebf7-117">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="6ebf7-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6ebf7-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6ebf7-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="6ebf7-119">AzureVM</span></span> 
- <span data-ttu-id="6ebf7-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="6ebf7-120">AzureSQLDatabase</span></span>
- <span data-ttu-id="6ebf7-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="6ebf7-121">AzureStorage</span></span>

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

### <span data-ttu-id="6ebf7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebf7-122">-DefaultProfile</span></span>
<span data-ttu-id="6ebf7-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ebf7-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="6ebf7-124">-WorkloadType</span></span>
<span data-ttu-id="6ebf7-125">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-125">Specifies the workload type.</span></span>
<span data-ttu-id="6ebf7-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6ebf7-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6ebf7-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="6ebf7-127">AzureVM</span></span> 
- <span data-ttu-id="6ebf7-128">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="6ebf7-128">AzureSQLDatabase</span></span>
- <span data-ttu-id="6ebf7-129">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="6ebf7-129">AzureFiles</span></span>

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

### <span data-ttu-id="6ebf7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebf7-130">CommonParameters</span></span>
<span data-ttu-id="6ebf7-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ebf7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebf7-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ebf7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebf7-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ebf7-133">INPUTS</span></span>

### <span data-ttu-id="6ebf7-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="6ebf7-134">None</span></span>

## <span data-ttu-id="6ebf7-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ebf7-135">OUTPUTS</span></span>

### <span data-ttu-id="6ebf7-136">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="6ebf7-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="6ebf7-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ebf7-137">NOTES</span></span>

## <span data-ttu-id="6ebf7-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ebf7-138">RELATED LINKS</span></span>

[<span data-ttu-id="6ebf7-139">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="6ebf7-139">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="6ebf7-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ebf7-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


