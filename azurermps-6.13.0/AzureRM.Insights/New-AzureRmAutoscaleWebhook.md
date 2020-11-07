---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 607976539e6bf93a0fa947741a4af4d4a7d34b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732480"
---
# <span data-ttu-id="9691a-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="9691a-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="9691a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9691a-102">SYNOPSIS</span></span>
<span data-ttu-id="9691a-103">Создание веб-перехватчика автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9691a-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9691a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9691a-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9691a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9691a-105">DESCRIPTION</span></span>
<span data-ttu-id="9691a-106">Командлет **New-AzureRmAutoscaleWebhook** создает интерфейс автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9691a-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="9691a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9691a-107">EXAMPLES</span></span>

## <span data-ttu-id="9691a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9691a-108">PARAMETERS</span></span>

### <span data-ttu-id="9691a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9691a-109">-DefaultProfile</span></span>
<span data-ttu-id="9691a-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9691a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9691a-111">-Property</span><span class="sxs-lookup"><span data-stu-id="9691a-111">-Property</span></span>
<span data-ttu-id="9691a-112">Задает список свойств в формате @ (property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="9691a-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="9691a-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="9691a-113">-ServiceUri</span></span>
<span data-ttu-id="9691a-114">Указывает URI службы.</span><span class="sxs-lookup"><span data-stu-id="9691a-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="9691a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9691a-115">CommonParameters</span></span>
<span data-ttu-id="9691a-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9691a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9691a-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9691a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9691a-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9691a-118">INPUTS</span></span>

### <span data-ttu-id="9691a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="9691a-119">System.String</span></span>

### <span data-ttu-id="9691a-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9691a-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9691a-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9691a-121">OUTPUTS</span></span>

### <span data-ttu-id="9691a-122">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="9691a-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="9691a-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="9691a-123">NOTES</span></span>

## <span data-ttu-id="9691a-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9691a-124">RELATED LINKS</span></span>

[<span data-ttu-id="9691a-125">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="9691a-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


