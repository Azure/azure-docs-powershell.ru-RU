---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: de676da4e276cf7e2b49558c81e9d7f6876d158b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566044"
---
# <span data-ttu-id="05c9c-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="05c9c-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="05c9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="05c9c-103">Возвращает сведения о квоте единицы потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="05c9c-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05c9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05c9c-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05c9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="05c9c-106">Командлет **Get-AzureRmStreamAnalyticsQuota** получает сведения о квоте единицы потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="05c9c-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="05c9c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05c9c-107">EXAMPLES</span></span>

### <span data-ttu-id="05c9c-108">Пример 1: получение сведений о квоте единицы потоковой передачи для региона</span><span class="sxs-lookup"><span data-stu-id="05c9c-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="05c9c-109">Эта команда возвращает сведения о квоте и использовании модуля потоковой передачи в регионе Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="05c9c-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="05c9c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05c9c-110">PARAMETERS</span></span>

### <span data-ttu-id="05c9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c9c-111">-DefaultProfile</span></span>
<span data-ttu-id="05c9c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05c9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05c9c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="05c9c-113">-Location</span></span>
<span data-ttu-id="05c9c-114">Указывает имя области Azure или расположение центра обработки данных, для которого требуется получить сведения о квоте единицы потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="05c9c-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="05c9c-115"> https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#servicesСписок поддерживаемых областей Azure см.</span><span class="sxs-lookup"><span data-stu-id="05c9c-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c9c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c9c-116">CommonParameters</span></span>
<span data-ttu-id="05c9c-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05c9c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c9c-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05c9c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c9c-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05c9c-119">INPUTS</span></span>

### <span data-ttu-id="05c9c-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="05c9c-120">None</span></span>
<span data-ttu-id="05c9c-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="05c9c-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05c9c-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05c9c-122">OUTPUTS</span></span>

### <span data-ttu-id="05c9c-123">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="05c9c-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="05c9c-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="05c9c-124">NOTES</span></span>

## <span data-ttu-id="05c9c-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05c9c-125">RELATED LINKS</span></span>

[<span data-ttu-id="05c9c-126">Командлеты Azure Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="05c9c-126">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


