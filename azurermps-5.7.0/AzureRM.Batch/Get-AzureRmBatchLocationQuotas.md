---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchlocationquotas
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 1390efccef67e6bfb626e9b31d1a58c72c9fb36e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733577"
---
# <span data-ttu-id="56d1c-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="56d1c-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="56d1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="56d1c-103">Получает квоты пакетной службы для вашей подписки в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="56d1c-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56d1c-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56d1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56d1c-105">DESCRIPTION</span></span>
<span data-ttu-id="56d1c-106">Получает квоты пакетной службы для указанной подписки в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="56d1c-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="56d1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56d1c-107">EXAMPLES</span></span>

### <span data-ttu-id="56d1c-108">Пример 1: получение квот пакетной службы для подписки в регионе "Западная часть США"</span><span class="sxs-lookup"><span data-stu-id="56d1c-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="56d1c-109">Эта команда возвращает квоты для текущей подписки в регионе Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="56d1c-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="56d1c-110">Возвращаемое значение указывает на то, что эта подписка может создавать только одну пакетную учетную запись в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="56d1c-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="56d1c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56d1c-111">PARAMETERS</span></span>

### <span data-ttu-id="56d1c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d1c-112">-DefaultProfile</span></span>
<span data-ttu-id="56d1c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56d1c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d1c-114">-Location</span><span class="sxs-lookup"><span data-stu-id="56d1c-114">-Location</span></span>
<span data-ttu-id="56d1c-115">Указывает регион, для которого этот командлет проверяет квоты.</span><span class="sxs-lookup"><span data-stu-id="56d1c-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="56d1c-116">Дополнительные сведения можно найти в разделе регионы Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="56d1c-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="56d1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d1c-117">CommonParameters</span></span>
<span data-ttu-id="56d1c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56d1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d1c-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d1c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d1c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56d1c-120">INPUTS</span></span>

### <span data-ttu-id="56d1c-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="56d1c-121">None</span></span>
<span data-ttu-id="56d1c-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="56d1c-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56d1c-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56d1c-123">OUTPUTS</span></span>

### <span data-ttu-id="56d1c-124">Microsoft.Azure.Commands.BatCH. Models. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="56d1c-124">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="56d1c-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="56d1c-125">NOTES</span></span>

## <span data-ttu-id="56d1c-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56d1c-126">RELATED LINKS</span></span>

