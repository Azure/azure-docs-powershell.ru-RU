---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243331"
---
# <span data-ttu-id="1475e-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="1475e-101">New-AzSearchService</span></span>

## <span data-ttu-id="1475e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1475e-102">SYNOPSIS</span></span>
<span data-ttu-id="1475e-103">Создает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1475e-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="1475e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1475e-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1475e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1475e-105">DESCRIPTION</span></span>
<span data-ttu-id="1475e-106">Командлет **New-AzSearchService** создает службу поиска Azure с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="1475e-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="1475e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1475e-107">EXAMPLES</span></span>

### <span data-ttu-id="1475e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1475e-108">Example 1</span></span>
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

<span data-ttu-id="1475e-109">Команда создает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="1475e-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="1475e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1475e-110">PARAMETERS</span></span>

### <span data-ttu-id="1475e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1475e-111">-DefaultProfile</span></span>
<span data-ttu-id="1475e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1475e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1475e-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="1475e-113">-HostingMode</span></span>
<span data-ttu-id="1475e-114">Режим размещения службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1475e-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="1475e-115">-Location</span><span class="sxs-lookup"><span data-stu-id="1475e-115">-Location</span></span>
<span data-ttu-id="1475e-116">Расположение службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1475e-116">Search Service location.</span></span>

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

### <span data-ttu-id="1475e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1475e-117">-Name</span></span>
<span data-ttu-id="1475e-118">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1475e-118">Search Service name.</span></span>

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

### <span data-ttu-id="1475e-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="1475e-119">-PartitionCount</span></span>
<span data-ttu-id="1475e-120">Количество разделов службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1475e-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="1475e-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="1475e-121">-ReplicaCount</span></span>
<span data-ttu-id="1475e-122">Счетчик реплики службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1475e-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="1475e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1475e-123">-ResourceGroupName</span></span>
<span data-ttu-id="1475e-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1475e-124">Resource Group name.</span></span>

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

### <span data-ttu-id="1475e-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="1475e-125">-Sku</span></span>
<span data-ttu-id="1475e-126">SKU службы поиска.</span><span class="sxs-lookup"><span data-stu-id="1475e-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="1475e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1475e-127">-Confirm</span></span>
<span data-ttu-id="1475e-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1475e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1475e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1475e-129">-WhatIf</span></span>
<span data-ttu-id="1475e-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1475e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1475e-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1475e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1475e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1475e-132">CommonParameters</span></span>
<span data-ttu-id="1475e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1475e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1475e-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1475e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1475e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1475e-135">INPUTS</span></span>

### <span data-ttu-id="1475e-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="1475e-136">None</span></span>

## <span data-ttu-id="1475e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1475e-137">OUTPUTS</span></span>

### <span data-ttu-id="1475e-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="1475e-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="1475e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1475e-139">NOTES</span></span>

## <span data-ttu-id="1475e-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1475e-140">RELATED LINKS</span></span>

[<span data-ttu-id="1475e-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="1475e-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="1475e-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="1475e-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="1475e-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="1475e-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)