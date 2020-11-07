---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 1de2d49d6e914635f8fc0d38ffa81755cc622481
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734392"
---
# <span data-ttu-id="ed27c-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="ed27c-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="ed27c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed27c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed27c-103">Получает метрики квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="ed27c-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed27c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed27c-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed27c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed27c-105">DESCRIPTION</span></span>
<span data-ttu-id="ed27c-106">Получает метрики квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="ed27c-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="ed27c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed27c-107">EXAMPLES</span></span>

### <span data-ttu-id="ed27c-108">Пример 1. Получение метрик квоты</span><span class="sxs-lookup"><span data-stu-id="ed27c-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ed27c-109">Получает сведения о метрике квоты для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ed27c-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ed27c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed27c-110">PARAMETERS</span></span>

### <span data-ttu-id="ed27c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed27c-111">-DefaultProfile</span></span>
<span data-ttu-id="ed27c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed27c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed27c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed27c-113">-Name</span></span>
<span data-ttu-id="ed27c-114">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="ed27c-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed27c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed27c-115">-ResourceGroupName</span></span>
<span data-ttu-id="ed27c-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ed27c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="ed27c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed27c-117">CommonParameters</span></span>
<span data-ttu-id="ed27c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed27c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed27c-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed27c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed27c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed27c-120">INPUTS</span></span>

### <span data-ttu-id="ed27c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ed27c-121">System.String</span></span>

## <span data-ttu-id="ed27c-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed27c-122">OUTPUTS</span></span>

### <span data-ttu-id="ed27c-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="ed27c-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="ed27c-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed27c-124">NOTES</span></span>

## <span data-ttu-id="ed27c-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed27c-125">RELATED LINKS</span></span>
