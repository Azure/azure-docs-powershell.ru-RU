---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/confirm-azurermcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
ms.openlocfilehash: d6cf25c352c89592112aaa0a60cf7ba14ff7acf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565901"
---
# <span data-ttu-id="1a746-101">Confirm-AzureRmCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="1a746-101">Confirm-AzureRmCdnEndpointProbeURL</span></span>

## <span data-ttu-id="1a746-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a746-102">SYNOPSIS</span></span>
<span data-ttu-id="1a746-103">Проверка пробного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="1a746-103">Validates a probe URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a746-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a746-104">SYNTAX</span></span>

```
Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a746-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a746-105">DESCRIPTION</span></span>
<span data-ttu-id="1a746-106">Командлет **Confirm-AzureRmCdnEndpointProbeURL** подтверждает, что указанный URL-адрес пробной проверки можно использовать для ускорения динамического сайта.</span><span class="sxs-lookup"><span data-stu-id="1a746-106">The **Confirm-AzureRmCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="1a746-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a746-107">EXAMPLES</span></span>

### <span data-ttu-id="1a746-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a746-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="1a746-109">Проверка URL-адреса пробы " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="1a746-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="1a746-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a746-110">PARAMETERS</span></span>

### <span data-ttu-id="1a746-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a746-111">-DefaultProfile</span></span>
<span data-ttu-id="1a746-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a746-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a746-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="1a746-113">-ProbeUrl</span></span>
<span data-ttu-id="1a746-114">Предложенное имя URL-адреса пробы для проверки.</span><span class="sxs-lookup"><span data-stu-id="1a746-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="1a746-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a746-115">CommonParameters</span></span>
<span data-ttu-id="1a746-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a746-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a746-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a746-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a746-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a746-118">INPUTS</span></span>

### <span data-ttu-id="1a746-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="1a746-119">None</span></span>

## <span data-ttu-id="1a746-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a746-120">OUTPUTS</span></span>

### <span data-ttu-id="1a746-121">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="1a746-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="1a746-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a746-122">NOTES</span></span>

## <span data-ttu-id="1a746-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a746-123">RELATED LINKS</span></span>
