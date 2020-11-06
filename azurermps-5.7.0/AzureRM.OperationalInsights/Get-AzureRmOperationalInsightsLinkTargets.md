---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 64e74b2c9d4aa5f22d48bb6cb80c5a1952424c38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561651"
---
# <span data-ttu-id="34ac3-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="34ac3-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="34ac3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="34ac3-103">Возвращает учетные записи, не связанные с подпиской.</span><span class="sxs-lookup"><span data-stu-id="34ac3-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34ac3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34ac3-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34ac3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34ac3-105">DESCRIPTION</span></span>
<span data-ttu-id="34ac3-106">Командлет **Get-AzureRmOperationalInsightsLinkTargets** содержит список существующих учетных записей, не связанных с подпиской Azure.</span><span class="sxs-lookup"><span data-stu-id="34ac3-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="34ac3-107">Чтобы связать новую рабочую область с существующей учетной записью, используйте идентификатор клиента, возвращенный этой операцией, в свойстве идентификатора клиента для новой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="34ac3-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="34ac3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34ac3-108">EXAMPLES</span></span>

### <span data-ttu-id="34ac3-109">Пример 1: получение несвязанных учетных записей</span><span class="sxs-lookup"><span data-stu-id="34ac3-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="34ac3-110">Эта команда получает несвязанные учетные записи, принадлежащие ИДЕНТИФИКАТОРу вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="34ac3-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="34ac3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34ac3-111">PARAMETERS</span></span>

### <span data-ttu-id="34ac3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ac3-112">-DefaultProfile</span></span>
<span data-ttu-id="34ac3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="34ac3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34ac3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ac3-114">CommonParameters</span></span>
<span data-ttu-id="34ac3-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34ac3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ac3-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ac3-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ac3-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34ac3-117">INPUTS</span></span>

### <span data-ttu-id="34ac3-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="34ac3-118">None</span></span>
<span data-ttu-id="34ac3-119">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="34ac3-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34ac3-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34ac3-120">OUTPUTS</span></span>

### <span data-ttu-id="34ac3-121">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="34ac3-121">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="34ac3-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="34ac3-122">NOTES</span></span>

## <span data-ttu-id="34ac3-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34ac3-123">RELATED LINKS</span></span>

[<span data-ttu-id="34ac3-124">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="34ac3-124">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


