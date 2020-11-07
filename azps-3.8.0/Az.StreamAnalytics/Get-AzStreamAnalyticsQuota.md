---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912969"
---
# <span data-ttu-id="e2907-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="e2907-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="e2907-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2907-102">SYNOPSIS</span></span>
<span data-ttu-id="e2907-103">Возвращает сведения о квоте единицы потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="e2907-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="e2907-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2907-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2907-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2907-105">DESCRIPTION</span></span>
<span data-ttu-id="e2907-106">Командлет **Get-AzStreamAnalyticsQuota** получает сведения о квоте единицы потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="e2907-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="e2907-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2907-107">EXAMPLES</span></span>

### <span data-ttu-id="e2907-108">Пример 1: получение сведений о квоте единицы потоковой передачи для региона</span><span class="sxs-lookup"><span data-stu-id="e2907-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="e2907-109">Эта команда возвращает сведения о квоте и использовании модуля потоковой передачи в регионе Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="e2907-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="e2907-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2907-110">PARAMETERS</span></span>

### <span data-ttu-id="e2907-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2907-111">-DefaultProfile</span></span>
<span data-ttu-id="e2907-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2907-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2907-113">-Location</span><span class="sxs-lookup"><span data-stu-id="e2907-113">-Location</span></span>
<span data-ttu-id="e2907-114">Указывает имя области Azure или расположение центра обработки данных, для которого требуется получить сведения о квоте единицы потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="e2907-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="e2907-115"> http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#servicesСписок поддерживаемых областей Azure см.</span><span class="sxs-lookup"><span data-stu-id="e2907-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="e2907-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2907-116">CommonParameters</span></span>
<span data-ttu-id="e2907-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2907-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2907-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2907-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2907-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2907-119">INPUTS</span></span>

### <span data-ttu-id="e2907-120">System. String</span><span class="sxs-lookup"><span data-stu-id="e2907-120">System.String</span></span>

## <span data-ttu-id="e2907-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2907-121">OUTPUTS</span></span>

### <span data-ttu-id="e2907-122">Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="e2907-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="e2907-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2907-123">NOTES</span></span>

## <span data-ttu-id="e2907-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2907-124">RELATED LINKS</span></span>

[<span data-ttu-id="e2907-125">Командлеты Azure Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="e2907-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


