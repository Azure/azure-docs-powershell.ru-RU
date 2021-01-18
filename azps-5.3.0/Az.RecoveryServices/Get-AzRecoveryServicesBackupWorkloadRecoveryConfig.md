---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508085"
---
# <span data-ttu-id="752d5-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="752d5-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="752d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="752d5-102">SYNOPSIS</span></span>
<span data-ttu-id="752d5-103">Эта команда строит конфигурацию восстановления для такого элемента, как SQL DB.</span><span class="sxs-lookup"><span data-stu-id="752d5-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="752d5-104">В объекте конфигурации хранится все сведения, такие как режим восстановления, целевые назначения для восстановления и параметры приложения, например целевые физические пути для SQL.</span><span class="sxs-lookup"><span data-stu-id="752d5-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="752d5-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="752d5-105">SYNTAX</span></span>

### <span data-ttu-id="752d5-106">RpParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="752d5-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="752d5-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="752d5-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="752d5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="752d5-108">DESCRIPTION</span></span>
<span data-ttu-id="752d5-109">Команда возвращает для элементов AzureWorkload config восстановления, который передается командлету восстановления.</span><span class="sxs-lookup"><span data-stu-id="752d5-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="752d5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="752d5-110">EXAMPLES</span></span>

### <span data-ttu-id="752d5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="752d5-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="752d5-112">Первый из них используется для получения объекта точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="752d5-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="752d5-113">Второй cmdlet создает план восстановления исходного расположения.</span><span class="sxs-lookup"><span data-stu-id="752d5-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="752d5-114">Третий cmdlet THe создает план восстановления для альтернативного расположения.</span><span class="sxs-lookup"><span data-stu-id="752d5-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="752d5-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="752d5-115">Example 2</span></span>

<span data-ttu-id="752d5-116">Эта команда строит конфигурацию восстановления для такого элемента, как SQL DB.</span><span class="sxs-lookup"><span data-stu-id="752d5-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="752d5-117">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="752d5-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="752d5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="752d5-118">PARAMETERS</span></span>

### <span data-ttu-id="752d5-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="752d5-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="752d5-120">Указывает, что базовую службу DB нужно восстановить на другом выбранном сервере.</span><span class="sxs-lookup"><span data-stu-id="752d5-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="752d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752d5-121">-DefaultProfile</span></span>
<span data-ttu-id="752d5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="752d5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="752d5-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="752d5-123">-FilePath</span></span>
<span data-ttu-id="752d5-124">Определяет filepath, который используется для восстановления.</span><span class="sxs-lookup"><span data-stu-id="752d5-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="752d5-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="752d5-125">-FromFull</span></span>
<span data-ttu-id="752d5-126">Указывает full RecoveryPoint, к которому будут применяться резервные копии журнала.</span><span class="sxs-lookup"><span data-stu-id="752d5-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="752d5-127">-Item</span><span class="sxs-lookup"><span data-stu-id="752d5-127">-Item</span></span>
<span data-ttu-id="752d5-128">Определяет элемент резервной копии, для которого выполняется восстановление.</span><span class="sxs-lookup"><span data-stu-id="752d5-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="752d5-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="752d5-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="752d5-130">Указывает, что перезаписывается активная базовая кодоваяя информация с данными, присутствующими в точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="752d5-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="752d5-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="752d5-131">-PointInTime</span></span>
<span data-ttu-id="752d5-132">Время окончания диапазона времени, для которого требуется получить точку восстановления</span><span class="sxs-lookup"><span data-stu-id="752d5-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="752d5-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="752d5-133">-RecoveryPoint</span></span>
<span data-ttu-id="752d5-134">Объект точки восстановления, который нужно восстановить</span><span class="sxs-lookup"><span data-stu-id="752d5-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="752d5-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="752d5-135">-RestoreAsFiles</span></span>
<span data-ttu-id="752d5-136">Указывает на восстановление базы данных в качестве файлов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="752d5-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="752d5-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="752d5-137">-TargetContainer</span></span>
<span data-ttu-id="752d5-138">Указывает целевой компьютер, на котором необходимо восстановить файлы DB.</span><span class="sxs-lookup"><span data-stu-id="752d5-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="752d5-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="752d5-139">-TargetItem</span></span>
<span data-ttu-id="752d5-140">Указывает целевой объект, для которого требуется восстановить ДД.</span><span class="sxs-lookup"><span data-stu-id="752d5-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="752d5-141">Для SQL требуется только защищенный тип элемента SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="752d5-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="752d5-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="752d5-142">-VaultId</span></span>
<span data-ttu-id="752d5-143">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="752d5-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="752d5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752d5-144">CommonParameters</span></span>
<span data-ttu-id="752d5-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752d5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752d5-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="752d5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752d5-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="752d5-147">INPUTS</span></span>

### <span data-ttu-id="752d5-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="752d5-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="752d5-149">System.String</span><span class="sxs-lookup"><span data-stu-id="752d5-149">System.String</span></span>

## <span data-ttu-id="752d5-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="752d5-150">OUTPUTS</span></span>

### <span data-ttu-id="752d5-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="752d5-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="752d5-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="752d5-152">NOTES</span></span>

## <span data-ttu-id="752d5-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="752d5-153">RELATED LINKS</span></span>
