---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f648d347e45b6394776a25735efbb06157cc5611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236905"
---
# <span data-ttu-id="96dd2-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="96dd2-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="96dd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="96dd2-103">Возвращает сервер источника сети CDN.</span><span class="sxs-lookup"><span data-stu-id="96dd2-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="96dd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96dd2-104">SYNTAX</span></span>

### <span data-ttu-id="96dd2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96dd2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96dd2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96dd2-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96dd2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96dd2-107">DESCRIPTION</span></span>
<span data-ttu-id="96dd2-108">Командлет **Get-AzCdnOrigin** получает исходный сервер сети доставки содержимого (CDN) для Azure и данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="96dd2-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="96dd2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96dd2-109">EXAMPLES</span></span>

## <span data-ttu-id="96dd2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96dd2-110">PARAMETERS</span></span>

### <span data-ttu-id="96dd2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="96dd2-111">-CdnEndpoint</span></span>
<span data-ttu-id="96dd2-112">Указывает объект конечной точки сети CDN, к которому относится источник.</span><span class="sxs-lookup"><span data-stu-id="96dd2-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="96dd2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96dd2-113">-DefaultProfile</span></span>
<span data-ttu-id="96dd2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="96dd2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96dd2-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="96dd2-115">-EndpointName</span></span>
<span data-ttu-id="96dd2-116">Указывает имя конечной точки, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="96dd2-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="96dd2-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="96dd2-117">-OriginName</span></span>
<span data-ttu-id="96dd2-118">Указывает имя исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="96dd2-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="96dd2-119">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="96dd2-119">-ProfileName</span></span>
<span data-ttu-id="96dd2-120">Указывает имя профиля, которому принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="96dd2-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="96dd2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96dd2-121">-ResourceGroupName</span></span>
<span data-ttu-id="96dd2-122">Указывает имя группы ресурсов, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="96dd2-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="96dd2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96dd2-123">CommonParameters</span></span>
<span data-ttu-id="96dd2-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96dd2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96dd2-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96dd2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96dd2-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96dd2-126">INPUTS</span></span>

### <span data-ttu-id="96dd2-127">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="96dd2-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="96dd2-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96dd2-128">OUTPUTS</span></span>

### <span data-ttu-id="96dd2-129">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="96dd2-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="96dd2-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="96dd2-130">NOTES</span></span>

## <span data-ttu-id="96dd2-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96dd2-131">RELATED LINKS</span></span>

[<span data-ttu-id="96dd2-132">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="96dd2-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


