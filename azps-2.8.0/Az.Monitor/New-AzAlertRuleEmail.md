---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 30447992cd8159f56ae08d6cb2baf659c9ed7bb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902653"
---
# <span data-ttu-id="c0375-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="c0375-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="c0375-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0375-102">SYNOPSIS</span></span>
<span data-ttu-id="c0375-103">Создание действия электронной почты для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="c0375-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="c0375-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0375-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0375-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0375-105">DESCRIPTION</span></span>
<span data-ttu-id="c0375-106">Командлет **New-AzAlertRuleEmail** создает действие электронной почты для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="c0375-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="c0375-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0375-107">EXAMPLES</span></span>

### <span data-ttu-id="c0375-108">Пример 1: Создание действия по электронной почте правила оповещения для владельцев служб</span><span class="sxs-lookup"><span data-stu-id="c0375-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="c0375-109">Эта команда создает действие по электронной почте правила оповещения, которое отправляется своим владельцам услуг при срабатывании правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="c0375-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="c0375-110">Пример 2: Создание действия по электронной почте для правила оповещения для владельцев, не связанных с обслуживанием</span><span class="sxs-lookup"><span data-stu-id="c0375-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="c0375-111">Эта команда создает действие по электронной почте правила оповещения для указанных адресов электронной почты, но не для владельцев служб.</span><span class="sxs-lookup"><span data-stu-id="c0375-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="c0375-112">Пример 3: Создание действия по электронной почте правила оповещения для владельцев услуг и не владельцев служб</span><span class="sxs-lookup"><span data-stu-id="c0375-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="c0375-113">Эта команда создает действие по электронной почте правила оповещения для указанного адреса и для владельцев служб.</span><span class="sxs-lookup"><span data-stu-id="c0375-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="c0375-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0375-114">PARAMETERS</span></span>

### <span data-ttu-id="c0375-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="c0375-115">-CustomEmail</span></span>
<span data-ttu-id="c0375-116">Задает список адресов электронной почты, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="c0375-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0375-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0375-117">-DefaultProfile</span></span>
<span data-ttu-id="c0375-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c0375-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0375-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="c0375-119">-SendToServiceOwner</span></span>
<span data-ttu-id="c0375-120">Указывает, что эта операция отправляет владельцам службы сообщение электронной почты при срабатывании правила.</span><span class="sxs-lookup"><span data-stu-id="c0375-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0375-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0375-121">CommonParameters</span></span>
<span data-ttu-id="c0375-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0375-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0375-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0375-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0375-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0375-124">INPUTS</span></span>

### <span data-ttu-id="c0375-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="c0375-125">System.String[]</span></span>

### <span data-ttu-id="c0375-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c0375-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c0375-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0375-127">OUTPUTS</span></span>

### <span data-ttu-id="c0375-128">Microsoft. Azure. Management. Monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="c0375-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="c0375-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0375-129">NOTES</span></span>

## <span data-ttu-id="c0375-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0375-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0375-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="c0375-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="c0375-132">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c0375-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="c0375-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c0375-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="c0375-134">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c0375-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


