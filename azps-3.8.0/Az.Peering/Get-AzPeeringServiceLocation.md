---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074487"
---
# <span data-ttu-id="c7e58-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="c7e58-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="c7e58-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7e58-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e58-103">Получает список местоположений служб пиринга, предложенных корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c7e58-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="c7e58-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7e58-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7e58-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7e58-105">DESCRIPTION</span></span>
<span data-ttu-id="c7e58-106">Перечислите расположения для пиринга.</span><span class="sxs-lookup"><span data-stu-id="c7e58-106">List peering locations.</span></span>

## <span data-ttu-id="c7e58-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7e58-107">EXAMPLES</span></span>

### <span data-ttu-id="c7e58-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7e58-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="c7e58-109">Получение местоположений пиринга для Вашингтоне.</span><span class="sxs-lookup"><span data-stu-id="c7e58-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="c7e58-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c7e58-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="c7e58-111">Получение местоположений пиринга для Вашингтоне.</span><span class="sxs-lookup"><span data-stu-id="c7e58-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="c7e58-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7e58-112">PARAMETERS</span></span>

### <span data-ttu-id="c7e58-113">-Country</span><span class="sxs-lookup"><span data-stu-id="c7e58-113">-Country</span></span>
<span data-ttu-id="c7e58-114">Фильтр по странам</span><span class="sxs-lookup"><span data-stu-id="c7e58-114">The country filter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7e58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e58-115">-DefaultProfile</span></span>
<span data-ttu-id="c7e58-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7e58-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e58-117">CommonParameters</span></span>
<span data-ttu-id="c7e58-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7e58-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e58-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7e58-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e58-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7e58-120">INPUTS</span></span>

### <span data-ttu-id="c7e58-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="c7e58-121">None</span></span>

## <span data-ttu-id="c7e58-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7e58-122">OUTPUTS</span></span>

### <span data-ttu-id="c7e58-123">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringServiceLocation)</span><span class="sxs-lookup"><span data-stu-id="c7e58-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="c7e58-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7e58-124">NOTES</span></span>

## <span data-ttu-id="c7e58-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7e58-125">RELATED LINKS</span></span>
