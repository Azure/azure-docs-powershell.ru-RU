---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505950"
---
# <span data-ttu-id="82779-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="82779-101">New-AzSearchService</span></span>

## <span data-ttu-id="82779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82779-102">SYNOPSIS</span></span>
<span data-ttu-id="82779-103">Создает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="82779-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="82779-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82779-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82779-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82779-105">DESCRIPTION</span></span>
<span data-ttu-id="82779-106">С **помощью cmdlet New-AzSearchService** создается служба Azure Search с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="82779-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="82779-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82779-107">EXAMPLES</span></span>

### <span data-ttu-id="82779-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82779-108">Example 1</span></span>
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

<span data-ttu-id="82779-109">Команда создает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="82779-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="82779-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82779-110">PARAMETERS</span></span>

### <span data-ttu-id="82779-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82779-111">-DefaultProfile</span></span>
<span data-ttu-id="82779-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82779-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82779-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="82779-113">-HostingMode</span></span>
<span data-ttu-id="82779-114">Режим размещения службы поиска.</span><span class="sxs-lookup"><span data-stu-id="82779-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="82779-115">-Location</span><span class="sxs-lookup"><span data-stu-id="82779-115">-Location</span></span>
<span data-ttu-id="82779-116">Поиск в службе.</span><span class="sxs-lookup"><span data-stu-id="82779-116">Search Service location.</span></span>

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

### <span data-ttu-id="82779-117">-Name</span><span class="sxs-lookup"><span data-stu-id="82779-117">-Name</span></span>
<span data-ttu-id="82779-118">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="82779-118">Search Service name.</span></span>

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

### <span data-ttu-id="82779-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="82779-119">-PartitionCount</span></span>
<span data-ttu-id="82779-120">Количество разделов службы поиска.</span><span class="sxs-lookup"><span data-stu-id="82779-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="82779-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="82779-121">-ReplicaCount</span></span>
<span data-ttu-id="82779-122">Количество репликации службы поиска.</span><span class="sxs-lookup"><span data-stu-id="82779-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="82779-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82779-123">-ResourceGroupName</span></span>
<span data-ttu-id="82779-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82779-124">Resource Group name.</span></span>

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

### <span data-ttu-id="82779-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="82779-125">-Sku</span></span>
<span data-ttu-id="82779-126">SKU службы поиска.</span><span class="sxs-lookup"><span data-stu-id="82779-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="82779-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82779-127">-Confirm</span></span>
<span data-ttu-id="82779-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82779-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82779-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82779-129">-WhatIf</span></span>
<span data-ttu-id="82779-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82779-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82779-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82779-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82779-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82779-132">CommonParameters</span></span>
<span data-ttu-id="82779-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82779-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82779-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82779-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82779-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82779-135">INPUTS</span></span>

### <span data-ttu-id="82779-136">Нет</span><span class="sxs-lookup"><span data-stu-id="82779-136">None</span></span>

## <span data-ttu-id="82779-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82779-137">OUTPUTS</span></span>

### <span data-ttu-id="82779-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="82779-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="82779-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82779-139">NOTES</span></span>

## <span data-ttu-id="82779-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82779-140">RELATED LINKS</span></span>

[<span data-ttu-id="82779-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="82779-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="82779-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="82779-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="82779-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="82779-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)