---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402223"
---
# <span data-ttu-id="bef17-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="bef17-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="bef17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bef17-102">SYNOPSIS</span></span>
<span data-ttu-id="bef17-103">Получает конфигурацию связи ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="bef17-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="bef17-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bef17-104">SYNTAX</span></span>

### <span data-ttu-id="bef17-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bef17-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bef17-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bef17-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bef17-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bef17-107">DESCRIPTION</span></span>
<span data-ttu-id="bef17-108">**Cmdlet Get-AzExpressRoutePortLinkConfig** извлекает конфигурацию связи ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="bef17-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="bef17-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bef17-109">EXAMPLES</span></span>

### <span data-ttu-id="bef17-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bef17-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="bef17-111">Получает конфигурацию Link1 для ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="bef17-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="bef17-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bef17-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="bef17-113">Получает конфигурацию связи с ResourceId $id ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="bef17-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="bef17-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bef17-114">PARAMETERS</span></span>

### <span data-ttu-id="bef17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef17-115">-DefaultProfile</span></span>
<span data-ttu-id="bef17-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bef17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bef17-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bef17-117">-ExpressRoutePort</span></span>
<span data-ttu-id="bef17-118">Ссылка на ресурс ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="bef17-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bef17-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bef17-119">-Name</span></span>
<span data-ttu-id="bef17-120">Имя ссылки.</span><span class="sxs-lookup"><span data-stu-id="bef17-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef17-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bef17-121">-ResourceId</span></span>
<span data-ttu-id="bef17-122">ResourceId ссылки.</span><span class="sxs-lookup"><span data-stu-id="bef17-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef17-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef17-123">CommonParameters</span></span>
<span data-ttu-id="bef17-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef17-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef17-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bef17-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef17-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bef17-126">INPUTS</span></span>

### <span data-ttu-id="bef17-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bef17-127">System.String</span></span>

### <span data-ttu-id="bef17-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bef17-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="bef17-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bef17-129">OUTPUTS</span></span>

### <span data-ttu-id="bef17-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="bef17-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="bef17-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bef17-131">NOTES</span></span>

## <span data-ttu-id="bef17-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bef17-132">RELATED LINKS</span></span>
