---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: 24f882ce9190553028a7d0eed80480da4c4f2bfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564899"
---
# <span data-ttu-id="be32e-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="be32e-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="be32e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be32e-102">SYNOPSIS</span></span>
<span data-ttu-id="be32e-103">Создание веб-перехватчика правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="be32e-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be32e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be32e-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be32e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be32e-105">DESCRIPTION</span></span>
<span data-ttu-id="be32e-106">Командлет **New-AzureRmAlertRuleWebhook** создает интерфейсный обработчик для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="be32e-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="be32e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be32e-107">EXAMPLES</span></span>

### <span data-ttu-id="be32e-108">Пример 1: создание веб-перехватчика правила оповещения</span><span class="sxs-lookup"><span data-stu-id="be32e-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="be32e-109">Эта команда создает веб-перехватчик правила оповещения, указывая только URI-адрес службы.</span><span class="sxs-lookup"><span data-stu-id="be32e-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="be32e-110">Пример 2: создание веб-перехватчика с одним свойством</span><span class="sxs-lookup"><span data-stu-id="be32e-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="be32e-111">Эта команда создает веб-перехватчик правила оповещения для Contoso.com с одним свойством, а затем сохраняет его в переменной $Actual.</span><span class="sxs-lookup"><span data-stu-id="be32e-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="be32e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be32e-112">PARAMETERS</span></span>

### <span data-ttu-id="be32e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be32e-113">-DefaultProfile</span></span>
<span data-ttu-id="be32e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="be32e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be32e-115">-Property</span><span class="sxs-lookup"><span data-stu-id="be32e-115">-Property</span></span>
<span data-ttu-id="be32e-116">Задает список свойств в формате @ (property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="be32e-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Properties

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be32e-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="be32e-117">-ServiceUri</span></span>
<span data-ttu-id="be32e-118">Указывает URI службы.</span><span class="sxs-lookup"><span data-stu-id="be32e-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="be32e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be32e-119">CommonParameters</span></span>
<span data-ttu-id="be32e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be32e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be32e-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be32e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be32e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be32e-122">INPUTS</span></span>

### <span data-ttu-id="be32e-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="be32e-123">None</span></span>
<span data-ttu-id="be32e-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="be32e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be32e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be32e-125">OUTPUTS</span></span>

### <span data-ttu-id="be32e-126">Microsoft. Azure. Management. Monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="be32e-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="be32e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="be32e-127">NOTES</span></span>

## <span data-ttu-id="be32e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be32e-128">RELATED LINKS</span></span>

[<span data-ttu-id="be32e-129">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="be32e-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="be32e-130">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="be32e-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="be32e-131">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="be32e-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="be32e-132">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="be32e-132">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="be32e-133">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="be32e-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


