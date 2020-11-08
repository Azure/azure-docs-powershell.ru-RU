---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236432"
---
# <span data-ttu-id="182c8-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="182c8-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="182c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="182c8-102">SYNOPSIS</span></span>
<span data-ttu-id="182c8-103">Получает метрики квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="182c8-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="182c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="182c8-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="182c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="182c8-105">DESCRIPTION</span></span>
<span data-ttu-id="182c8-106">Получает метрики квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="182c8-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="182c8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="182c8-107">EXAMPLES</span></span>

### <span data-ttu-id="182c8-108">Пример 1. Получение метрик квоты</span><span class="sxs-lookup"><span data-stu-id="182c8-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="182c8-109">Получает сведения о метрике квоты для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="182c8-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="182c8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="182c8-110">PARAMETERS</span></span>

### <span data-ttu-id="182c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="182c8-111">-DefaultProfile</span></span>
<span data-ttu-id="182c8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="182c8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="182c8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="182c8-113">-Name</span></span>
<span data-ttu-id="182c8-114">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="182c8-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="182c8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="182c8-115">-ResourceGroupName</span></span>
<span data-ttu-id="182c8-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="182c8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="182c8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="182c8-117">CommonParameters</span></span>
<span data-ttu-id="182c8-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="182c8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="182c8-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="182c8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="182c8-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="182c8-120">INPUTS</span></span>

### <span data-ttu-id="182c8-121">System. String</span><span class="sxs-lookup"><span data-stu-id="182c8-121">System.String</span></span>

## <span data-ttu-id="182c8-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="182c8-122">OUTPUTS</span></span>

### <span data-ttu-id="182c8-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="182c8-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="182c8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="182c8-124">NOTES</span></span>

## <span data-ttu-id="182c8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="182c8-125">RELATED LINKS</span></span>
