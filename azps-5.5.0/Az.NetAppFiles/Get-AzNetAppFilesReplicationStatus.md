---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: e59ce4f5e3b0f1b07744e0754cf0e1cae3de7da6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226145"
---
# <span data-ttu-id="7d70c-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="7d70c-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="7d70c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d70c-102">SYNOPSIS</span></span>
<span data-ttu-id="7d70c-103">Получить состояние репликации</span><span class="sxs-lookup"><span data-stu-id="7d70c-103">Get the status of the replication</span></span>

## <span data-ttu-id="7d70c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d70c-104">SYNTAX</span></span>

### <span data-ttu-id="7d70c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d70c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d70c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d70c-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d70c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d70c-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d70c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d70c-108">DESCRIPTION</span></span>
<span data-ttu-id="7d70c-109">Получить состояние репликации</span><span class="sxs-lookup"><span data-stu-id="7d70c-109">Get the status of the replication</span></span>

## <span data-ttu-id="7d70c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d70c-110">EXAMPLES</span></span>

### <span data-ttu-id="7d70c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d70c-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="7d70c-112">Эта команда получает состояние репликации на MyVol</span><span class="sxs-lookup"><span data-stu-id="7d70c-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="7d70c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d70c-113">PARAMETERS</span></span>

### <span data-ttu-id="7d70c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7d70c-114">-AccountName</span></span>
<span data-ttu-id="7d70c-115">Имя учетной записи ANF для конечного тома репликации</span><span class="sxs-lookup"><span data-stu-id="7d70c-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="7d70c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d70c-116">-DefaultProfile</span></span>
<span data-ttu-id="7d70c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d70c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d70c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d70c-118">-InputObject</span></span>
<span data-ttu-id="7d70c-119">Объект назначения тома репликации ANF для получения состояния репликации</span><span class="sxs-lookup"><span data-stu-id="7d70c-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="7d70c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7d70c-120">-Name</span></span>
<span data-ttu-id="7d70c-121">Имя конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="7d70c-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="7d70c-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7d70c-122">-PoolName</span></span>
<span data-ttu-id="7d70c-123">Имя пула ANF для конечного тома репликации</span><span class="sxs-lookup"><span data-stu-id="7d70c-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="7d70c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d70c-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d70c-125">Группа ресурсов для конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="7d70c-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="7d70c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d70c-126">-ResourceId</span></span>
<span data-ttu-id="7d70c-127">ИД ресурса конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="7d70c-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="7d70c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d70c-128">CommonParameters</span></span>
<span data-ttu-id="7d70c-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d70c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d70c-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d70c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d70c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d70c-131">INPUTS</span></span>

### <span data-ttu-id="7d70c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7d70c-132">System.String</span></span>

### <span data-ttu-id="7d70c-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7d70c-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7d70c-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d70c-134">OUTPUTS</span></span>

### <span data-ttu-id="7d70c-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="7d70c-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="7d70c-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d70c-136">NOTES</span></span>

## <span data-ttu-id="7d70c-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d70c-137">RELATED LINKS</span></span>
