---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: a8f256f9a383b3cb7c7aed014474c1ea24706106
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902470"
---
# <span data-ttu-id="e45df-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e45df-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="e45df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e45df-102">SYNOPSIS</span></span>
<span data-ttu-id="e45df-103">Возвращают доступные типы частных конечных точек в расположении</span><span class="sxs-lookup"><span data-stu-id="e45df-103">Return available private end point types in the location</span></span>

## <span data-ttu-id="e45df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e45df-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e45df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e45df-105">DESCRIPTION</span></span>
<span data-ttu-id="e45df-106">Командлет **Get-AzAvailablePrivateEndpointType** возвращает все доступные типы частных конечных точек в расположении.</span><span class="sxs-lookup"><span data-stu-id="e45df-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="e45df-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e45df-107">EXAMPLES</span></span>

### <span data-ttu-id="e45df-108">Образом</span><span class="sxs-lookup"><span data-stu-id="e45df-108">Example</span></span>
```
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsot.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsot.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsot.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="e45df-109">В этом примере возвращаются все доступные типы частных конечных точек в расположении.</span><span class="sxs-lookup"><span data-stu-id="e45df-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="e45df-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e45df-110">PARAMETERS</span></span>

### <span data-ttu-id="e45df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45df-111">-DefaultProfile</span></span>
<span data-ttu-id="e45df-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e45df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e45df-113">-Location</span><span class="sxs-lookup"><span data-stu-id="e45df-113">-Location</span></span>
<span data-ttu-id="e45df-114">Расположение.</span><span class="sxs-lookup"><span data-stu-id="e45df-114">The location.</span></span>

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

### <span data-ttu-id="e45df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45df-115">-ResourceGroupName</span></span>
<span data-ttu-id="e45df-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e45df-116">The resource group name.</span></span>

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

### <span data-ttu-id="e45df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45df-117">CommonParameters</span></span>
<span data-ttu-id="e45df-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e45df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45df-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e45df-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45df-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e45df-120">INPUTS</span></span>

### <span data-ttu-id="e45df-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e45df-121">System.String</span></span>

## <span data-ttu-id="e45df-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e45df-122">OUTPUTS</span></span>

### <span data-ttu-id="e45df-123">Microsoft. Azure. Commands. Network. Models. PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e45df-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="e45df-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="e45df-124">NOTES</span></span>

## <span data-ttu-id="e45df-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e45df-125">RELATED LINKS</span></span>
