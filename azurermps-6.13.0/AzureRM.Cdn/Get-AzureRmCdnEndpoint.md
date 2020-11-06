---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: eb4215a281b83bd533a7502e3ec538ec4e3a570c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566836"
---
# <span data-ttu-id="3ffeb-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ffeb-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="3ffeb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ffeb-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffeb-103">Получает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="3ffeb-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ffeb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ffeb-104">SYNTAX</span></span>

### <span data-ttu-id="3ffeb-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ffeb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ffeb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ffeb-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ffeb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ffeb-107">DESCRIPTION</span></span>
<span data-ttu-id="3ffeb-108">Командлет **Get-AzureRMCdnEndpoint** получает конечную точку сети доставки содержимого (CDN) для Azure и связанные с ней данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ffeb-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="3ffeb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ffeb-109">EXAMPLES</span></span>

## <span data-ttu-id="3ffeb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ffeb-110">PARAMETERS</span></span>

### <span data-ttu-id="3ffeb-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="3ffeb-111">-CdnProfile</span></span>
<span data-ttu-id="3ffeb-112">Указывает объект профиля CDN, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="3ffeb-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3ffeb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffeb-113">-DefaultProfile</span></span>
<span data-ttu-id="3ffeb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3ffeb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffeb-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3ffeb-115">-EndpointName</span></span>
<span data-ttu-id="3ffeb-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3ffeb-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="3ffeb-117">Имя конечной точки не является именем узла конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3ffeb-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="3ffeb-118">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="3ffeb-118">-ProfileName</span></span>
<span data-ttu-id="3ffeb-119">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="3ffeb-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3ffeb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ffeb-120">-ResourceGroupName</span></span>
<span data-ttu-id="3ffeb-121">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="3ffeb-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3ffeb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffeb-122">CommonParameters</span></span>
<span data-ttu-id="3ffeb-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ffeb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffeb-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ffeb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffeb-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ffeb-125">INPUTS</span></span>

### <span data-ttu-id="3ffeb-126">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="3ffeb-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="3ffeb-127">Параметры: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ffeb-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="3ffeb-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ffeb-128">OUTPUTS</span></span>

### <span data-ttu-id="3ffeb-129">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ffeb-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="3ffeb-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ffeb-130">NOTES</span></span>

## <span data-ttu-id="3ffeb-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ffeb-131">RELATED LINKS</span></span>

[<span data-ttu-id="3ffeb-132">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ffeb-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="3ffeb-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ffeb-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="3ffeb-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ffeb-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="3ffeb-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ffeb-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="3ffeb-136">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ffeb-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


