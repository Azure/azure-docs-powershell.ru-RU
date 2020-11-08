---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: a2345dfe37fd43532739cdfd8000b47fb1e20906
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247610"
---
# <span data-ttu-id="c228d-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="c228d-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="c228d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c228d-102">SYNOPSIS</span></span>
<span data-ttu-id="c228d-103">Получение состояния репликации</span><span class="sxs-lookup"><span data-stu-id="c228d-103">Get the status of the replication</span></span>

## <span data-ttu-id="c228d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c228d-104">SYNTAX</span></span>

### <span data-ttu-id="c228d-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c228d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c228d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c228d-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c228d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c228d-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c228d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c228d-108">DESCRIPTION</span></span>
<span data-ttu-id="c228d-109">Получение состояния репликации</span><span class="sxs-lookup"><span data-stu-id="c228d-109">Get the status of the replication</span></span>

## <span data-ttu-id="c228d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c228d-110">EXAMPLES</span></span>

### <span data-ttu-id="c228d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c228d-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="c228d-112">Эта команда возвращает состояние репликации на MyVol</span><span class="sxs-lookup"><span data-stu-id="c228d-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="c228d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c228d-113">PARAMETERS</span></span>

### <span data-ttu-id="c228d-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="c228d-114">-AccountName</span></span>
<span data-ttu-id="c228d-115">Имя учетной записи ANF целевого тома репликации</span><span class="sxs-lookup"><span data-stu-id="c228d-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="c228d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c228d-116">-DefaultProfile</span></span>
<span data-ttu-id="c228d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c228d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c228d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c228d-118">-InputObject</span></span>
<span data-ttu-id="c228d-119">Объект тома назначения репликации ANF для получения состояния репликации</span><span class="sxs-lookup"><span data-stu-id="c228d-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="c228d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c228d-120">-Name</span></span>
<span data-ttu-id="c228d-121">Имя тома назначения репликации ANF</span><span class="sxs-lookup"><span data-stu-id="c228d-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c228d-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c228d-122">-PoolName</span></span>
<span data-ttu-id="c228d-123">Имя пула ANF целевого тома репликации</span><span class="sxs-lookup"><span data-stu-id="c228d-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="c228d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c228d-124">-ResourceGroupName</span></span>
<span data-ttu-id="c228d-125">Группа ресурсов целевого тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="c228d-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c228d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c228d-126">-ResourceId</span></span>
<span data-ttu-id="c228d-127">Идентификатор ресурса целевого тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="c228d-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="c228d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c228d-128">CommonParameters</span></span>
<span data-ttu-id="c228d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c228d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c228d-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c228d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c228d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c228d-131">INPUTS</span></span>

### <span data-ttu-id="c228d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c228d-132">System.String</span></span>

## <span data-ttu-id="c228d-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c228d-133">OUTPUTS</span></span>

### <span data-ttu-id="c228d-134">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="c228d-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="c228d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c228d-135">NOTES</span></span>

## <span data-ttu-id="c228d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c228d-136">RELATED LINKS</span></span>
