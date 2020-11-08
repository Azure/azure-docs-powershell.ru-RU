---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249964"
---
# <span data-ttu-id="b99fd-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b99fd-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="b99fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b99fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b99fd-103">Возвращают доступные типы частных конечных точек в расположении.</span><span class="sxs-lookup"><span data-stu-id="b99fd-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="b99fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b99fd-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b99fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b99fd-105">DESCRIPTION</span></span>
<span data-ttu-id="b99fd-106">Командлет **Get-AzAvailablePrivateEndpointType** возвращает все доступные типы частных конечных точек в расположении.</span><span class="sxs-lookup"><span data-stu-id="b99fd-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="b99fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b99fd-107">EXAMPLES</span></span>

### <span data-ttu-id="b99fd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b99fd-108">Example 1</span></span>
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

<span data-ttu-id="b99fd-109">В этом примере возвращаются все доступные типы частных конечных точек в расположении.</span><span class="sxs-lookup"><span data-stu-id="b99fd-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="b99fd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b99fd-110">PARAMETERS</span></span>

### <span data-ttu-id="b99fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b99fd-111">-DefaultProfile</span></span>
<span data-ttu-id="b99fd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b99fd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b99fd-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b99fd-113">-Location</span></span>
<span data-ttu-id="b99fd-114">Расположение.</span><span class="sxs-lookup"><span data-stu-id="b99fd-114">The location.</span></span>

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

### <span data-ttu-id="b99fd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b99fd-115">-ResourceGroupName</span></span>
<span data-ttu-id="b99fd-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b99fd-116">The resource group name.</span></span>

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

### <span data-ttu-id="b99fd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b99fd-117">CommonParameters</span></span>
<span data-ttu-id="b99fd-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b99fd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b99fd-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b99fd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b99fd-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b99fd-120">INPUTS</span></span>

### <span data-ttu-id="b99fd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b99fd-121">System.String</span></span>

## <span data-ttu-id="b99fd-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b99fd-122">OUTPUTS</span></span>

### <span data-ttu-id="b99fd-123">Microsoft. Azure. Commands. Network. Models. PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b99fd-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="b99fd-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b99fd-124">NOTES</span></span>

## <span data-ttu-id="b99fd-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b99fd-125">RELATED LINKS</span></span>
