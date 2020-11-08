---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247117"
---
# <span data-ttu-id="039c1-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="039c1-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="039c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="039c1-102">SYNOPSIS</span></span>
<span data-ttu-id="039c1-103">Создание пула заметок в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="039c1-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="039c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="039c1-104">SYNTAX</span></span>

### <span data-ttu-id="039c1-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="039c1-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="039c1-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="039c1-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="039c1-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="039c1-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="039c1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="039c1-108">DESCRIPTION</span></span>
<span data-ttu-id="039c1-109">Создание пула заметок в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="039c1-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="039c1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="039c1-110">EXAMPLES</span></span>

### <span data-ttu-id="039c1-111">Получение всех пулов узлов в указанном кластере</span><span class="sxs-lookup"><span data-stu-id="039c1-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="039c1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="039c1-112">PARAMETERS</span></span>

### <span data-ttu-id="039c1-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="039c1-113">-ClusterName</span></span>
<span data-ttu-id="039c1-114">Имя ресурса управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="039c1-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="039c1-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="039c1-115">-ClusterObject</span></span>
<span data-ttu-id="039c1-116">Объект кластера.</span><span class="sxs-lookup"><span data-stu-id="039c1-116">The cluster object.</span></span>

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

### <span data-ttu-id="039c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039c1-117">-DefaultProfile</span></span>
<span data-ttu-id="039c1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="039c1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="039c1-119">-ID</span><span class="sxs-lookup"><span data-stu-id="039c1-119">-Id</span></span>
<span data-ttu-id="039c1-120">Идентификатор пула узлов в управляемом кластере Kubernetes</span><span class="sxs-lookup"><span data-stu-id="039c1-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="039c1-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="039c1-121">-Name</span></span>
<span data-ttu-id="039c1-122">Имя пула узлов.</span><span class="sxs-lookup"><span data-stu-id="039c1-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="039c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="039c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="039c1-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="039c1-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="039c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039c1-125">CommonParameters</span></span>
<span data-ttu-id="039c1-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="039c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039c1-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="039c1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039c1-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="039c1-128">INPUTS</span></span>

### <span data-ttu-id="039c1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="039c1-129">System.String</span></span>

## <span data-ttu-id="039c1-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="039c1-130">OUTPUTS</span></span>

### <span data-ttu-id="039c1-131">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="039c1-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="039c1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="039c1-132">NOTES</span></span>

## <span data-ttu-id="039c1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="039c1-133">RELATED LINKS</span></span>
