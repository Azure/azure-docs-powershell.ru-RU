---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078469"
---
# <span data-ttu-id="9ac4a-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="9ac4a-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="9ac4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ac4a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac4a-103">Проверка пробного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-103">Validates a probe URL.</span></span>

## <span data-ttu-id="9ac4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ac4a-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ac4a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ac4a-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac4a-106">Командлет **Confirm-AzCdnEndpointProbeURL** подтверждает, что указанный URL-адрес пробной проверки можно использовать для ускорения динамического сайта.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="9ac4a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ac4a-107">EXAMPLES</span></span>

### <span data-ttu-id="9ac4a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ac4a-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="9ac4a-109">Проверка URL-адреса пробы " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="9ac4a-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="9ac4a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ac4a-110">PARAMETERS</span></span>

### <span data-ttu-id="9ac4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac4a-111">-DefaultProfile</span></span>
<span data-ttu-id="9ac4a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ac4a-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="9ac4a-113">-ProbeUrl</span></span>
<span data-ttu-id="9ac4a-114">Предложенное имя URL-адреса пробы для проверки.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="9ac4a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac4a-115">CommonParameters</span></span>
<span data-ttu-id="9ac4a-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ac4a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac4a-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ac4a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac4a-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ac4a-118">INPUTS</span></span>

### <span data-ttu-id="9ac4a-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="9ac4a-119">None</span></span>

## <span data-ttu-id="9ac4a-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ac4a-120">OUTPUTS</span></span>

### <span data-ttu-id="9ac4a-121">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="9ac4a-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="9ac4a-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ac4a-122">NOTES</span></span>

## <span data-ttu-id="9ac4a-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ac4a-123">RELATED LINKS</span></span>
