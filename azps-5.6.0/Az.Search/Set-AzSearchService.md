---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 8fadba097b602bd84c8eb36d75f5b7a331e2280b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972547"
---
# <span data-ttu-id="10888-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="10888-101">Set-AzSearchService</span></span>

## <span data-ttu-id="10888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10888-102">SYNOPSIS</span></span>
<span data-ttu-id="10888-103">Обновив службу поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="10888-103">Update an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="10888-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10888-104">SYNTAX</span></span>

### <span data-ttu-id="10888-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10888-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>]
 [-IPRuleList <PSIpRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10888-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10888-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10888-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10888-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10888-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10888-108">DESCRIPTION</span></span>
<span data-ttu-id="10888-109">**Cmdlet Set-AzSearchService** изменяет службу azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="10888-109">The **Set-AzSearchService** cmdlet modifies an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="10888-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10888-110">EXAMPLES</span></span>

### <span data-ttu-id="10888-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10888-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="10888-112">В этом примере количество разделов и количество реплик в службе azure Cognitive Search изменяется на 2.</span><span class="sxs-lookup"><span data-stu-id="10888-112">The example changes partition count and replica count of the Azure Cognitive Search service to 2.</span></span>

## <span data-ttu-id="10888-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10888-113">PARAMETERS</span></span>

### <span data-ttu-id="10888-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10888-114">-DefaultProfile</span></span>
<span data-ttu-id="10888-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10888-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10888-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="10888-116">-IdentityType</span></span>
<span data-ttu-id="10888-117">(Необязательно) Удостоверение службы интеллектуального поиска Azure (отсутствует/назначена система)</span><span class="sxs-lookup"><span data-stu-id="10888-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSIdentityType]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10888-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10888-118">-InputObject</span></span>
<span data-ttu-id="10888-119">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="10888-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10888-120">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="10888-120">-IPRuleList</span></span>
<span data-ttu-id="10888-121">(Необязательно) Ip-правила службы интеллектуального поиска Azure</span><span class="sxs-lookup"><span data-stu-id="10888-121">(Optional) Azure Cognitive Search Service IP rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10888-122">-Name</span><span class="sxs-lookup"><span data-stu-id="10888-122">-Name</span></span>
<span data-ttu-id="10888-123">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="10888-123">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10888-124">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="10888-124">-PartitionCount</span></span>
<span data-ttu-id="10888-125">Количество разделов службы поиска.</span><span class="sxs-lookup"><span data-stu-id="10888-125">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10888-126">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="10888-126">-PublicNetworkAccess</span></span>
<span data-ttu-id="10888-127">(Необязательно) Доступ к общесетной сети службы поиска Azure (включен или отключен)</span><span class="sxs-lookup"><span data-stu-id="10888-127">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSPublicNetworkAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10888-128">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="10888-128">-ReplicaCount</span></span>
<span data-ttu-id="10888-129">Количество репликации службы поиска.</span><span class="sxs-lookup"><span data-stu-id="10888-129">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10888-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10888-130">-ResourceGroupName</span></span>
<span data-ttu-id="10888-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10888-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10888-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10888-132">-ResourceId</span></span>
<span data-ttu-id="10888-133">ИД ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="10888-133">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10888-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10888-134">-Confirm</span></span>
<span data-ttu-id="10888-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="10888-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10888-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10888-136">-WhatIf</span></span>
<span data-ttu-id="10888-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10888-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10888-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="10888-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10888-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10888-139">CommonParameters</span></span>
<span data-ttu-id="10888-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10888-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10888-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10888-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10888-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10888-142">INPUTS</span></span>

### <span data-ttu-id="10888-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="10888-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="10888-144">System.String</span><span class="sxs-lookup"><span data-stu-id="10888-144">System.String</span></span>

## <span data-ttu-id="10888-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10888-145">OUTPUTS</span></span>

### <span data-ttu-id="10888-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="10888-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="10888-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10888-147">NOTES</span></span>

## <span data-ttu-id="10888-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10888-148">RELATED LINKS</span></span>

[<span data-ttu-id="10888-149">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="10888-149">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="10888-150">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="10888-150">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="10888-151">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="10888-151">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)