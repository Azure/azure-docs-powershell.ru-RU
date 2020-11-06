---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 952cf5d9f0eff288a65df2dd2917d341582237db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568584"
---
# <span data-ttu-id="62e73-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="62e73-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="62e73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62e73-102">SYNOPSIS</span></span>
<span data-ttu-id="62e73-103">Получает метрики квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="62e73-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62e73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62e73-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62e73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62e73-105">DESCRIPTION</span></span>
<span data-ttu-id="62e73-106">Получает метрики квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="62e73-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="62e73-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62e73-107">EXAMPLES</span></span>

### <span data-ttu-id="62e73-108">Пример 1. Получение метрик квоты</span><span class="sxs-lookup"><span data-stu-id="62e73-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="62e73-109">Получает сведения о метрике квоты для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="62e73-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="62e73-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62e73-110">PARAMETERS</span></span>

### <span data-ttu-id="62e73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e73-111">-DefaultProfile</span></span>
<span data-ttu-id="62e73-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="62e73-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62e73-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62e73-113">-Name</span></span>
<span data-ttu-id="62e73-114">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="62e73-114">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e73-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e73-115">-ResourceGroupName</span></span>
<span data-ttu-id="62e73-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="62e73-116">Resource Group Name</span></span>

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

### <span data-ttu-id="62e73-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e73-117">CommonParameters</span></span>
<span data-ttu-id="62e73-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62e73-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e73-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62e73-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e73-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62e73-120">INPUTS</span></span>

### <span data-ttu-id="62e73-121">System. String</span><span class="sxs-lookup"><span data-stu-id="62e73-121">System.String</span></span>

## <span data-ttu-id="62e73-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62e73-122">OUTPUTS</span></span>

### <span data-ttu-id="62e73-123">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. IotHub... Models. PSIotHubQuotaMetric, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = "нейтрально", PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="62e73-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="62e73-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="62e73-124">NOTES</span></span>

## <span data-ttu-id="62e73-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62e73-125">RELATED LINKS</span></span>

