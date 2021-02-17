---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 237742c633ffe7a2a113467c7a12725b4f3b8b89
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403074"
---
# <span data-ttu-id="d3a7c-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="d3a7c-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="d3a7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a7c-103">Создает правило оповещения webhook.</span><span class="sxs-lookup"><span data-stu-id="d3a7c-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="d3a7c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3a7c-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3a7c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3a7c-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a7c-106">Для создания правила оповещения webhook будет создаваться **cmdlet New-AzAlertRuleWebhook.**</span><span class="sxs-lookup"><span data-stu-id="d3a7c-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="d3a7c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3a7c-107">EXAMPLES</span></span>

### <span data-ttu-id="d3a7c-108">Пример 1. Создание веб-приложения "Правило оповещения"</span><span class="sxs-lookup"><span data-stu-id="d3a7c-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="d3a7c-109">Эта команда создает правило оповещения с указанием только URI службы.</span><span class="sxs-lookup"><span data-stu-id="d3a7c-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="d3a7c-110">Пример 2. Создание веб-сайта с одним свойством</span><span class="sxs-lookup"><span data-stu-id="d3a7c-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="d3a7c-111">Эта команда создает веб-сайт правила оповещения для Contoso.com с одним свойством, а затем сохраняет его в $Actual переменной.</span><span class="sxs-lookup"><span data-stu-id="d3a7c-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="d3a7c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a7c-112">PARAMETERS</span></span>

### <span data-ttu-id="d3a7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a7c-113">-DefaultProfile</span></span>
<span data-ttu-id="d3a7c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d3a7c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3a7c-115">-Свойство</span><span class="sxs-lookup"><span data-stu-id="d3a7c-115">-Property</span></span>
<span data-ttu-id="d3a7c-116">Список свойств в формате @(свойство1 = 'значение1',....).</span><span class="sxs-lookup"><span data-stu-id="d3a7c-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="d3a7c-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="d3a7c-117">-ServiceUri</span></span>
<span data-ttu-id="d3a7c-118">Указывает URI службы.</span><span class="sxs-lookup"><span data-stu-id="d3a7c-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="d3a7c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a7c-119">CommonParameters</span></span>
<span data-ttu-id="d3a7c-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a7c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a7c-121">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a7c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a7c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a7c-122">INPUTS</span></span>

### <span data-ttu-id="d3a7c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d3a7c-123">System.String</span></span>

### <span data-ttu-id="d3a7c-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d3a7c-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d3a7c-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a7c-125">OUTPUTS</span></span>

### <span data-ttu-id="d3a7c-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="d3a7c-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="d3a7c-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3a7c-127">NOTES</span></span>

## <span data-ttu-id="d3a7c-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3a7c-128">RELATED LINKS</span></span>


[<span data-ttu-id="d3a7c-129">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d3a7c-129">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="d3a7c-130">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d3a7c-130">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="d3a7c-131">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="d3a7c-131">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="d3a7c-132">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="d3a7c-132">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


