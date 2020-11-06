---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
ms.openlocfilehash: 934ba85d438178ee636d5042f1fa145e63d60291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562659"
---
# <span data-ttu-id="c1850-101">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="c1850-101">New-AzureRmSearchService</span></span>

## <span data-ttu-id="c1850-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1850-102">SYNOPSIS</span></span>
<span data-ttu-id="c1850-103">Создает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="c1850-103">Creates an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1850-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1850-104">SYNTAX</span></span>

```
New-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1850-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1850-105">DESCRIPTION</span></span>
<span data-ttu-id="c1850-106">Командлет **New-AzureRmSearchService** создает службу поиска Azure с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="c1850-106">The **New-AzureRmSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="c1850-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1850-107">EXAMPLES</span></span>

### <span data-ttu-id="c1850-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1850-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


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

<span data-ttu-id="c1850-109">Команда создает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="c1850-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="c1850-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1850-110">PARAMETERS</span></span>

### <span data-ttu-id="c1850-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1850-111">-DefaultProfile</span></span>
<span data-ttu-id="c1850-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1850-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1850-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="c1850-113">-HostingMode</span></span>
<span data-ttu-id="c1850-114">Режим размещения службы поиска.</span><span class="sxs-lookup"><span data-stu-id="c1850-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="c1850-115">-Location</span><span class="sxs-lookup"><span data-stu-id="c1850-115">-Location</span></span>
<span data-ttu-id="c1850-116">Расположение службы поиска.</span><span class="sxs-lookup"><span data-stu-id="c1850-116">Search Service location.</span></span>

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

### <span data-ttu-id="c1850-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1850-117">-Name</span></span>
<span data-ttu-id="c1850-118">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="c1850-118">Search Service name.</span></span>

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

### <span data-ttu-id="c1850-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="c1850-119">-PartitionCount</span></span>
<span data-ttu-id="c1850-120">Количество разделов службы поиска.</span><span class="sxs-lookup"><span data-stu-id="c1850-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="c1850-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="c1850-121">-ReplicaCount</span></span>
<span data-ttu-id="c1850-122">Счетчик реплики службы поиска.</span><span class="sxs-lookup"><span data-stu-id="c1850-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="c1850-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1850-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1850-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1850-124">Resource Group name.</span></span>

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

### <span data-ttu-id="c1850-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="c1850-125">-Sku</span></span>
<span data-ttu-id="c1850-126">SKU службы поиска.</span><span class="sxs-lookup"><span data-stu-id="c1850-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="c1850-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1850-127">-Confirm</span></span>
<span data-ttu-id="c1850-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1850-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1850-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1850-129">-WhatIf</span></span>
<span data-ttu-id="c1850-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1850-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1850-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1850-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1850-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1850-132">CommonParameters</span></span>
<span data-ttu-id="c1850-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1850-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1850-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1850-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1850-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1850-135">INPUTS</span></span>

### <span data-ttu-id="c1850-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="c1850-136">None</span></span>

## <span data-ttu-id="c1850-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1850-137">OUTPUTS</span></span>

### <span data-ttu-id="c1850-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c1850-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="c1850-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1850-139">NOTES</span></span>

## <span data-ttu-id="c1850-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1850-140">RELATED LINKS</span></span>

[<span data-ttu-id="c1850-141">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="c1850-141">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="c1850-142">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="c1850-142">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="c1850-143">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="c1850-143">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
