---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248185"
---
# <span data-ttu-id="7d0ce-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7d0ce-101">Set-AzSearchService</span></span>

## <span data-ttu-id="7d0ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="7d0ce-103">Обновите службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="7d0ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d0ce-104">SYNTAX</span></span>

### <span data-ttu-id="7d0ce-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d0ce-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d0ce-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d0ce-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d0ce-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d0ce-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d0ce-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d0ce-108">DESCRIPTION</span></span>
<span data-ttu-id="7d0ce-109">Командлет **Set-AzSearchService** изменяет службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="7d0ce-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d0ce-110">EXAMPLES</span></span>

### <span data-ttu-id="7d0ce-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d0ce-111">Example 1</span></span>
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

<span data-ttu-id="7d0ce-112">В этом примере количество секций и число реплик в службе поиска Azure превышено на 2.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="7d0ce-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d0ce-113">PARAMETERS</span></span>

### <span data-ttu-id="7d0ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d0ce-114">-DefaultProfile</span></span>
<span data-ttu-id="7d0ce-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d0ce-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d0ce-116">-InputObject</span></span>
<span data-ttu-id="7d0ce-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="7d0ce-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d0ce-118">-Name</span></span>
<span data-ttu-id="7d0ce-119">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-119">Search Service name.</span></span>

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

### <span data-ttu-id="7d0ce-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="7d0ce-120">-PartitionCount</span></span>
<span data-ttu-id="7d0ce-121">Количество разделов службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="7d0ce-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="7d0ce-122">-ReplicaCount</span></span>
<span data-ttu-id="7d0ce-123">Счетчик реплики службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="7d0ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d0ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d0ce-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-125">Resource Group name.</span></span>

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

### <span data-ttu-id="7d0ce-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d0ce-126">-ResourceId</span></span>
<span data-ttu-id="7d0ce-127">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="7d0ce-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d0ce-128">-Confirm</span></span>
<span data-ttu-id="7d0ce-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d0ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d0ce-130">-WhatIf</span></span>
<span data-ttu-id="7d0ce-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d0ce-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d0ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d0ce-133">CommonParameters</span></span>
<span data-ttu-id="7d0ce-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d0ce-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d0ce-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d0ce-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d0ce-136">INPUTS</span></span>

### <span data-ttu-id="7d0ce-137">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7d0ce-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="7d0ce-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7d0ce-138">System.String</span></span>

## <span data-ttu-id="7d0ce-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d0ce-139">OUTPUTS</span></span>

### <span data-ttu-id="7d0ce-140">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7d0ce-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="7d0ce-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d0ce-141">NOTES</span></span>

## <span data-ttu-id="7d0ce-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d0ce-142">RELATED LINKS</span></span>

[<span data-ttu-id="7d0ce-143">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7d0ce-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="7d0ce-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7d0ce-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="7d0ce-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="7d0ce-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)