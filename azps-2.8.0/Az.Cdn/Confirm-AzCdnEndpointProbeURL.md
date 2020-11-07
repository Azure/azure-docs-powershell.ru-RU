---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: 517fb30fd95bfc435fcc847a7f9f0765befc21c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727621"
---
# <span data-ttu-id="0e910-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="0e910-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="0e910-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e910-102">SYNOPSIS</span></span>
<span data-ttu-id="0e910-103">Проверка пробного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="0e910-103">Validates a probe URL.</span></span>

## <span data-ttu-id="0e910-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e910-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e910-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e910-105">DESCRIPTION</span></span>
<span data-ttu-id="0e910-106">Командлет **Confirm-AzCdnEndpointProbeURL** подтверждает, что указанный URL-адрес пробной проверки можно использовать для ускорения динамического сайта.</span><span class="sxs-lookup"><span data-stu-id="0e910-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="0e910-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e910-107">EXAMPLES</span></span>

### <span data-ttu-id="0e910-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e910-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="0e910-109">Проверка URL-адреса пробы " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="0e910-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="0e910-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e910-110">PARAMETERS</span></span>

### <span data-ttu-id="0e910-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e910-111">-DefaultProfile</span></span>
<span data-ttu-id="0e910-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e910-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e910-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="0e910-113">-ProbeUrl</span></span>
<span data-ttu-id="0e910-114">Предложенное имя URL-адреса пробы для проверки.</span><span class="sxs-lookup"><span data-stu-id="0e910-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="0e910-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e910-115">CommonParameters</span></span>
<span data-ttu-id="0e910-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e910-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e910-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e910-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e910-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e910-118">INPUTS</span></span>

### <span data-ttu-id="0e910-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="0e910-119">None</span></span>

## <span data-ttu-id="0e910-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e910-120">OUTPUTS</span></span>

### <span data-ttu-id="0e910-121">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="0e910-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="0e910-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e910-122">NOTES</span></span>

## <span data-ttu-id="0e910-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e910-123">RELATED LINKS</span></span>
