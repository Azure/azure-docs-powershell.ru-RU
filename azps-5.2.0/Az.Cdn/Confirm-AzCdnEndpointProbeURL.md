---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401492"
---
# <span data-ttu-id="6cdf0-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="6cdf0-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="6cdf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdf0-103">Проверяет URL-адрес, на который он ссылается.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-103">Validates a probe URL.</span></span>

## <span data-ttu-id="6cdf0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6cdf0-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cdf0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cdf0-105">DESCRIPTION</span></span>
<span data-ttu-id="6cdf0-106">Cmdlet **Confirm-AzCdnEndpointProbeURL** подтверждает, можно ли использовать предоставленный URL-адрес для динамического ускорения сайта.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="6cdf0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6cdf0-107">EXAMPLES</span></span>

### <span data-ttu-id="6cdf0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6cdf0-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="6cdf0-109">Проверяет URL-адрес url-адреса с url-адресом " http://www.bing.com/images</span><span class="sxs-lookup"><span data-stu-id="6cdf0-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="6cdf0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cdf0-110">PARAMETERS</span></span>

### <span data-ttu-id="6cdf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cdf0-111">-DefaultProfile</span></span>
<span data-ttu-id="6cdf0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cdf0-113">-СкайпUrl</span><span class="sxs-lookup"><span data-stu-id="6cdf0-113">-ProbeUrl</span></span>
<span data-ttu-id="6cdf0-114">Предлагаемый URL-адрес для проверки.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="6cdf0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdf0-115">CommonParameters</span></span>
<span data-ttu-id="6cdf0-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cdf0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdf0-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cdf0-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdf0-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cdf0-118">INPUTS</span></span>

### <span data-ttu-id="6cdf0-119">Нет</span><span class="sxs-lookup"><span data-stu-id="6cdf0-119">None</span></span>

## <span data-ttu-id="6cdf0-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cdf0-120">OUTPUTS</span></span>

### <span data-ttu-id="6cdf0-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="6cdf0-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="6cdf0-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6cdf0-122">NOTES</span></span>

## <span data-ttu-id="6cdf0-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cdf0-123">RELATED LINKS</span></span>
