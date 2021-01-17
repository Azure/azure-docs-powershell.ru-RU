---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422279"
---
# <span data-ttu-id="41514-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="41514-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="41514-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41514-102">SYNOPSIS</span></span>
<span data-ttu-id="41514-103">Возвращает расположения, в которых доступны ресурсы ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="41514-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="41514-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41514-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41514-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41514-105">DESCRIPTION</span></span>
<span data-ttu-id="41514-106">Для извлечения ресурсов **ExpressRoutePortsLocation используется cmdlet Get-AzExpressRoutePortsLocation.**</span><span class="sxs-lookup"><span data-stu-id="41514-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="41514-107">Если в качестве входного данных задано определенное расположение, он отображает подробные сведения о конкретном расположении, то есть список доступных пропускной способности в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="41514-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="41514-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41514-108">EXAMPLES</span></span>

### <span data-ttu-id="41514-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41514-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="41514-110">Здесь перечислены расположения, в которых доступны ресурсы ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="41514-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="41514-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="41514-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="41514-112">Список пропускной способности ExpressRoutePort, доступных в $loc.</span><span class="sxs-lookup"><span data-stu-id="41514-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="41514-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41514-113">PARAMETERS</span></span>

### <span data-ttu-id="41514-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41514-114">-DefaultProfile</span></span>
<span data-ttu-id="41514-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41514-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41514-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="41514-116">-LocationName</span></span>
<span data-ttu-id="41514-117">Название расположения.</span><span class="sxs-lookup"><span data-stu-id="41514-117">The name of the location.</span></span>

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

### <span data-ttu-id="41514-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41514-118">CommonParameters</span></span>
<span data-ttu-id="41514-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41514-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41514-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41514-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41514-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41514-121">INPUTS</span></span>

### <span data-ttu-id="41514-122">System.String</span><span class="sxs-lookup"><span data-stu-id="41514-122">System.String</span></span>

## <span data-ttu-id="41514-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41514-123">OUTPUTS</span></span>

### <span data-ttu-id="41514-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="41514-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="41514-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41514-125">NOTES</span></span>

## <span data-ttu-id="41514-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41514-126">RELATED LINKS</span></span>
