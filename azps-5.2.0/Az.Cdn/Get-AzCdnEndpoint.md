---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402623"
---
# <span data-ttu-id="88825-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="88825-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="88825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88825-102">SYNOPSIS</span></span>
<span data-ttu-id="88825-103">Возвращает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="88825-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="88825-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88825-104">SYNTAX</span></span>

### <span data-ttu-id="88825-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88825-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88825-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88825-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88825-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88825-107">DESCRIPTION</span></span>
<span data-ttu-id="88825-108">Для **этого будет выбрана** конечная точка сети доставки содержимого (CDN) Azure и связанные с ней данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="88825-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="88825-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88825-109">EXAMPLES</span></span>

## <span data-ttu-id="88825-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88825-110">PARAMETERS</span></span>

### <span data-ttu-id="88825-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="88825-111">-CdnProfile</span></span>
<span data-ttu-id="88825-112">Определяет объект профиля CDN, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="88825-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88825-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88825-113">-DefaultProfile</span></span>
<span data-ttu-id="88825-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="88825-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88825-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="88825-115">-EndpointName</span></span>
<span data-ttu-id="88825-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="88825-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="88825-117">Имя конечной точки не является именем хоста конечной точки.</span><span class="sxs-lookup"><span data-stu-id="88825-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="88825-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="88825-118">-ProfileName</span></span>
<span data-ttu-id="88825-119">Имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="88825-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88825-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88825-120">-ResourceGroupName</span></span>
<span data-ttu-id="88825-121">Имя группы ресурсов, к которой относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="88825-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88825-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88825-122">CommonParameters</span></span>
<span data-ttu-id="88825-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88825-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88825-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88825-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88825-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88825-125">INPUTS</span></span>

### <span data-ttu-id="88825-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="88825-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="88825-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88825-127">OUTPUTS</span></span>

### <span data-ttu-id="88825-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="88825-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="88825-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88825-129">NOTES</span></span>

## <span data-ttu-id="88825-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88825-130">RELATED LINKS</span></span>

[<span data-ttu-id="88825-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="88825-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="88825-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="88825-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="88825-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="88825-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="88825-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="88825-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="88825-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="88825-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


