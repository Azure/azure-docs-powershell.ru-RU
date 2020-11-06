---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 3f0418a06b11af933cfc7ad09a2c0fc492db4f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567552"
---
# <span data-ttu-id="74ccd-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="74ccd-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="74ccd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="74ccd-103">Возвращает учетные записи, не связанные с подпиской.</span><span class="sxs-lookup"><span data-stu-id="74ccd-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74ccd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74ccd-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74ccd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74ccd-105">DESCRIPTION</span></span>
<span data-ttu-id="74ccd-106">Командлет **Get-AzureRmOperationalInsightsLinkTargets** содержит список существующих учетных записей, не связанных с подпиской Azure.</span><span class="sxs-lookup"><span data-stu-id="74ccd-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="74ccd-107">Чтобы связать новую рабочую область с существующей учетной записью, используйте идентификатор клиента, возвращенный этой операцией, в свойстве идентификатора клиента для новой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="74ccd-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="74ccd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74ccd-108">EXAMPLES</span></span>

### <span data-ttu-id="74ccd-109">Пример 1: получение несвязанных учетных записей</span><span class="sxs-lookup"><span data-stu-id="74ccd-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="74ccd-110">Эта команда получает несвязанные учетные записи, принадлежащие ИДЕНТИФИКАТОРу вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="74ccd-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="74ccd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74ccd-111">PARAMETERS</span></span>

### <span data-ttu-id="74ccd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ccd-112">-DefaultProfile</span></span>
<span data-ttu-id="74ccd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74ccd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74ccd-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ccd-114">CommonParameters</span></span>
<span data-ttu-id="74ccd-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74ccd-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ccd-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74ccd-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ccd-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74ccd-117">INPUTS</span></span>

## <span data-ttu-id="74ccd-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74ccd-118">OUTPUTS</span></span>

### <span data-ttu-id="74ccd-119">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="74ccd-119">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="74ccd-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="74ccd-120">NOTES</span></span>

## <span data-ttu-id="74ccd-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74ccd-121">RELATED LINKS</span></span>

[<span data-ttu-id="74ccd-122">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="74ccd-122">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


