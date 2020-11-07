---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6b0f2e2c5b2e9579a92b2cee7387a19fda498fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729683"
---
# <span data-ttu-id="4c53c-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="4c53c-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="4c53c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c53c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c53c-103">Эта команда создает конфигурацию восстановления резервной копии элемента, например SQL DB.</span><span class="sxs-lookup"><span data-stu-id="4c53c-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="4c53c-104">Объект Configuration хранит все данные, такие как режим восстановления, целевые назначения для параметров восстановления и конкретных приложений, такие как целевые физические пути для SQL.</span><span class="sxs-lookup"><span data-stu-id="4c53c-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="4c53c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c53c-105">SYNTAX</span></span>

### <span data-ttu-id="4c53c-106">RpParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4c53c-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c53c-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c53c-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c53c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c53c-108">DESCRIPTION</span></span>
<span data-ttu-id="4c53c-109">Команда возвращает конфигурацию восстановления для элементов AzureWorkload, которые передаются в командлет Restore.</span><span class="sxs-lookup"><span data-stu-id="4c53c-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="4c53c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c53c-110">EXAMPLES</span></span>

### <span data-ttu-id="4c53c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4c53c-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="4c53c-112">Первый командлет используется для получения объекта точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="4c53c-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="4c53c-113">Второй командлет создает план восстановления для исходного восстановления местоположения.</span><span class="sxs-lookup"><span data-stu-id="4c53c-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="4c53c-114">Третий командлет crreats план восстановления для восстановления альтернативного расположения.</span><span class="sxs-lookup"><span data-stu-id="4c53c-114">THe third cmdlet crreats a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="4c53c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c53c-115">PARAMETERS</span></span>

### <span data-ttu-id="4c53c-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="4c53c-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="4c53c-117">Указывает, что резервная база данных должна быть переписано на базу данных, которая находится в точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="4c53c-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c53c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c53c-118">-DefaultProfile</span></span>
<span data-ttu-id="4c53c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c53c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c53c-120">-Item</span><span class="sxs-lookup"><span data-stu-id="4c53c-120">-Item</span></span>
<span data-ttu-id="4c53c-121">Указывает элемент резервного копирования, для которого выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="4c53c-121">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c53c-122">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="4c53c-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="4c53c-123">Указывает, что резервная база данных должна быть переписано на базу данных, которая находится в точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="4c53c-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c53c-124">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="4c53c-124">-PointInTime</span></span>
<span data-ttu-id="4c53c-125">Время окончания временного интервала, для которого требуется извлечь точку восстановления</span><span class="sxs-lookup"><span data-stu-id="4c53c-125">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c53c-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4c53c-126">-RecoveryPoint</span></span>
<span data-ttu-id="4c53c-127">Восстанавливаемый объект точки восстановления</span><span class="sxs-lookup"><span data-stu-id="4c53c-127">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c53c-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="4c53c-128">-TargetItem</span></span>
<span data-ttu-id="4c53c-129">Указывает целевой объект, для которого требуется восстановить базу данных.</span><span class="sxs-lookup"><span data-stu-id="4c53c-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="4c53c-130">Для восстановления SQL он должен быть защищенным типом элемента только SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="4c53c-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c53c-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4c53c-131">-VaultId</span></span>
<span data-ttu-id="4c53c-132">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4c53c-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4c53c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c53c-133">-Confirm</span></span>
<span data-ttu-id="4c53c-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c53c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c53c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c53c-135">-WhatIf</span></span>
<span data-ttu-id="4c53c-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c53c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c53c-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c53c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c53c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c53c-138">CommonParameters</span></span>
<span data-ttu-id="4c53c-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c53c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c53c-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c53c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c53c-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c53c-141">INPUTS</span></span>

### <span data-ttu-id="4c53c-142">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="4c53c-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="4c53c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4c53c-143">System.String</span></span>

## <span data-ttu-id="4c53c-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c53c-144">OUTPUTS</span></span>

### <span data-ttu-id="4c53c-145">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="4c53c-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="4c53c-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c53c-146">NOTES</span></span>

## <span data-ttu-id="4c53c-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c53c-147">RELATED LINKS</span></span>