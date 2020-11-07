---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 67c5ccb24267825313612cc539f243551ad1894e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905450"
---
# <span data-ttu-id="67bc3-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="67bc3-101">New-AzSearchService</span></span>

## <span data-ttu-id="67bc3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="67bc3-103">Создает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="67bc3-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="67bc3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67bc3-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67bc3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67bc3-105">DESCRIPTION</span></span>
<span data-ttu-id="67bc3-106">Командлет **New-AzSearchService** создает службу поиска Azure с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="67bc3-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="67bc3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67bc3-107">EXAMPLES</span></span>

### <span data-ttu-id="67bc3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67bc3-108">Example 1</span></span>
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

<span data-ttu-id="67bc3-109">Команда создает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="67bc3-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="67bc3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67bc3-110">PARAMETERS</span></span>

### <span data-ttu-id="67bc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67bc3-111">-DefaultProfile</span></span>
<span data-ttu-id="67bc3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67bc3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67bc3-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="67bc3-113">-HostingMode</span></span>
<span data-ttu-id="67bc3-114">Режим размещения службы поиска.</span><span class="sxs-lookup"><span data-stu-id="67bc3-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="67bc3-115">-Location</span><span class="sxs-lookup"><span data-stu-id="67bc3-115">-Location</span></span>
<span data-ttu-id="67bc3-116">Расположение службы поиска.</span><span class="sxs-lookup"><span data-stu-id="67bc3-116">Search Service location.</span></span>

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

### <span data-ttu-id="67bc3-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="67bc3-117">-Name</span></span>
<span data-ttu-id="67bc3-118">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="67bc3-118">Search Service name.</span></span>

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

### <span data-ttu-id="67bc3-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="67bc3-119">-PartitionCount</span></span>
<span data-ttu-id="67bc3-120">Количество разделов службы поиска.</span><span class="sxs-lookup"><span data-stu-id="67bc3-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="67bc3-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="67bc3-121">-ReplicaCount</span></span>
<span data-ttu-id="67bc3-122">Счетчик реплики службы поиска.</span><span class="sxs-lookup"><span data-stu-id="67bc3-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="67bc3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67bc3-123">-ResourceGroupName</span></span>
<span data-ttu-id="67bc3-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67bc3-124">Resource Group name.</span></span>

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

### <span data-ttu-id="67bc3-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="67bc3-125">-Sku</span></span>
<span data-ttu-id="67bc3-126">SKU службы поиска.</span><span class="sxs-lookup"><span data-stu-id="67bc3-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="67bc3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67bc3-127">-Confirm</span></span>
<span data-ttu-id="67bc3-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67bc3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67bc3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67bc3-129">-WhatIf</span></span>
<span data-ttu-id="67bc3-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67bc3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67bc3-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67bc3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67bc3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67bc3-132">CommonParameters</span></span>
<span data-ttu-id="67bc3-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67bc3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67bc3-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67bc3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67bc3-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67bc3-135">INPUTS</span></span>

### <span data-ttu-id="67bc3-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="67bc3-136">None</span></span>

## <span data-ttu-id="67bc3-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67bc3-137">OUTPUTS</span></span>

### <span data-ttu-id="67bc3-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="67bc3-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="67bc3-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="67bc3-139">NOTES</span></span>

## <span data-ttu-id="67bc3-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67bc3-140">RELATED LINKS</span></span>

[<span data-ttu-id="67bc3-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="67bc3-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="67bc3-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="67bc3-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="67bc3-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="67bc3-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)