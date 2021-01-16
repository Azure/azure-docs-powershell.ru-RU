---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401671"
---
# <span data-ttu-id="438b6-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="438b6-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="438b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="438b6-102">SYNOPSIS</span></span>
<span data-ttu-id="438b6-103">Получить или кластеры списков</span><span class="sxs-lookup"><span data-stu-id="438b6-103">Get or list clusters</span></span>

## <span data-ttu-id="438b6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="438b6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="438b6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="438b6-105">DESCRIPTION</span></span>
<span data-ttu-id="438b6-106">Получить или кластеры списков, кластеры списков в группе ресурсов, если не предоставлена "-ClusterName", кластеры списков под подпиской, если не предоставлены "-ClusterName" и "ResourceGroupName".</span><span class="sxs-lookup"><span data-stu-id="438b6-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="438b6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="438b6-107">EXAMPLES</span></span>

### <span data-ttu-id="438b6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="438b6-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="438b6-109">Получить кластер</span><span class="sxs-lookup"><span data-stu-id="438b6-109">Get cluster</span></span>

## <span data-ttu-id="438b6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="438b6-110">PARAMETERS</span></span>

### <span data-ttu-id="438b6-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="438b6-111">-ClusterName</span></span>
<span data-ttu-id="438b6-112">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="438b6-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="438b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438b6-113">-DefaultProfile</span></span>
<span data-ttu-id="438b6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="438b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="438b6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="438b6-115">-ResourceGroupName</span></span>
<span data-ttu-id="438b6-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="438b6-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="438b6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438b6-117">CommonParameters</span></span>
<span data-ttu-id="438b6-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="438b6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438b6-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="438b6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438b6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="438b6-120">INPUTS</span></span>

### <span data-ttu-id="438b6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="438b6-121">System.String</span></span>

## <span data-ttu-id="438b6-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="438b6-122">OUTPUTS</span></span>

### <span data-ttu-id="438b6-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="438b6-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="438b6-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="438b6-124">NOTES</span></span>

## <span data-ttu-id="438b6-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="438b6-125">RELATED LINKS</span></span>
