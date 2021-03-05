---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 22afc323e827c543150bffb317f1b5db5275d82c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979880"
---
# <span data-ttu-id="77fad-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="77fad-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="77fad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77fad-102">SYNOPSIS</span></span>
<span data-ttu-id="77fad-103">Создает правило оповещения webhook.</span><span class="sxs-lookup"><span data-stu-id="77fad-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="77fad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77fad-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77fad-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77fad-105">DESCRIPTION</span></span>
<span data-ttu-id="77fad-106">Для создания правила оповещения webhook будет создаваться **cmdlet New-AzAlertRuleWebhook.**</span><span class="sxs-lookup"><span data-stu-id="77fad-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="77fad-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77fad-107">EXAMPLES</span></span>

### <span data-ttu-id="77fad-108">Пример 1. Создание правила оповещения webhook</span><span class="sxs-lookup"><span data-stu-id="77fad-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="77fad-109">Эта команда создает правило оповещения webhook с указанием только URI службы.</span><span class="sxs-lookup"><span data-stu-id="77fad-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="77fad-110">Пример 2. Создание веб-приложения с одним свойством</span><span class="sxs-lookup"><span data-stu-id="77fad-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="77fad-111">Эта команда создает веб-сайт правила оповещения для Contoso.com с одним свойством, а затем сохраняет его в $Actual переменной.</span><span class="sxs-lookup"><span data-stu-id="77fad-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="77fad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77fad-112">PARAMETERS</span></span>

### <span data-ttu-id="77fad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fad-113">-DefaultProfile</span></span>
<span data-ttu-id="77fad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77fad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77fad-115">-Свойство</span><span class="sxs-lookup"><span data-stu-id="77fad-115">-Property</span></span>
<span data-ttu-id="77fad-116">Список свойств в формате @(свойство1 = 'значение1',....).</span><span class="sxs-lookup"><span data-stu-id="77fad-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="77fad-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="77fad-117">-ServiceUri</span></span>
<span data-ttu-id="77fad-118">Указывает URI службы.</span><span class="sxs-lookup"><span data-stu-id="77fad-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="77fad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fad-119">CommonParameters</span></span>
<span data-ttu-id="77fad-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77fad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fad-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77fad-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fad-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77fad-122">INPUTS</span></span>

### <span data-ttu-id="77fad-123">System.String</span><span class="sxs-lookup"><span data-stu-id="77fad-123">System.String</span></span>

### <span data-ttu-id="77fad-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="77fad-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="77fad-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77fad-125">OUTPUTS</span></span>

### <span data-ttu-id="77fad-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="77fad-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="77fad-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77fad-127">NOTES</span></span>

## <span data-ttu-id="77fad-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77fad-128">RELATED LINKS</span></span>

[<span data-ttu-id="77fad-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="77fad-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="77fad-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="77fad-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="77fad-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="77fad-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="77fad-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="77fad-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="77fad-133">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="77fad-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


