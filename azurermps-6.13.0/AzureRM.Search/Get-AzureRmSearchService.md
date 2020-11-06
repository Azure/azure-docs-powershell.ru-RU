---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
ms.openlocfilehash: 57b09ea3267447f16ceadf4d1eae51f997c53a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560639"
---
# <span data-ttu-id="7a716-101">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="7a716-101">Get-AzureRmSearchService</span></span>

## <span data-ttu-id="7a716-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a716-102">SYNOPSIS</span></span>
<span data-ttu-id="7a716-103">Получает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="7a716-103">Gets an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a716-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a716-104">SYNTAX</span></span>

### <span data-ttu-id="7a716-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a716-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSearchService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a716-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a716-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a716-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a716-107">DESCRIPTION</span></span>
<span data-ttu-id="7a716-108">Командлет **Get-AzureRmSearchService** получает указанную службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="7a716-108">The **Get-AzureRmSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="7a716-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a716-109">EXAMPLES</span></span>

### <span data-ttu-id="7a716-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a716-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="7a716-111">Получить службу поиска Azure с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="7a716-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="7a716-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a716-112">PARAMETERS</span></span>

### <span data-ttu-id="7a716-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a716-113">-DefaultProfile</span></span>
<span data-ttu-id="7a716-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a716-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a716-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a716-115">-Name</span></span>
<span data-ttu-id="7a716-116">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7a716-116">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a716-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a716-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a716-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a716-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a716-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a716-119">-ResourceId</span></span>
<span data-ttu-id="7a716-120">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="7a716-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="7a716-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a716-121">CommonParameters</span></span>
<span data-ttu-id="7a716-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a716-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a716-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a716-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a716-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a716-124">INPUTS</span></span>

### <span data-ttu-id="7a716-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7a716-125">System.String</span></span>

## <span data-ttu-id="7a716-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a716-126">OUTPUTS</span></span>

### <span data-ttu-id="7a716-127">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7a716-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="7a716-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a716-128">NOTES</span></span>

## <span data-ttu-id="7a716-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a716-129">RELATED LINKS</span></span>

[<span data-ttu-id="7a716-130">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="7a716-130">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="7a716-131">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="7a716-131">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="7a716-132">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="7a716-132">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
