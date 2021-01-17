---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398100"
---
# <span data-ttu-id="7fbd4-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7fbd4-101">Set-AzSearchService</span></span>

## <span data-ttu-id="7fbd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbd4-103">Обновив службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="7fbd4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7fbd4-104">SYNTAX</span></span>

### <span data-ttu-id="7fbd4-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fbd4-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fbd4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fbd4-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fbd4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fbd4-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fbd4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fbd4-108">DESCRIPTION</span></span>
<span data-ttu-id="7fbd4-109">**Cmdlet Set-AzSearchService** изменяет службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="7fbd4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7fbd4-110">EXAMPLES</span></span>

### <span data-ttu-id="7fbd4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7fbd4-111">Example 1</span></span>
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

<span data-ttu-id="7fbd4-112">В этом примере количество разделов и количество репликации службы поиска Azure изменяется на 2.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="7fbd4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fbd4-113">PARAMETERS</span></span>

### <span data-ttu-id="7fbd4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbd4-114">-DefaultProfile</span></span>
<span data-ttu-id="7fbd4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fbd4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fbd4-116">-InputObject</span></span>
<span data-ttu-id="7fbd4-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="7fbd4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7fbd4-118">-Name</span></span>
<span data-ttu-id="7fbd4-119">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-119">Search Service name.</span></span>

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

### <span data-ttu-id="7fbd4-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="7fbd4-120">-PartitionCount</span></span>
<span data-ttu-id="7fbd4-121">Количество разделов службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="7fbd4-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="7fbd4-122">-ReplicaCount</span></span>
<span data-ttu-id="7fbd4-123">Количество репликации службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="7fbd4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fbd4-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fbd4-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-125">Resource Group name.</span></span>

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

### <span data-ttu-id="7fbd4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fbd4-126">-ResourceId</span></span>
<span data-ttu-id="7fbd4-127">ИД ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="7fbd4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fbd4-128">-Confirm</span></span>
<span data-ttu-id="7fbd4-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fbd4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fbd4-130">-WhatIf</span></span>
<span data-ttu-id="7fbd4-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fbd4-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fbd4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbd4-133">CommonParameters</span></span>
<span data-ttu-id="7fbd4-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbd4-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fbd4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbd4-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fbd4-136">INPUTS</span></span>

### <span data-ttu-id="7fbd4-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7fbd4-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="7fbd4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7fbd4-138">System.String</span></span>

## <span data-ttu-id="7fbd4-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7fbd4-139">OUTPUTS</span></span>

### <span data-ttu-id="7fbd4-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7fbd4-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="7fbd4-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7fbd4-141">NOTES</span></span>

## <span data-ttu-id="7fbd4-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fbd4-142">RELATED LINKS</span></span>

[<span data-ttu-id="7fbd4-143">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7fbd4-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="7fbd4-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7fbd4-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="7fbd4-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7fbd4-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)