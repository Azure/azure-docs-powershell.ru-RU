---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318965"
---
# <span data-ttu-id="d6b4a-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="d6b4a-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="d6b4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b4a-103">Получение и перечисление кластеров</span><span class="sxs-lookup"><span data-stu-id="d6b4a-103">Get or list clusters</span></span>

## <span data-ttu-id="d6b4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6b4a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6b4a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="d6b4a-106">Получение или перечисление кластеров, список кластеров в группе ресурсов если "-имя_кластера" не предоставлен, список кластеров в разделе "подписку", если не предоставлены "-имя_кластера" и "ResourceGroupName".</span><span class="sxs-lookup"><span data-stu-id="d6b4a-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="d6b4a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6b4a-107">EXAMPLES</span></span>

### <span data-ttu-id="d6b4a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6b4a-108">Example 1</span></span>
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

<span data-ttu-id="d6b4a-109">Получить кластер</span><span class="sxs-lookup"><span data-stu-id="d6b4a-109">Get cluster</span></span>

## <span data-ttu-id="d6b4a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6b4a-110">PARAMETERS</span></span>

### <span data-ttu-id="d6b4a-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="d6b4a-111">-ClusterName</span></span>
<span data-ttu-id="d6b4a-112">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-112">The cluster name.</span></span>

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

### <span data-ttu-id="d6b4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b4a-113">-DefaultProfile</span></span>
<span data-ttu-id="d6b4a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6b4a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b4a-115">-ResourceGroupName</span></span>
<span data-ttu-id="d6b4a-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-116">The resource group name.</span></span>

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

### <span data-ttu-id="d6b4a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b4a-117">CommonParameters</span></span>
<span data-ttu-id="d6b4a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b4a-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6b4a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b4a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6b4a-120">INPUTS</span></span>

### <span data-ttu-id="d6b4a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d6b4a-121">System.String</span></span>

## <span data-ttu-id="d6b4a-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6b4a-122">OUTPUTS</span></span>

### <span data-ttu-id="d6b4a-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="d6b4a-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="d6b4a-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6b4a-124">NOTES</span></span>

## <span data-ttu-id="d6b4a-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6b4a-125">RELATED LINKS</span></span>