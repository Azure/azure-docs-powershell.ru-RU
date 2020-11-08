---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065583"
---
# <span data-ttu-id="dc197-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="dc197-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="dc197-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc197-102">SYNOPSIS</span></span>
<span data-ttu-id="dc197-103">Создание веб-перехватчика правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="dc197-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="dc197-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc197-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc197-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc197-105">DESCRIPTION</span></span>
<span data-ttu-id="dc197-106">Командлет **New-AzAlertRuleWebhook** создает интерфейсный обработчик для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="dc197-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="dc197-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc197-107">EXAMPLES</span></span>

### <span data-ttu-id="dc197-108">Пример 1: создание веб-перехватчика правила оповещения</span><span class="sxs-lookup"><span data-stu-id="dc197-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="dc197-109">Эта команда создает веб-перехватчик правила оповещения, указывая только URI-адрес службы.</span><span class="sxs-lookup"><span data-stu-id="dc197-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="dc197-110">Пример 2: создание веб-перехватчика с одним свойством</span><span class="sxs-lookup"><span data-stu-id="dc197-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="dc197-111">Эта команда создает веб-перехватчик правила оповещения для Contoso.com с одним свойством, а затем сохраняет его в переменной $Actual.</span><span class="sxs-lookup"><span data-stu-id="dc197-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="dc197-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc197-112">PARAMETERS</span></span>

### <span data-ttu-id="dc197-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc197-113">-DefaultProfile</span></span>
<span data-ttu-id="dc197-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dc197-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc197-115">-Property</span><span class="sxs-lookup"><span data-stu-id="dc197-115">-Property</span></span>
<span data-ttu-id="dc197-116">Задает список свойств в формате @ (property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="dc197-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="dc197-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="dc197-117">-ServiceUri</span></span>
<span data-ttu-id="dc197-118">Указывает URI службы.</span><span class="sxs-lookup"><span data-stu-id="dc197-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="dc197-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc197-119">CommonParameters</span></span>
<span data-ttu-id="dc197-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc197-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc197-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc197-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc197-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc197-122">INPUTS</span></span>

### <span data-ttu-id="dc197-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dc197-123">System.String</span></span>

### <span data-ttu-id="dc197-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dc197-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dc197-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc197-125">OUTPUTS</span></span>

### <span data-ttu-id="dc197-126">Microsoft. Azure. Management. Monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="dc197-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="dc197-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc197-127">NOTES</span></span>

## <span data-ttu-id="dc197-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc197-128">RELATED LINKS</span></span>

[<span data-ttu-id="dc197-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="dc197-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="dc197-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="dc197-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="dc197-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="dc197-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="dc197-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="dc197-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="dc197-133">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="dc197-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


