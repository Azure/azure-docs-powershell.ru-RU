---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217073"
---
# <span data-ttu-id="1e122-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="1e122-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="1e122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e122-102">SYNOPSIS</span></span>
<span data-ttu-id="1e122-103">Получает сведения о квоте потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="1e122-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="1e122-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1e122-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e122-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e122-105">DESCRIPTION</span></span>
<span data-ttu-id="1e122-106">С **помощью cmdlet get-AzStreamAnalyticsQuota** можно получить сведения о квоте потоковой передачи для региона.</span><span class="sxs-lookup"><span data-stu-id="1e122-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="1e122-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1e122-107">EXAMPLES</span></span>

### <span data-ttu-id="1e122-108">ПРИМЕР 1. Просмотр сведений о квоте потоковой передачи для региона</span><span class="sxs-lookup"><span data-stu-id="1e122-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="1e122-109">Эта команда возвращает сведения о квоте потоковой передачи и использовании ресурсов в западной части США.</span><span class="sxs-lookup"><span data-stu-id="1e122-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="1e122-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e122-110">PARAMETERS</span></span>

### <span data-ttu-id="1e122-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e122-111">-DefaultProfile</span></span>
<span data-ttu-id="1e122-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e122-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e122-113">-Location</span><span class="sxs-lookup"><span data-stu-id="1e122-113">-Location</span></span>
<span data-ttu-id="1e122-114">Название региона или расположения центра обработки данных Azure, для которого нужно получить сведения о квоте потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="1e122-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="1e122-115">Список http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services поддерживаемых регионов Azure см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="1e122-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="1e122-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e122-116">CommonParameters</span></span>
<span data-ttu-id="1e122-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e122-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e122-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e122-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e122-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e122-119">INPUTS</span></span>

### <span data-ttu-id="1e122-120">System.String</span><span class="sxs-lookup"><span data-stu-id="1e122-120">System.String</span></span>

## <span data-ttu-id="1e122-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e122-121">OUTPUTS</span></span>

### <span data-ttu-id="1e122-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span><span class="sxs-lookup"><span data-stu-id="1e122-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="1e122-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1e122-123">NOTES</span></span>

## <span data-ttu-id="1e122-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e122-124">RELATED LINKS</span></span>

[<span data-ttu-id="1e122-125">Azure Stream Analytics Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1e122-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


