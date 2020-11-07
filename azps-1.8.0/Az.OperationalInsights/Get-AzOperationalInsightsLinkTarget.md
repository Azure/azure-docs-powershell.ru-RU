---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: beb4fad10424a94b2623070508ac827ea7b15306
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731941"
---
# <span data-ttu-id="1c48a-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="1c48a-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="1c48a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c48a-102">SYNOPSIS</span></span>
<span data-ttu-id="1c48a-103">Возвращает учетные записи, не связанные с подпиской.</span><span class="sxs-lookup"><span data-stu-id="1c48a-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="1c48a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c48a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c48a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c48a-105">DESCRIPTION</span></span>
<span data-ttu-id="1c48a-106">Командлет **Get-AzOperationalInsightsLinkTarget** содержит список существующих учетных записей, не связанных с подпиской Azure.</span><span class="sxs-lookup"><span data-stu-id="1c48a-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="1c48a-107">Чтобы связать новую рабочую область с существующей учетной записью, используйте идентификатор клиента, возвращенный этой операцией, в свойстве идентификатора клиента для новой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1c48a-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="1c48a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c48a-108">EXAMPLES</span></span>

### <span data-ttu-id="1c48a-109">Пример 1: получение несвязанных учетных записей</span><span class="sxs-lookup"><span data-stu-id="1c48a-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="1c48a-110">Эта команда получает несвязанные учетные записи, принадлежащие ИДЕНТИФИКАТОРу вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="1c48a-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="1c48a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c48a-111">PARAMETERS</span></span>

### <span data-ttu-id="1c48a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c48a-112">-DefaultProfile</span></span>
<span data-ttu-id="1c48a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1c48a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c48a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c48a-114">CommonParameters</span></span>
<span data-ttu-id="1c48a-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c48a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c48a-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c48a-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c48a-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c48a-117">INPUTS</span></span>

### <span data-ttu-id="1c48a-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="1c48a-118">None</span></span>

## <span data-ttu-id="1c48a-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c48a-119">OUTPUTS</span></span>

### <span data-ttu-id="1c48a-120">Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="1c48a-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="1c48a-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c48a-121">NOTES</span></span>

## <span data-ttu-id="1c48a-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c48a-122">RELATED LINKS</span></span>

[<span data-ttu-id="1c48a-123">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="1c48a-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


