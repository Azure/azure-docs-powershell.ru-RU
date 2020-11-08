---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249016"
---
# <span data-ttu-id="5623a-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="5623a-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="5623a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5623a-102">SYNOPSIS</span></span>
<span data-ttu-id="5623a-103">Список подходящих SKU для поставщика ресурсов Kusto.</span><span class="sxs-lookup"><span data-stu-id="5623a-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="5623a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5623a-104">SYNTAX</span></span>

### <span data-ttu-id="5623a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5623a-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5623a-106">List1</span><span class="sxs-lookup"><span data-stu-id="5623a-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5623a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5623a-107">DESCRIPTION</span></span>
<span data-ttu-id="5623a-108">Список подходящих SKU для поставщика ресурсов Kusto.</span><span class="sxs-lookup"><span data-stu-id="5623a-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="5623a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5623a-109">EXAMPLES</span></span>

### <span data-ttu-id="5623a-110">Пример 1: список подходящих конфигураций</span><span class="sxs-lookup"><span data-stu-id="5623a-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="5623a-111">В приведенной выше команде перечислены доступные SKU.</span><span class="sxs-lookup"><span data-stu-id="5623a-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="5623a-112">Пример 2: список подходящих конфигураций для определенного кластера</span><span class="sxs-lookup"><span data-stu-id="5623a-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="5623a-113">В приведенной выше команде перечислены доступные SKU для определенного кластера</span><span class="sxs-lookup"><span data-stu-id="5623a-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="5623a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5623a-114">PARAMETERS</span></span>

### <span data-ttu-id="5623a-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="5623a-115">-ClusterName</span></span>
<span data-ttu-id="5623a-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="5623a-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5623a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5623a-117">-DefaultProfile</span></span>
<span data-ttu-id="5623a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5623a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5623a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5623a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5623a-120">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="5623a-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5623a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5623a-121">-SubscriptionId</span></span>
<span data-ttu-id="5623a-122">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5623a-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5623a-123">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="5623a-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5623a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5623a-124">CommonParameters</span></span>
<span data-ttu-id="5623a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5623a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5623a-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5623a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5623a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5623a-127">INPUTS</span></span>

## <span data-ttu-id="5623a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5623a-128">OUTPUTS</span></span>

### <span data-ttu-id="5623a-129">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="5623a-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="5623a-130">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="5623a-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="5623a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5623a-131">NOTES</span></span>

<span data-ttu-id="5623a-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5623a-132">ALIASES</span></span>

## <span data-ttu-id="5623a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5623a-133">RELATED LINKS</span></span>

