---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249310"
---
# <span data-ttu-id="b8cdf-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="b8cdf-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="b8cdf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="b8cdf-103">Возвращает сведения о квоте единицы потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="b8cdf-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="b8cdf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8cdf-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8cdf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8cdf-105">DESCRIPTION</span></span>
<span data-ttu-id="b8cdf-106">Командлет **Get-AzStreamAnalyticsQuota** получает сведения о квоте единицы потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="b8cdf-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="b8cdf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8cdf-107">EXAMPLES</span></span>

### <span data-ttu-id="b8cdf-108">Пример 1: получение сведений о квоте единицы потоковой передачи для региона</span><span class="sxs-lookup"><span data-stu-id="b8cdf-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="b8cdf-109">Эта команда возвращает сведения о квоте и использовании модуля потоковой передачи в регионе Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="b8cdf-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="b8cdf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8cdf-110">PARAMETERS</span></span>

### <span data-ttu-id="b8cdf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8cdf-111">-DefaultProfile</span></span>
<span data-ttu-id="b8cdf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8cdf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8cdf-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b8cdf-113">-Location</span></span>
<span data-ttu-id="b8cdf-114">Указывает имя области Azure или расположение центра обработки данных, для которого требуется получить сведения о квоте единицы потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="b8cdf-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="b8cdf-115"> http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#servicesСписок поддерживаемых областей Azure см.</span><span class="sxs-lookup"><span data-stu-id="b8cdf-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8cdf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8cdf-116">CommonParameters</span></span>
<span data-ttu-id="b8cdf-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8cdf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8cdf-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8cdf-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8cdf-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8cdf-119">INPUTS</span></span>

### <span data-ttu-id="b8cdf-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b8cdf-120">System.String</span></span>

## <span data-ttu-id="b8cdf-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8cdf-121">OUTPUTS</span></span>

### <span data-ttu-id="b8cdf-122">Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="b8cdf-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="b8cdf-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8cdf-123">NOTES</span></span>

## <span data-ttu-id="b8cdf-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8cdf-124">RELATED LINKS</span></span>

[<span data-ttu-id="b8cdf-125">Командлеты Azure Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="b8cdf-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


