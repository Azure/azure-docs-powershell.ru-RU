---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079837"
---
# <span data-ttu-id="108f4-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="108f4-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="108f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="108f4-102">SYNOPSIS</span></span>
<span data-ttu-id="108f4-103">Получает квоты пакетной службы для вашей подписки в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="108f4-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="108f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="108f4-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="108f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="108f4-105">DESCRIPTION</span></span>
<span data-ttu-id="108f4-106">Получает квоты пакетной службы для указанной подписки в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="108f4-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="108f4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="108f4-107">EXAMPLES</span></span>

### <span data-ttu-id="108f4-108">Пример 1: получение квот пакетной службы для подписки в регионе "Западная часть США"</span><span class="sxs-lookup"><span data-stu-id="108f4-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="108f4-109">Эта команда возвращает квоты для текущей подписки в регионе Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="108f4-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="108f4-110">Возвращаемое значение указывает на то, что эта подписка может создавать только одну пакетную учетную запись в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="108f4-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="108f4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="108f4-111">PARAMETERS</span></span>

### <span data-ttu-id="108f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108f4-112">-DefaultProfile</span></span>
<span data-ttu-id="108f4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="108f4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="108f4-114">-Location</span><span class="sxs-lookup"><span data-stu-id="108f4-114">-Location</span></span>
<span data-ttu-id="108f4-115">Указывает регион, для которого этот командлет проверяет квоты.</span><span class="sxs-lookup"><span data-stu-id="108f4-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="108f4-116">Дополнительные сведения можно найти в разделе регионы Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="108f4-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="108f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108f4-117">CommonParameters</span></span>
<span data-ttu-id="108f4-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="108f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108f4-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="108f4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108f4-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="108f4-120">INPUTS</span></span>

### <span data-ttu-id="108f4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="108f4-121">System.String</span></span>

## <span data-ttu-id="108f4-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="108f4-122">OUTPUTS</span></span>

### <span data-ttu-id="108f4-123">Microsoft.Azure.Commands.BatCH. Models. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="108f4-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="108f4-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="108f4-124">NOTES</span></span>

## <span data-ttu-id="108f4-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="108f4-125">RELATED LINKS</span></span>
