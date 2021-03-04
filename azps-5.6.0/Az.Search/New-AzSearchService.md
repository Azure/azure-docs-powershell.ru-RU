---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 61101242b100ca4b477910a0dfa339ef7f9ea81b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958003"
---
# <span data-ttu-id="6d453-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="6d453-101">New-AzSearchService</span></span>

## <span data-ttu-id="6d453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d453-102">SYNOPSIS</span></span>
<span data-ttu-id="6d453-103">Создает службу поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="6d453-103">Creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6d453-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6d453-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d453-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d453-105">DESCRIPTION</span></span>
<span data-ttu-id="6d453-106">С **помощью cmdlet New-AzSearchService** создается служба Azure Cognitive Search с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="6d453-106">The **New-AzSearchService** cmdlet creates an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="6d453-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6d453-107">EXAMPLES</span></span>

### <span data-ttu-id="6d453-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d453-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="6d453-109">Команда создает службу поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="6d453-109">The command creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6d453-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d453-110">PARAMETERS</span></span>

### <span data-ttu-id="6d453-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d453-111">-DefaultProfile</span></span>
<span data-ttu-id="6d453-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d453-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d453-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="6d453-113">-HostingMode</span></span>
<span data-ttu-id="6d453-114">Режим размещения службы интеллектуального поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="6d453-114">Azure Cognitive Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d453-115">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6d453-115">-IdentityType</span></span>
<span data-ttu-id="6d453-116">(Необязательно) Удостоверение службы интеллектуального поиска Azure (отсутствует/назначена система)</span><span class="sxs-lookup"><span data-stu-id="6d453-116">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

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

### <span data-ttu-id="6d453-117">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="6d453-117">-IPRuleList</span></span>
<span data-ttu-id="6d453-118">(Необязательно) Ip-правила службы интеллектуального поиска Azure</span><span class="sxs-lookup"><span data-stu-id="6d453-118">(Optional) Azure Cognitive Search Service IP rules</span></span>

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

### <span data-ttu-id="6d453-119">-Location</span><span class="sxs-lookup"><span data-stu-id="6d453-119">-Location</span></span>
<span data-ttu-id="6d453-120">Расположение службы поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="6d453-120">Azure Cognitive Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d453-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6d453-121">-Name</span></span>
<span data-ttu-id="6d453-122">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="6d453-122">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d453-123">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="6d453-123">-PartitionCount</span></span>
<span data-ttu-id="6d453-124">Количество разделов службы интеллектуального поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="6d453-124">Azure Cognitive Search Service partition count.</span></span>

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

### <span data-ttu-id="6d453-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="6d453-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="6d453-126">(Необязательно) Доступ к общесетной сети службы поиска Azure (включен или отключен)</span><span class="sxs-lookup"><span data-stu-id="6d453-126">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

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

### <span data-ttu-id="6d453-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="6d453-127">-ReplicaCount</span></span>
<span data-ttu-id="6d453-128">Количество репликации службы интеллектуального поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="6d453-128">Azure Cognitive Search Service replica count.</span></span>

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

### <span data-ttu-id="6d453-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d453-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d453-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d453-130">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d453-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="6d453-131">-Sku</span></span>
<span data-ttu-id="6d453-132">SKU службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="6d453-132">Azure Cognitive Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d453-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d453-133">-Confirm</span></span>
<span data-ttu-id="6d453-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6d453-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d453-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d453-135">-WhatIf</span></span>
<span data-ttu-id="6d453-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d453-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d453-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6d453-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d453-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d453-138">CommonParameters</span></span>
<span data-ttu-id="6d453-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d453-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d453-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d453-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d453-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d453-141">INPUTS</span></span>

### <span data-ttu-id="6d453-142">Нет</span><span class="sxs-lookup"><span data-stu-id="6d453-142">None</span></span>

## <span data-ttu-id="6d453-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6d453-143">OUTPUTS</span></span>

### <span data-ttu-id="6d453-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="6d453-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="6d453-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6d453-145">NOTES</span></span>

## <span data-ttu-id="6d453-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d453-146">RELATED LINKS</span></span>

[<span data-ttu-id="6d453-147">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="6d453-147">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="6d453-148">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="6d453-148">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="6d453-149">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="6d453-149">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)