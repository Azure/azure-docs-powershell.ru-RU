---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/set-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
ms.openlocfilehash: c938dd611d9f6d731c07d5aee76cb390838f4679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562652"
---
# <span data-ttu-id="1cb4a-101">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="1cb4a-101">Set-AzureRmSearchService</span></span>

## <span data-ttu-id="1cb4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1cb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb4a-103">Обновите службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-103">Update an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cb4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1cb4a-104">SYNTAX</span></span>

### <span data-ttu-id="1cb4a-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1cb4a-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb4a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb4a-106">InputObjectParameterSet</span></span>
```
Set-AzureRmSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb4a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb4a-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb4a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cb4a-108">DESCRIPTION</span></span>
<span data-ttu-id="1cb4a-109">Командлет **Set-AzureRmSearchService** изменяет службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-109">The **Set-AzureRmSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="1cb4a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1cb4a-110">EXAMPLES</span></span>

### <span data-ttu-id="1cb4a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1cb4a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


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

<span data-ttu-id="1cb4a-112">В этом примере количество секций и число реплик в службе поиска Azure превышено на 2.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="1cb4a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1cb4a-113">PARAMETERS</span></span>

### <span data-ttu-id="1cb4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb4a-114">-DefaultProfile</span></span>
<span data-ttu-id="1cb4a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb4a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cb4a-116">-InputObject</span></span>
<span data-ttu-id="1cb4a-117">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="1cb4a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1cb4a-118">-Name</span></span>
<span data-ttu-id="1cb4a-119">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-119">Search Service name.</span></span>

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

### <span data-ttu-id="1cb4a-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="1cb4a-120">-PartitionCount</span></span>
<span data-ttu-id="1cb4a-121">Количество разделов службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="1cb4a-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="1cb4a-122">-ReplicaCount</span></span>
<span data-ttu-id="1cb4a-123">Счетчик реплики службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="1cb4a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb4a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1cb4a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-125">Resource Group name.</span></span>

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

### <span data-ttu-id="1cb4a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cb4a-126">-ResourceId</span></span>
<span data-ttu-id="1cb4a-127">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="1cb4a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb4a-128">-Confirm</span></span>
<span data-ttu-id="1cb4a-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb4a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb4a-130">-WhatIf</span></span>
<span data-ttu-id="1cb4a-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cb4a-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb4a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb4a-133">CommonParameters</span></span>
<span data-ttu-id="1cb4a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1cb4a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb4a-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cb4a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb4a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1cb4a-136">INPUTS</span></span>

### <span data-ttu-id="1cb4a-137">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="1cb4a-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="1cb4a-138">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1cb4a-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1cb4a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1cb4a-139">System.String</span></span>

## <span data-ttu-id="1cb4a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cb4a-140">OUTPUTS</span></span>

### <span data-ttu-id="1cb4a-141">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="1cb4a-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="1cb4a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1cb4a-142">NOTES</span></span>

## <span data-ttu-id="1cb4a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cb4a-143">RELATED LINKS</span></span>

[<span data-ttu-id="1cb4a-144">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="1cb4a-144">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="1cb4a-145">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="1cb4a-145">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="1cb4a-146">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="1cb4a-146">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
