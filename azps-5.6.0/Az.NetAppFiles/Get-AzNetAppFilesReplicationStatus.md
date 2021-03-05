---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: 73efd000f6889675c3daf9f99821640a8b6fbb99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968611"
---
# <span data-ttu-id="c4de5-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="c4de5-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="c4de5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4de5-102">SYNOPSIS</span></span>
<span data-ttu-id="c4de5-103">Получить состояние репликации</span><span class="sxs-lookup"><span data-stu-id="c4de5-103">Get the status of the replication</span></span>

## <span data-ttu-id="c4de5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4de5-104">SYNTAX</span></span>

### <span data-ttu-id="c4de5-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4de5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4de5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4de5-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4de5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4de5-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4de5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4de5-108">DESCRIPTION</span></span>
<span data-ttu-id="c4de5-109">Получить состояние репликации</span><span class="sxs-lookup"><span data-stu-id="c4de5-109">Get the status of the replication</span></span>

## <span data-ttu-id="c4de5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4de5-110">EXAMPLES</span></span>

### <span data-ttu-id="c4de5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4de5-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="c4de5-112">Эта команда получает состояние репликации на MyVol</span><span class="sxs-lookup"><span data-stu-id="c4de5-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="c4de5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4de5-113">PARAMETERS</span></span>

### <span data-ttu-id="c4de5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4de5-114">-AccountName</span></span>
<span data-ttu-id="c4de5-115">Имя учетной записи ANF для конечного тома репликации</span><span class="sxs-lookup"><span data-stu-id="c4de5-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="c4de5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4de5-116">-DefaultProfile</span></span>
<span data-ttu-id="c4de5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4de5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4de5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4de5-118">-InputObject</span></span>
<span data-ttu-id="c4de5-119">Объект назначения тома репликации ANF для получения состояния репликации</span><span class="sxs-lookup"><span data-stu-id="c4de5-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="c4de5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c4de5-120">-Name</span></span>
<span data-ttu-id="c4de5-121">Имя конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="c4de5-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4de5-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c4de5-122">-PoolName</span></span>
<span data-ttu-id="c4de5-123">Имя пула ANF для конечного тома репликации</span><span class="sxs-lookup"><span data-stu-id="c4de5-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="c4de5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4de5-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4de5-125">Группа ресурсов для конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="c4de5-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c4de5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4de5-126">-ResourceId</span></span>
<span data-ttu-id="c4de5-127">ИД ресурса конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="c4de5-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c4de5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4de5-128">CommonParameters</span></span>
<span data-ttu-id="c4de5-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4de5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4de5-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4de5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4de5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4de5-131">INPUTS</span></span>

### <span data-ttu-id="c4de5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c4de5-132">System.String</span></span>

### <span data-ttu-id="c4de5-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c4de5-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c4de5-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4de5-134">OUTPUTS</span></span>

### <span data-ttu-id="c4de5-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="c4de5-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="c4de5-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4de5-136">NOTES</span></span>

## <span data-ttu-id="c4de5-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4de5-137">RELATED LINKS</span></span>
