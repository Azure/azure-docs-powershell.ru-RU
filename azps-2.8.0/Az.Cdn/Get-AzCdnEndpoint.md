---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 09439fd202d01d6cf5ffc8be614940cdf39ad1ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727612"
---
# <span data-ttu-id="ebdce-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebdce-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="ebdce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebdce-102">SYNOPSIS</span></span>
<span data-ttu-id="ebdce-103">Получает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="ebdce-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="ebdce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebdce-104">SYNTAX</span></span>

### <span data-ttu-id="ebdce-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebdce-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebdce-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebdce-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebdce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebdce-107">DESCRIPTION</span></span>
<span data-ttu-id="ebdce-108">Командлет **Get-AzCdnEndpoint** получает конечную точку сети доставки содержимого (CDN) для Azure и связанные с ней данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ebdce-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="ebdce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebdce-109">EXAMPLES</span></span>

## <span data-ttu-id="ebdce-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebdce-110">PARAMETERS</span></span>

### <span data-ttu-id="ebdce-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ebdce-111">-CdnProfile</span></span>
<span data-ttu-id="ebdce-112">Указывает объект профиля CDN, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="ebdce-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="ebdce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebdce-113">-DefaultProfile</span></span>
<span data-ttu-id="ebdce-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ebdce-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebdce-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ebdce-115">-EndpointName</span></span>
<span data-ttu-id="ebdce-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ebdce-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="ebdce-117">Имя конечной точки не является именем узла конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ebdce-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="ebdce-118">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="ebdce-118">-ProfileName</span></span>
<span data-ttu-id="ebdce-119">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="ebdce-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="ebdce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebdce-120">-ResourceGroupName</span></span>
<span data-ttu-id="ebdce-121">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="ebdce-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="ebdce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebdce-122">CommonParameters</span></span>
<span data-ttu-id="ebdce-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebdce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebdce-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebdce-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebdce-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebdce-125">INPUTS</span></span>

### <span data-ttu-id="ebdce-126">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ebdce-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ebdce-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebdce-127">OUTPUTS</span></span>

### <span data-ttu-id="ebdce-128">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebdce-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ebdce-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebdce-129">NOTES</span></span>

## <span data-ttu-id="ebdce-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebdce-130">RELATED LINKS</span></span>

[<span data-ttu-id="ebdce-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebdce-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="ebdce-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebdce-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="ebdce-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebdce-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="ebdce-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebdce-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="ebdce-135">Остановить-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebdce-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


