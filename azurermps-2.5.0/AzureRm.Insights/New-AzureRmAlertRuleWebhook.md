---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
ms.openlocfilehash: d45624da172ecafba48354968d5a3ac5531be693
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915286"
---
# <span data-ttu-id="088af-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="088af-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="088af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="088af-102">SYNOPSIS</span></span>
<span data-ttu-id="088af-103">Создание веб-перехватчика правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="088af-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="088af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="088af-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="088af-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="088af-105">DESCRIPTION</span></span>
<span data-ttu-id="088af-106">Командлет **New-AzureRmAlertRuleWebhook** создает интерфейсный обработчик для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="088af-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="088af-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="088af-107">EXAMPLES</span></span>

### <span data-ttu-id="088af-108">Пример 1: создание веб-перехватчика правила оповещения</span><span class="sxs-lookup"><span data-stu-id="088af-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="088af-109">Эта команда создает веб-перехватчик правила оповещения, указывая только URI-адрес службы.</span><span class="sxs-lookup"><span data-stu-id="088af-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="088af-110">Пример 2: создание веб-перехватчика с одним свойством</span><span class="sxs-lookup"><span data-stu-id="088af-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="088af-111">Эта команда создает веб-перехватчик правила оповещения для Contoso.com с одним свойством, а затем сохраняет его в переменной $Actual.</span><span class="sxs-lookup"><span data-stu-id="088af-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="088af-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="088af-112">PARAMETERS</span></span>

### <span data-ttu-id="088af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="088af-113">-DefaultProfile</span></span>
<span data-ttu-id="088af-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="088af-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="088af-115">-Property</span><span class="sxs-lookup"><span data-stu-id="088af-115">-Property</span></span>
<span data-ttu-id="088af-116">Задает список свойств в формате @ (property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="088af-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="088af-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="088af-117">-ServiceUri</span></span>
<span data-ttu-id="088af-118">Указывает URI службы.</span><span class="sxs-lookup"><span data-stu-id="088af-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="088af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="088af-119">CommonParameters</span></span>
<span data-ttu-id="088af-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="088af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="088af-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="088af-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="088af-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="088af-122">INPUTS</span></span>

### <span data-ttu-id="088af-123">System. String</span><span class="sxs-lookup"><span data-stu-id="088af-123">System.String</span></span>

### <span data-ttu-id="088af-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="088af-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="088af-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="088af-125">OUTPUTS</span></span>

### <span data-ttu-id="088af-126">Microsoft. Azure. Management. Monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="088af-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="088af-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="088af-127">NOTES</span></span>

## <span data-ttu-id="088af-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="088af-128">RELATED LINKS</span></span>



[<span data-ttu-id="088af-129">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="088af-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="088af-130">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="088af-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="088af-131">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="088af-131">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="088af-132">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="088af-132">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


