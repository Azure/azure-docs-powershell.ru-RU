---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249537"
---
# <span data-ttu-id="4340f-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="4340f-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="4340f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4340f-102">SYNOPSIS</span></span>
<span data-ttu-id="4340f-103">Возвращает сервер источника сети CDN.</span><span class="sxs-lookup"><span data-stu-id="4340f-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="4340f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4340f-104">SYNTAX</span></span>

### <span data-ttu-id="4340f-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4340f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4340f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4340f-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4340f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4340f-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4340f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4340f-108">DESCRIPTION</span></span>
<span data-ttu-id="4340f-109">Командлет **Get-AzCdnOrigin** получает исходный сервер сети доставки содержимого (CDN) для Azure и данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4340f-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="4340f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4340f-110">EXAMPLES</span></span>

## <span data-ttu-id="4340f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4340f-111">PARAMETERS</span></span>

### <span data-ttu-id="4340f-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4340f-112">-CdnEndpoint</span></span>
<span data-ttu-id="4340f-113">Указывает объект конечной точки сети CDN, к которому относится источник.</span><span class="sxs-lookup"><span data-stu-id="4340f-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="4340f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4340f-114">-DefaultProfile</span></span>
<span data-ttu-id="4340f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4340f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4340f-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4340f-116">-EndpointName</span></span>
<span data-ttu-id="4340f-117">Указывает имя конечной точки, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="4340f-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="4340f-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="4340f-118">-OriginName</span></span>
<span data-ttu-id="4340f-119">Указывает имя исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="4340f-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="4340f-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="4340f-120">-ProfileName</span></span>
<span data-ttu-id="4340f-121">Указывает имя профиля, которому принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="4340f-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="4340f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4340f-122">-ResourceGroupName</span></span>
<span data-ttu-id="4340f-123">Указывает имя группы ресурсов, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="4340f-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="4340f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4340f-124">-ResourceId</span></span>
<span data-ttu-id="4340f-125">Идентификатор ресурса источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4340f-125">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="4340f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4340f-126">CommonParameters</span></span>
<span data-ttu-id="4340f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4340f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4340f-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4340f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4340f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4340f-129">INPUTS</span></span>

### <span data-ttu-id="4340f-130">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4340f-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4340f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4340f-131">OUTPUTS</span></span>

### <span data-ttu-id="4340f-132">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="4340f-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="4340f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="4340f-133">NOTES</span></span>

## <span data-ttu-id="4340f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4340f-134">RELATED LINKS</span></span>

[<span data-ttu-id="4340f-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="4340f-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


