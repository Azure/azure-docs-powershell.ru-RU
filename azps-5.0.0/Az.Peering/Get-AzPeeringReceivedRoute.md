---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247935"
---
# <span data-ttu-id="0a180-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="0a180-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="0a180-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a180-102">SYNOPSIS</span></span>
<span data-ttu-id="0a180-103">Список полученных маршрутов для пиринга.</span><span class="sxs-lookup"><span data-stu-id="0a180-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="0a180-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a180-104">SYNTAX</span></span>

### <span data-ttu-id="0a180-105">ByResourceGroupAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a180-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a180-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a180-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a180-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a180-107">DESCRIPTION</span></span>
<span data-ttu-id="0a180-108">Списки полученных маршрутов от пиринга</span><span class="sxs-lookup"><span data-stu-id="0a180-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="0a180-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a180-109">EXAMPLES</span></span>

### <span data-ttu-id="0a180-110">Список первых 100 полученных маршрутов для пиринга</span><span class="sxs-lookup"><span data-stu-id="0a180-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="0a180-111">Список всех полученных маршрутов для пиринга</span><span class="sxs-lookup"><span data-stu-id="0a180-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="0a180-112">Фильтрация по пути</span><span class="sxs-lookup"><span data-stu-id="0a180-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="0a180-113">Список всех полученных маршрутов для пиринга с фильтром в виде</span><span class="sxs-lookup"><span data-stu-id="0a180-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="0a180-114">Фильтрация по RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="0a180-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="0a180-115">Список всех полученных маршрутов для пиринга с фильтром на RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="0a180-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="0a180-116">Фильтрация по OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="0a180-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="0a180-117">Список всех полученных маршрутов для пиринга с фильтром на OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="0a180-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="0a180-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a180-118">PARAMETERS</span></span>

### <span data-ttu-id="0a180-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="0a180-119">-AsPath</span></span>
<span data-ttu-id="0a180-120">Фильтрация по пути.</span><span class="sxs-lookup"><span data-stu-id="0a180-120">Filter by AS Path.</span></span>
<span data-ttu-id="0a180-121">Пример: "9342 1234 4567"</span><span class="sxs-lookup"><span data-stu-id="0a180-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="0a180-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a180-122">-DefaultProfile</span></span>
<span data-ttu-id="0a180-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a180-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a180-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a180-124">-Name</span></span>
<span data-ttu-id="0a180-125">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="0a180-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a180-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="0a180-126">-OriginAsValidationState</span></span>
<span data-ttu-id="0a180-127">Фильтрация по источнику в качестве состояния проверки.</span><span class="sxs-lookup"><span data-stu-id="0a180-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="0a180-128">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="0a180-128">-Prefix</span></span>
<span data-ttu-id="0a180-129">Фильтрация по префиксу.</span><span class="sxs-lookup"><span data-stu-id="0a180-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="0a180-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a180-130">-ResourceGroupName</span></span>
<span data-ttu-id="0a180-131">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a180-131">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a180-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a180-132">-ResourceId</span></span>
<span data-ttu-id="0a180-133">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a180-133">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a180-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="0a180-134">-RPKIValidationState</span></span>
<span data-ttu-id="0a180-135">Фильтрация по состоянию проверки RPKI.</span><span class="sxs-lookup"><span data-stu-id="0a180-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="0a180-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a180-136">CommonParameters</span></span>
<span data-ttu-id="0a180-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a180-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a180-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a180-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a180-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a180-139">INPUTS</span></span>

### <span data-ttu-id="0a180-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0a180-140">System.String</span></span>

## <span data-ttu-id="0a180-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a180-141">OUTPUTS</span></span>

### <span data-ttu-id="0a180-142">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringReceivedRoute)</span><span class="sxs-lookup"><span data-stu-id="0a180-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="0a180-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a180-143">NOTES</span></span>

## <span data-ttu-id="0a180-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a180-144">RELATED LINKS</span></span>
