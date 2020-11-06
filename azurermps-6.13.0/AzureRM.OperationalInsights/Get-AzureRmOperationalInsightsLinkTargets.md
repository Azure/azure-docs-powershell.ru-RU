---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: a1040e5fe810a5dfbbb2e41daf7e8933102e3799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560815"
---
# <span data-ttu-id="e9b56-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="e9b56-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="e9b56-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9b56-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b56-103">Возвращает учетные записи, не связанные с подпиской.</span><span class="sxs-lookup"><span data-stu-id="e9b56-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9b56-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9b56-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9b56-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9b56-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b56-106">Командлет **Get-AzureRmOperationalInsightsLinkTargets** содержит список существующих учетных записей, не связанных с подпиской Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b56-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="e9b56-107">Чтобы связать новую рабочую область с существующей учетной записью, используйте идентификатор клиента, возвращенный этой операцией, в свойстве идентификатора клиента для новой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e9b56-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="e9b56-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9b56-108">EXAMPLES</span></span>

### <span data-ttu-id="e9b56-109">Пример 1: получение несвязанных учетных записей</span><span class="sxs-lookup"><span data-stu-id="e9b56-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="e9b56-110">Эта команда получает несвязанные учетные записи, принадлежащие ИДЕНТИФИКАТОРу вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="e9b56-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="e9b56-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9b56-111">PARAMETERS</span></span>

### <span data-ttu-id="e9b56-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b56-112">-DefaultProfile</span></span>
<span data-ttu-id="e9b56-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e9b56-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9b56-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b56-114">CommonParameters</span></span>
<span data-ttu-id="e9b56-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9b56-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b56-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b56-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b56-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9b56-117">INPUTS</span></span>

### <span data-ttu-id="e9b56-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="e9b56-118">None</span></span>

## <span data-ttu-id="e9b56-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9b56-119">OUTPUTS</span></span>

### <span data-ttu-id="e9b56-120">Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="e9b56-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="e9b56-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9b56-121">NOTES</span></span>

## <span data-ttu-id="e9b56-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9b56-122">RELATED LINKS</span></span>

[<span data-ttu-id="e9b56-123">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="e9b56-123">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


