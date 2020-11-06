---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559419"
---
# <span data-ttu-id="49e6a-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="49e6a-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="49e6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="49e6a-103">Возвращает сведения о квоте единицы потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="49e6a-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49e6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49e6a-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49e6a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="49e6a-106">Командлет **Get-AzureRmStreamAnalyticsQuota** получает сведения о квоте единицы потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="49e6a-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="49e6a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49e6a-107">EXAMPLES</span></span>

### <span data-ttu-id="49e6a-108">Пример 1: получение сведений о квоте единицы потоковой передачи для региона</span><span class="sxs-lookup"><span data-stu-id="49e6a-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="49e6a-109">Эта команда возвращает сведения о квоте и использовании модуля потоковой передачи в регионе Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="49e6a-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="49e6a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49e6a-110">PARAMETERS</span></span>

### <span data-ttu-id="49e6a-111">-Location</span><span class="sxs-lookup"><span data-stu-id="49e6a-111">-Location</span></span>
<span data-ttu-id="49e6a-112">Указывает имя области Azure или расположение центра обработки данных, для которого требуется получить сведения о квоте единицы потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="49e6a-112">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="49e6a-113"> https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#servicesСписок поддерживаемых областей Azure см.</span><span class="sxs-lookup"><span data-stu-id="49e6a-113">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="49e6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e6a-114">-DefaultProfile</span></span>
<span data-ttu-id="49e6a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49e6a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49e6a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e6a-116">CommonParameters</span></span>
<span data-ttu-id="49e6a-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49e6a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e6a-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e6a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e6a-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49e6a-119">INPUTS</span></span>

## <span data-ttu-id="49e6a-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49e6a-120">OUTPUTS</span></span>

### <span data-ttu-id="49e6a-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="49e6a-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="49e6a-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="49e6a-122">NOTES</span></span>

## <span data-ttu-id="49e6a-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49e6a-123">RELATED LINKS</span></span>

[<span data-ttu-id="49e6a-124">Командлеты Azure Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="49e6a-124">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


