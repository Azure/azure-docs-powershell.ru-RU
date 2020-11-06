---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: 6c5c11123ab39d92bb7b702542b007c8c075f9b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567166"
---
# <span data-ttu-id="b8916-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b8916-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="b8916-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8916-102">SYNOPSIS</span></span>
<span data-ttu-id="b8916-103">Получает состояние доступности конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="b8916-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8916-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8916-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8916-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8916-105">DESCRIPTION</span></span>
<span data-ttu-id="b8916-106">Командлет **Get-AzureRmCdnEndpointNameAvailability** получает состояние доступности конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="b8916-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b8916-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8916-107">EXAMPLES</span></span>

## <span data-ttu-id="b8916-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8916-108">PARAMETERS</span></span>

### <span data-ttu-id="b8916-109">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b8916-109">-EndpointName</span></span>
<span data-ttu-id="b8916-110">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b8916-110">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8916-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8916-111">-DefaultProfile</span></span>
<span data-ttu-id="b8916-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8916-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8916-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8916-113">CommonParameters</span></span>
<span data-ttu-id="b8916-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8916-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8916-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8916-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8916-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8916-116">INPUTS</span></span>

## <span data-ttu-id="b8916-117">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8916-117">OUTPUTS</span></span>

### <span data-ttu-id="b8916-118">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="b8916-118">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="b8916-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8916-119">NOTES</span></span>

## <span data-ttu-id="b8916-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8916-120">RELATED LINKS</span></span>

