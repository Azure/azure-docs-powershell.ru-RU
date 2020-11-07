---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
ms.openlocfilehash: fe6170842bcacf4d7fb0c8e442dc988c03c67e35
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913890"
---
# <span data-ttu-id="6337c-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="6337c-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="6337c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6337c-102">SYNOPSIS</span></span>
<span data-ttu-id="6337c-103">Создание веб-перехватчика автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="6337c-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6337c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6337c-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6337c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6337c-105">DESCRIPTION</span></span>
<span data-ttu-id="6337c-106">Командлет **New-AzureRmAutoscaleWebhook** создает интерфейс автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="6337c-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="6337c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6337c-107">EXAMPLES</span></span>

## <span data-ttu-id="6337c-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6337c-108">PARAMETERS</span></span>

### <span data-ttu-id="6337c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6337c-109">-DefaultProfile</span></span>
<span data-ttu-id="6337c-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6337c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6337c-111">-Property</span><span class="sxs-lookup"><span data-stu-id="6337c-111">-Property</span></span>
<span data-ttu-id="6337c-112">Задает список свойств в формате @ (property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="6337c-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6337c-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="6337c-113">-ServiceUri</span></span>
<span data-ttu-id="6337c-114">Указывает URI службы.</span><span class="sxs-lookup"><span data-stu-id="6337c-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="6337c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6337c-115">CommonParameters</span></span>
<span data-ttu-id="6337c-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6337c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6337c-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6337c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6337c-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6337c-118">INPUTS</span></span>

### <span data-ttu-id="6337c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="6337c-119">System.String</span></span>

### <span data-ttu-id="6337c-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6337c-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6337c-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6337c-121">OUTPUTS</span></span>

### <span data-ttu-id="6337c-122">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="6337c-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="6337c-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="6337c-123">NOTES</span></span>

## <span data-ttu-id="6337c-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6337c-124">RELATED LINKS</span></span>

[<span data-ttu-id="6337c-125">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6337c-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


