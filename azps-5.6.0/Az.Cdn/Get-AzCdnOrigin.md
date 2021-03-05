---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: 5c2aa677bd2f197cfae262ed54372d5172fe2a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009267"
---
# <span data-ttu-id="076fa-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="076fa-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="076fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="076fa-102">SYNOPSIS</span></span>
<span data-ttu-id="076fa-103">Возвращает сервер источника CDN.</span><span class="sxs-lookup"><span data-stu-id="076fa-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="076fa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="076fa-104">SYNTAX</span></span>

### <span data-ttu-id="076fa-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="076fa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="076fa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="076fa-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="076fa-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="076fa-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="076fa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="076fa-108">DESCRIPTION</span></span>
<span data-ttu-id="076fa-109">Для получения источника источник данных сети доставки содержимого (CDN) Azure и его данных конфигурации можно получить проектныйлет **Get-AzCdnOrigin.**</span><span class="sxs-lookup"><span data-stu-id="076fa-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="076fa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="076fa-110">EXAMPLES</span></span>

## <span data-ttu-id="076fa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="076fa-111">PARAMETERS</span></span>

### <span data-ttu-id="076fa-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="076fa-112">-CdnEndpoint</span></span>
<span data-ttu-id="076fa-113">Определяет объект конечной точки CDN, к которому относится источник.</span><span class="sxs-lookup"><span data-stu-id="076fa-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="076fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="076fa-114">-DefaultProfile</span></span>
<span data-ttu-id="076fa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="076fa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="076fa-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="076fa-116">-EndpointName</span></span>
<span data-ttu-id="076fa-117">Указывает имя конечной точки, к которой принадлежит сервер-источник.</span><span class="sxs-lookup"><span data-stu-id="076fa-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="076fa-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="076fa-118">-OriginName</span></span>
<span data-ttu-id="076fa-119">Указывает имя сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="076fa-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="076fa-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="076fa-120">-ProfileName</span></span>
<span data-ttu-id="076fa-121">Определяет имя профиля, к которому принадлежит сервер-источник.</span><span class="sxs-lookup"><span data-stu-id="076fa-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="076fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="076fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="076fa-123">Имя группы ресурсов, к которой принадлежит сервер-источник.</span><span class="sxs-lookup"><span data-stu-id="076fa-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="076fa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="076fa-124">-ResourceId</span></span>
<span data-ttu-id="076fa-125">ИД ресурса источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="076fa-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076fa-126">CommonParameters</span></span>
<span data-ttu-id="076fa-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="076fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076fa-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="076fa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076fa-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="076fa-129">INPUTS</span></span>

### <span data-ttu-id="076fa-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="076fa-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="076fa-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="076fa-131">OUTPUTS</span></span>

### <span data-ttu-id="076fa-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="076fa-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="076fa-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="076fa-133">NOTES</span></span>

## <span data-ttu-id="076fa-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="076fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="076fa-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="076fa-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


