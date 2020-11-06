---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: 088f9ff5ee1c41b4529353b2740bf9ef1fa8e33c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567167"
---
# <span data-ttu-id="c0530-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0530-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="c0530-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0530-102">SYNOPSIS</span></span>
<span data-ttu-id="c0530-103">Получает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="c0530-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0530-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0530-104">SYNTAX</span></span>

### <span data-ttu-id="c0530-105">Параметры, заданные для параметров полей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0530-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0530-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="c0530-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0530-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0530-107">DESCRIPTION</span></span>
<span data-ttu-id="c0530-108">Командлет **Get-AzureRMCdnEndpoint** получает конечную точку сети доставки содержимого (CDN) для Azure и связанные с ней данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c0530-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="c0530-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0530-109">EXAMPLES</span></span>

## <span data-ttu-id="c0530-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0530-110">PARAMETERS</span></span>

### <span data-ttu-id="c0530-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c0530-111">-CdnProfile</span></span>
<span data-ttu-id="c0530-112">Указывает объект профиля CDN, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="c0530-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0530-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c0530-113">-EndpointName</span></span>
<span data-ttu-id="c0530-114">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c0530-114">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="c0530-115">Имя конечной точки не является именем узла конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c0530-115">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="c0530-116">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="c0530-116">-ProfileName</span></span>
<span data-ttu-id="c0530-117">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="c0530-117">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0530-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0530-118">-ResourceGroupName</span></span>
<span data-ttu-id="c0530-119">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="c0530-119">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0530-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0530-120">-DefaultProfile</span></span>
<span data-ttu-id="c0530-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0530-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0530-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0530-122">CommonParameters</span></span>
<span data-ttu-id="c0530-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0530-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0530-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0530-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0530-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0530-125">INPUTS</span></span>

### <span data-ttu-id="c0530-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="c0530-126">PSProfile</span></span>
<span data-ttu-id="c0530-127">Параметр "CdnProfile" принимает значение типа "PSProfile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0530-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="c0530-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0530-128">OUTPUTS</span></span>

###  
<span data-ttu-id="c0530-129">Этот командлет возвращает объект конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c0530-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="c0530-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0530-130">NOTES</span></span>

## <span data-ttu-id="c0530-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0530-131">RELATED LINKS</span></span>

[<span data-ttu-id="c0530-132">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0530-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="c0530-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0530-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="c0530-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0530-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="c0530-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0530-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="c0530-136">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0530-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


