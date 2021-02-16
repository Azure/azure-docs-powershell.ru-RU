---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237156"
---
# <span data-ttu-id="941e4-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="941e4-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="941e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="941e4-102">SYNOPSIS</span></span>
<span data-ttu-id="941e4-103">Обновляет громкость файлов Azure NetApp Files (ANF) в соответствии с предоставленными необязательными модификаторами.</span><span class="sxs-lookup"><span data-stu-id="941e4-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="941e4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="941e4-104">SYNTAX</span></span>

### <span data-ttu-id="941e4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="941e4-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="941e4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="941e4-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="941e4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="941e4-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="941e4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="941e4-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="941e4-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="941e4-109">DESCRIPTION</span></span>
<span data-ttu-id="941e4-110">Для обновления громкости ANF обновляется **cmdlet Update-AzNetAppFilesVolume.**</span><span class="sxs-lookup"><span data-stu-id="941e4-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="941e4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="941e4-111">EXAMPLES</span></span>

### <span data-ttu-id="941e4-112">Пример 1. Обновление тома ANF</span><span class="sxs-lookup"><span data-stu-id="941e4-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="941e4-113">Эта команда обновляет том ANF "MyAnfVolume" с новым размером UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="941e4-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="941e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="941e4-114">PARAMETERS</span></span>

### <span data-ttu-id="941e4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="941e4-115">-AccountName</span></span>
<span data-ttu-id="941e4-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="941e4-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-117">-Backup</span><span class="sxs-lookup"><span data-stu-id="941e4-117">-Backup</span></span>
<span data-ttu-id="941e4-118">A hashtable array which represents the backup object</span><span class="sxs-lookup"><span data-stu-id="941e4-118">A hashtable array which represents the backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeBackupProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="941e4-119">-DefaultProfile</span></span>
<span data-ttu-id="941e4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="941e4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="941e4-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="941e4-121">-ExportPolicy</span></span>
<span data-ttu-id="941e4-122">A hashtable array which represents the export policy</span><span class="sxs-lookup"><span data-stu-id="941e4-122">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="941e4-123">-InputObject</span></span>
<span data-ttu-id="941e4-124">Обновляемый объект громкости</span><span class="sxs-lookup"><span data-stu-id="941e4-124">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-125">-Location</span><span class="sxs-lookup"><span data-stu-id="941e4-125">-Location</span></span>
<span data-ttu-id="941e4-126">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="941e4-126">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="941e4-127">-Name</span></span>
<span data-ttu-id="941e4-128">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="941e4-128">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="941e4-129">-PoolName</span></span>
<span data-ttu-id="941e4-130">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="941e4-130">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="941e4-131">-PoolObject</span></span>
<span data-ttu-id="941e4-132">Объект пула, содержащий объем для обновления</span><span class="sxs-lookup"><span data-stu-id="941e4-132">The pool object containing the volume to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="941e4-133">-ResourceGroupName</span></span>
<span data-ttu-id="941e4-134">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="941e4-134">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="941e4-135">-ResourceId</span></span>
<span data-ttu-id="941e4-136">ИД ресурса для тома ANF</span><span class="sxs-lookup"><span data-stu-id="941e4-136">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="941e4-137">-ServiceLevel</span></span>
<span data-ttu-id="941e4-138">Уровень обслуживания для тома ANF</span><span class="sxs-lookup"><span data-stu-id="941e4-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="941e4-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="941e4-139">-Tag</span></span>
<span data-ttu-id="941e4-140">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="941e4-140">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="941e4-141">-ThroughputMibps</span></span>
<span data-ttu-id="941e4-142">Максимальная пропускная способность в MIBPS, которую можно достичь с помощью такой громкости</span><span class="sxs-lookup"><span data-stu-id="941e4-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="941e4-143">-UsageThreshold</span></span>
<span data-ttu-id="941e4-144">Максимальная квота хранилища, допустимая для файловой системы вбавь</span><span class="sxs-lookup"><span data-stu-id="941e4-144">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e4-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="941e4-145">-Confirm</span></span>
<span data-ttu-id="941e4-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="941e4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="941e4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="941e4-147">-WhatIf</span></span>
<span data-ttu-id="941e4-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="941e4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="941e4-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="941e4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="941e4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941e4-150">CommonParameters</span></span>
<span data-ttu-id="941e4-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="941e4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941e4-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="941e4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941e4-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="941e4-153">INPUTS</span></span>

### <span data-ttu-id="941e4-154">System.String</span><span class="sxs-lookup"><span data-stu-id="941e4-154">System.String</span></span>

### <span data-ttu-id="941e4-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="941e4-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="941e4-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="941e4-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="941e4-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="941e4-157">OUTPUTS</span></span>

### <span data-ttu-id="941e4-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="941e4-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="941e4-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="941e4-159">NOTES</span></span>

## <span data-ttu-id="941e4-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="941e4-160">RELATED LINKS</span></span>
