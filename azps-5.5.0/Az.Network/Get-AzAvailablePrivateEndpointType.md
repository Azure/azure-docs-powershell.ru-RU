---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221308"
---
# <span data-ttu-id="7e0f6-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7e0f6-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="7e0f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0f6-103">Возвращать доступные типы частных конечных точек в расположении.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="7e0f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e0f6-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e0f6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e0f6-105">DESCRIPTION</span></span>
<span data-ttu-id="7e0f6-106">**Cmdlet Get-AzAvailablePrivateEndpointType** возвращает все доступные типы частных конечных точек в расположении.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="7e0f6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e0f6-107">EXAMPLES</span></span>

### <span data-ttu-id="7e0f6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e0f6-108">Example 1</span></span>
```powershell
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="7e0f6-109">В этом примере возвращаются все доступные типы частных конечных точек в расположении.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="7e0f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e0f6-110">PARAMETERS</span></span>

### <span data-ttu-id="7e0f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0f6-111">-DefaultProfile</span></span>
<span data-ttu-id="7e0f6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e0f6-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7e0f6-113">-Location</span></span>
<span data-ttu-id="7e0f6-114">Расположение.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-114">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e0f6-115">-ResourceGroupName</span></span>
<span data-ttu-id="7e0f6-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0f6-117">CommonParameters</span></span>
<span data-ttu-id="7e0f6-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0f6-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e0f6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0f6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e0f6-120">INPUTS</span></span>

### <span data-ttu-id="7e0f6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7e0f6-121">System.String</span></span>

## <span data-ttu-id="7e0f6-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e0f6-122">OUTPUTS</span></span>

### <span data-ttu-id="7e0f6-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7e0f6-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="7e0f6-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e0f6-124">NOTES</span></span>

## <span data-ttu-id="7e0f6-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e0f6-125">RELATED LINKS</span></span>
