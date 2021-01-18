---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518173"
---
# <span data-ttu-id="b4645-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b4645-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="b4645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4645-102">SYNOPSIS</span></span>
<span data-ttu-id="b4645-103">Создает новый том файлов Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="b4645-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="b4645-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4645-104">SYNTAX</span></span>

### <span data-ttu-id="b4645-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4645-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4645-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4645-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4645-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4645-107">DESCRIPTION</span></span>
<span data-ttu-id="b4645-108">Для создания громкости ANF создается **cmdlet New-AzNetAppFilesVolume.**</span><span class="sxs-lookup"><span data-stu-id="b4645-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="b4645-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4645-109">EXAMPLES</span></span>

### <span data-ttu-id="b4645-110">Пример 1. Создание тома ANF</span><span class="sxs-lookup"><span data-stu-id="b4645-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="b4645-111">Эта команда создает новый том ANF "MyAnfVolume" в пуле "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="b4645-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="b4645-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4645-112">PARAMETERS</span></span>

### <span data-ttu-id="b4645-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4645-113">-AccountName</span></span>
<span data-ttu-id="b4645-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="b4645-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="b4645-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="b4645-115">-Backup</span></span>
<span data-ttu-id="b4645-116">A hashtable array which represents the backup object</span><span class="sxs-lookup"><span data-stu-id="b4645-116">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="b4645-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="b4645-117">-BackupId</span></span>
<span data-ttu-id="b4645-118">ИД резервной копии.</span><span class="sxs-lookup"><span data-stu-id="b4645-118">Backup ID.</span></span> <span data-ttu-id="b4645-119">UUID 4 или идентификатор ресурса, используемый для идентификации резервного копирования</span><span class="sxs-lookup"><span data-stu-id="b4645-119">UUID v4 or resource identifier used to identify the Backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="b4645-120">-CreationToken</span></span>
<span data-ttu-id="b4645-121">Уникальный путь к файлу для объема</span><span class="sxs-lookup"><span data-stu-id="b4645-121">A unique file path for the volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4645-122">-DefaultProfile</span></span>
<span data-ttu-id="b4645-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4645-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4645-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="b4645-124">-ExportPolicy</span></span>
<span data-ttu-id="b4645-125">A hashtable array which represents the export policy</span><span class="sxs-lookup"><span data-stu-id="b4645-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="b4645-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="b4645-126">-KerberosEnabled</span></span>
<span data-ttu-id="b4645-127">Опишите, включена ли громкость Kerberos</span><span class="sxs-lookup"><span data-stu-id="b4645-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="b4645-128">-Location</span><span class="sxs-lookup"><span data-stu-id="b4645-128">-Location</span></span>
<span data-ttu-id="b4645-129">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="b4645-129">The location of the resource</span></span>

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

### <span data-ttu-id="b4645-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b4645-130">-Name</span></span>
<span data-ttu-id="b4645-131">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="b4645-131">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b4645-132">-PoolName</span></span>
<span data-ttu-id="b4645-133">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="b4645-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="b4645-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="b4645-134">-PoolObject</span></span>
<span data-ttu-id="b4645-135">Пул для нового объекта громкости</span><span class="sxs-lookup"><span data-stu-id="b4645-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="b4645-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="b4645-136">-ProtocolType</span></span>
<span data-ttu-id="b4645-137">A hashtable array which represents the export policy</span><span class="sxs-lookup"><span data-stu-id="b4645-137">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="b4645-138">-ReplicationObject</span></span>
<span data-ttu-id="b4645-139">A hashtable array which represents the replication object</span><span class="sxs-lookup"><span data-stu-id="b4645-139">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4645-140">-ResourceGroupName</span></span>
<span data-ttu-id="b4645-141">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="b4645-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b4645-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="b4645-142">-SecurityStyle</span></span>
<span data-ttu-id="b4645-143">Стиль безопасности громкости.</span><span class="sxs-lookup"><span data-stu-id="b4645-143">The security style of volume.</span></span> <span data-ttu-id="b4645-144">Возможные значения: ntfs, 'unix'</span><span class="sxs-lookup"><span data-stu-id="b4645-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="b4645-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="b4645-145">-ServiceLevel</span></span>
<span data-ttu-id="b4645-146">Уровень обслуживания для тома ANF</span><span class="sxs-lookup"><span data-stu-id="b4645-146">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-147">-Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="b4645-147">-Snapshot</span></span>
<span data-ttu-id="b4645-148">A hashtable array which represents the snapshot object</span><span class="sxs-lookup"><span data-stu-id="b4645-148">A hashtable array which represents the snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeSnapshot
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="b4645-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="b4645-150">Если включена (истина), то объем будет содержать доступный только для чтения .snapshot каталог, который предоставляет доступ к снимкам каждого тома (по умолчанию — true).</span><span class="sxs-lookup"><span data-stu-id="b4645-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="b4645-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="b4645-151">-SnapshotId</span></span>
<span data-ttu-id="b4645-152">Создание громкости на сайте из моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b4645-152">Create volume from a snapshot.</span></span> <span data-ttu-id="b4645-153">UUID 4 или идентификатор ресурса, используемый для идентификации моментального снимка</span><span class="sxs-lookup"><span data-stu-id="b4645-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b4645-154">-SubnetId</span></span>
<span data-ttu-id="b4645-155">URI ресурса Azure для делегированной подсети</span><span class="sxs-lookup"><span data-stu-id="b4645-155">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4645-156">-Tag</span></span>
<span data-ttu-id="b4645-157">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="b4645-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="b4645-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="b4645-158">-ThroughputMibps</span></span>
<span data-ttu-id="b4645-159">Максимальная пропускная способность в MIBPS, которую можно достичь с помощью такой громкости</span><span class="sxs-lookup"><span data-stu-id="b4645-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="b4645-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="b4645-160">-UsageThreshold</span></span>
<span data-ttu-id="b4645-161">Максимальная квота хранилища, допустимая для файловой системы вбавь</span><span class="sxs-lookup"><span data-stu-id="b4645-161">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="b4645-162">-VolumeType</span></span>
<span data-ttu-id="b4645-163">Тип тома ANF</span><span class="sxs-lookup"><span data-stu-id="b4645-163">The type of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4645-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4645-164">-Confirm</span></span>
<span data-ttu-id="b4645-165">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b4645-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4645-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4645-166">-WhatIf</span></span>
<span data-ttu-id="b4645-167">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4645-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4645-168">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b4645-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4645-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4645-169">CommonParameters</span></span>
<span data-ttu-id="b4645-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4645-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4645-171">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4645-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4645-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4645-172">INPUTS</span></span>

### <span data-ttu-id="b4645-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b4645-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="b4645-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4645-174">OUTPUTS</span></span>

### <span data-ttu-id="b4645-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b4645-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b4645-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4645-176">NOTES</span></span>

## <span data-ttu-id="b4645-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4645-177">RELATED LINKS</span></span>
