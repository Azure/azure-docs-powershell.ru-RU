---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233940"
---
# <span data-ttu-id="21908-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="21908-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="21908-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21908-102">SYNOPSIS</span></span>
<span data-ttu-id="21908-103">Создание пула заметок в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="21908-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="21908-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="21908-104">SYNTAX</span></span>

### <span data-ttu-id="21908-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21908-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21908-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21908-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21908-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21908-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21908-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21908-108">DESCRIPTION</span></span>
<span data-ttu-id="21908-109">Создание пула заметок в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="21908-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="21908-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="21908-110">EXAMPLES</span></span>

### <span data-ttu-id="21908-111">Получить все пулы узлов в указанном кластере</span><span class="sxs-lookup"><span data-stu-id="21908-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="21908-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21908-112">PARAMETERS</span></span>

### <span data-ttu-id="21908-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="21908-113">-ClusterName</span></span>
<span data-ttu-id="21908-114">Имя ресурса управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="21908-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21908-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="21908-115">-ClusterObject</span></span>
<span data-ttu-id="21908-116">Объект кластера.</span><span class="sxs-lookup"><span data-stu-id="21908-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21908-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21908-117">-DefaultProfile</span></span>
<span data-ttu-id="21908-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21908-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21908-119">-Id</span><span class="sxs-lookup"><span data-stu-id="21908-119">-Id</span></span>
<span data-ttu-id="21908-120">ИД пула узлов в кластере Managed Kubernetes</span><span class="sxs-lookup"><span data-stu-id="21908-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21908-121">-Name</span><span class="sxs-lookup"><span data-stu-id="21908-121">-Name</span></span>
<span data-ttu-id="21908-122">Имя пула узлов.</span><span class="sxs-lookup"><span data-stu-id="21908-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21908-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21908-123">-ResourceGroupName</span></span>
<span data-ttu-id="21908-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="21908-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21908-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21908-125">CommonParameters</span></span>
<span data-ttu-id="21908-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21908-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21908-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21908-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21908-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21908-128">INPUTS</span></span>

### <span data-ttu-id="21908-129">System.String</span><span class="sxs-lookup"><span data-stu-id="21908-129">System.String</span></span>

## <span data-ttu-id="21908-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21908-130">OUTPUTS</span></span>

### <span data-ttu-id="21908-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="21908-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="21908-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="21908-132">NOTES</span></span>

## <span data-ttu-id="21908-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21908-133">RELATED LINKS</span></span>
