---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: d16b5d916f3a807de818c58de94f7f0841e04d17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956979"
---
# <span data-ttu-id="8cd49-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="8cd49-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="8cd49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cd49-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd49-103">Возвращает расположения, в которых доступны ресурсы ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8cd49-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="8cd49-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8cd49-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cd49-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cd49-105">DESCRIPTION</span></span>
<span data-ttu-id="8cd49-106">Для извлечения ресурсов **ExpressRoutePortsLocation используется cmdlet Get-AzExpressRoutePortsLocation.**</span><span class="sxs-lookup"><span data-stu-id="8cd49-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="8cd49-107">Если в качестве входного данных задано определенное расположение, он отображает подробные сведения о конкретном расположении, то есть список доступных пропускной способности в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="8cd49-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="8cd49-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8cd49-108">EXAMPLES</span></span>

### <span data-ttu-id="8cd49-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8cd49-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="8cd49-110">Здесь перечислены расположения, в которых доступны ресурсы ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8cd49-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="8cd49-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8cd49-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="8cd49-112">Список пропускной способности ExpressRoutePort, доступных в $loc.</span><span class="sxs-lookup"><span data-stu-id="8cd49-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="8cd49-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cd49-113">PARAMETERS</span></span>

### <span data-ttu-id="8cd49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd49-114">-DefaultProfile</span></span>
<span data-ttu-id="8cd49-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8cd49-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cd49-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="8cd49-116">-LocationName</span></span>
<span data-ttu-id="8cd49-117">Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="8cd49-117">The name of the location.</span></span>

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

### <span data-ttu-id="8cd49-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd49-118">CommonParameters</span></span>
<span data-ttu-id="8cd49-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cd49-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd49-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8cd49-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd49-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8cd49-121">INPUTS</span></span>

### <span data-ttu-id="8cd49-122">System.String</span><span class="sxs-lookup"><span data-stu-id="8cd49-122">System.String</span></span>

## <span data-ttu-id="8cd49-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8cd49-123">OUTPUTS</span></span>

### <span data-ttu-id="8cd49-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="8cd49-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="8cd49-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8cd49-125">NOTES</span></span>

## <span data-ttu-id="8cd49-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cd49-126">RELATED LINKS</span></span>
