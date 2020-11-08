---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6033421b9a78e7cb531d2a33eabba1e97010c4f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074720"
---
# <span data-ttu-id="7e6f7-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="7e6f7-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="7e6f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e6f7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e6f7-103">Эта команда создает конфигурацию восстановления резервной копии элемента, например SQL DB.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="7e6f7-104">Объект Configuration хранит все данные, такие как режим восстановления, целевые назначения для параметров восстановления и конкретных приложений, такие как целевые физические пути для SQL.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="7e6f7-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e6f7-105">SYNTAX</span></span>

### <span data-ttu-id="7e6f7-106">RpParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e6f7-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e6f7-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e6f7-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e6f7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e6f7-108">DESCRIPTION</span></span>
<span data-ttu-id="7e6f7-109">Команда возвращает конфигурацию восстановления для элементов AzureWorkload, которые передаются в командлет Restore.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="7e6f7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e6f7-110">EXAMPLES</span></span>

### <span data-ttu-id="7e6f7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e6f7-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="7e6f7-112">Первый командлет используется для получения объекта точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="7e6f7-113">Второй командлет создает план восстановления для исходного восстановления местоположения.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="7e6f7-114">Третий командлет создает план восстановления для восстановления альтернативного расположения.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="7e6f7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e6f7-115">PARAMETERS</span></span>

### <span data-ttu-id="7e6f7-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="7e6f7-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="7e6f7-117">Указывает, что резервная база данных должна быть переписано на базу данных, которая находится в точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="7e6f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e6f7-118">-DefaultProfile</span></span>
<span data-ttu-id="7e6f7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e6f7-120">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7e6f7-120">-FilePath</span></span>
<span data-ttu-id="7e6f7-121">Задает путь к файлу для восстановления.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-121">Specifies the filepath for restore operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6f7-122">-FromFull</span><span class="sxs-lookup"><span data-stu-id="7e6f7-122">-FromFull</span></span>
<span data-ttu-id="7e6f7-123">Указывает полный RecoveryPoint, к которому будут применены резервные копии журнала.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-123">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6f7-124">-Item</span><span class="sxs-lookup"><span data-stu-id="7e6f7-124">-Item</span></span>
<span data-ttu-id="7e6f7-125">Указывает элемент резервного копирования, для которого выполняется операция восстановления.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-125">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="7e6f7-126">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="7e6f7-126">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="7e6f7-127">Указывает, что резервная база данных должна быть переписано на базу данных, которая находится в точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-127">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="7e6f7-128">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="7e6f7-128">-PointInTime</span></span>
<span data-ttu-id="7e6f7-129">Время окончания временного интервала, для которого требуется извлечь точку восстановления</span><span class="sxs-lookup"><span data-stu-id="7e6f7-129">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="7e6f7-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7e6f7-130">-RecoveryPoint</span></span>
<span data-ttu-id="7e6f7-131">Восстанавливаемый объект точки восстановления</span><span class="sxs-lookup"><span data-stu-id="7e6f7-131">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="7e6f7-132">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="7e6f7-132">-RestoreAsFiles</span></span>
<span data-ttu-id="7e6f7-133">Указывает, что база данных будет восстановлена как файлы на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-133">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="7e6f7-134">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="7e6f7-134">-TargetContainer</span></span>
<span data-ttu-id="7e6f7-135">Указывает конечный компьютер, для которого требуется восстановить файлы базы данных.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-135">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e6f7-136">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="7e6f7-136">-TargetItem</span></span>
<span data-ttu-id="7e6f7-137">Указывает целевой объект, для которого требуется восстановить базу данных.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-137">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="7e6f7-138">Для восстановления SQL он должен быть защищенным типом элемента только SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-138">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="7e6f7-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7e6f7-139">-VaultId</span></span>
<span data-ttu-id="7e6f7-140">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7e6f7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e6f7-141">CommonParameters</span></span>
<span data-ttu-id="7e6f7-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e6f7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e6f7-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e6f7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e6f7-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e6f7-144">INPUTS</span></span>

### <span data-ttu-id="7e6f7-145">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="7e6f7-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="7e6f7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7e6f7-146">System.String</span></span>

## <span data-ttu-id="7e6f7-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e6f7-147">OUTPUTS</span></span>

### <span data-ttu-id="7e6f7-148">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="7e6f7-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="7e6f7-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e6f7-149">NOTES</span></span>

## <span data-ttu-id="7e6f7-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e6f7-150">RELATED LINKS</span></span>
