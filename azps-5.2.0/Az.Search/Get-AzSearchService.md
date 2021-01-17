---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e4751232969c407484b978d495d348dc61810715
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393708"
---
# <span data-ttu-id="c763b-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c763b-101">Get-AzSearchService</span></span>

## <span data-ttu-id="c763b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c763b-102">SYNOPSIS</span></span>
<span data-ttu-id="c763b-103">Получает службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="c763b-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="c763b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c763b-104">SYNTAX</span></span>

### <span data-ttu-id="c763b-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c763b-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c763b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c763b-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c763b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c763b-107">DESCRIPTION</span></span>
<span data-ttu-id="c763b-108">Для получения указанной службы Azure Search возвращается cmdlet **Get-AzSearchService.**</span><span class="sxs-lookup"><span data-stu-id="c763b-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="c763b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c763b-109">EXAMPLES</span></span>

### <span data-ttu-id="c763b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c763b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="c763b-111">Получите службу поиска Azure с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="c763b-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="c763b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c763b-112">PARAMETERS</span></span>

### <span data-ttu-id="c763b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c763b-113">-DefaultProfile</span></span>
<span data-ttu-id="c763b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c763b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c763b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c763b-115">-Name</span></span>
<span data-ttu-id="c763b-116">Название службы поиска.</span><span class="sxs-lookup"><span data-stu-id="c763b-116">Search Service name.</span></span>

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

### <span data-ttu-id="c763b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c763b-117">-ResourceGroupName</span></span>
<span data-ttu-id="c763b-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c763b-118">Resource Group name.</span></span>

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

### <span data-ttu-id="c763b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c763b-119">-ResourceId</span></span>
<span data-ttu-id="c763b-120">ИД ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="c763b-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="c763b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c763b-121">CommonParameters</span></span>
<span data-ttu-id="c763b-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c763b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c763b-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c763b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c763b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c763b-124">INPUTS</span></span>

### <span data-ttu-id="c763b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c763b-125">System.String</span></span>

## <span data-ttu-id="c763b-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c763b-126">OUTPUTS</span></span>

### <span data-ttu-id="c763b-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c763b-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="c763b-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c763b-128">NOTES</span></span>

## <span data-ttu-id="c763b-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c763b-129">RELATED LINKS</span></span>

[<span data-ttu-id="c763b-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c763b-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="c763b-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c763b-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="c763b-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c763b-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)