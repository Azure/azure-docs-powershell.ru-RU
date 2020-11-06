---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: d3e33e8bf6dea2e06e8ee72199e040a563d0d974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559264"
---
# <span data-ttu-id="ebfbf-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebfbf-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="ebfbf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebfbf-102">SYNOPSIS</span></span>
<span data-ttu-id="ebfbf-103">Получает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebfbf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebfbf-104">SYNTAX</span></span>

### <span data-ttu-id="ebfbf-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebfbf-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebfbf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfbf-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebfbf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebfbf-107">DESCRIPTION</span></span>
<span data-ttu-id="ebfbf-108">Командлет **Get-AzureRMCdnEndpoint** получает конечную точку сети доставки содержимого (CDN) для Azure и связанные с ней данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="ebfbf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebfbf-109">EXAMPLES</span></span>

## <span data-ttu-id="ebfbf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebfbf-110">PARAMETERS</span></span>

### <span data-ttu-id="ebfbf-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ebfbf-111">-CdnProfile</span></span>
<span data-ttu-id="ebfbf-112">Указывает объект профиля CDN, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebfbf-113">-DefaultProfile</span></span>
<span data-ttu-id="ebfbf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ebfbf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfbf-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ebfbf-115">-EndpointName</span></span>
<span data-ttu-id="ebfbf-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="ebfbf-117">Имя конечной точки не является именем узла конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-117">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfbf-118">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="ebfbf-118">-ProfileName</span></span>
<span data-ttu-id="ebfbf-119">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfbf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebfbf-120">-ResourceGroupName</span></span>
<span data-ttu-id="ebfbf-121">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfbf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfbf-122">CommonParameters</span></span>
<span data-ttu-id="ebfbf-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfbf-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebfbf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfbf-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebfbf-125">INPUTS</span></span>

### <span data-ttu-id="ebfbf-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="ebfbf-126">PSProfile</span></span>
<span data-ttu-id="ebfbf-127">Параметр "CdnProfile" принимает значение типа "PSProfile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="ebfbf-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebfbf-128">OUTPUTS</span></span>

###  
<span data-ttu-id="ebfbf-129">Этот командлет возвращает объект конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ebfbf-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="ebfbf-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebfbf-130">NOTES</span></span>

## <span data-ttu-id="ebfbf-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebfbf-131">RELATED LINKS</span></span>

[<span data-ttu-id="ebfbf-132">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebfbf-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ebfbf-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebfbf-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ebfbf-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebfbf-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ebfbf-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebfbf-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ebfbf-136">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebfbf-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


