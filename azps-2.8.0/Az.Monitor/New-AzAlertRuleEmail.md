---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: e7ba5bc42e08ce73fcfac5fcbb7ea614a43f2b3e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397889"
---
# <span data-ttu-id="b3674-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="b3674-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="b3674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3674-102">SYNOPSIS</span></span>
<span data-ttu-id="b3674-103">Создает действие по электронной почте для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b3674-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="b3674-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3674-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3674-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3674-105">DESCRIPTION</span></span>
<span data-ttu-id="b3674-106">Для правила оповещения создается действие **"New-AzAlertRuleEmail".**</span><span class="sxs-lookup"><span data-stu-id="b3674-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="b3674-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3674-107">EXAMPLES</span></span>

### <span data-ttu-id="b3674-108">Пример 1. Создание действия правила оповещения для владельцев служб</span><span class="sxs-lookup"><span data-stu-id="b3674-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="b3674-109">Эта команда создает действие правила оповещения, которое отправляется владельцам служб при его отправке.</span><span class="sxs-lookup"><span data-stu-id="b3674-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="b3674-110">Пример 2. Создание действия правила оповещения для владельцев, не внося в службу</span><span class="sxs-lookup"><span data-stu-id="b3674-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="b3674-111">Эта команда создает действие правила оповещения для указанных адресов электронной почты, но не для владельцев служб.</span><span class="sxs-lookup"><span data-stu-id="b3674-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="b3674-112">Пример 3. Создание действия правила оповещения для владельцев служб и других владельцев</span><span class="sxs-lookup"><span data-stu-id="b3674-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="b3674-113">Эта команда создает действие правила оповещения для указанного адреса и для его владельцев служб.</span><span class="sxs-lookup"><span data-stu-id="b3674-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="b3674-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3674-114">PARAMETERS</span></span>

### <span data-ttu-id="b3674-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="b3674-115">-CustomEmail</span></span>
<span data-ttu-id="b3674-116">Список адресов электронной почты, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="b3674-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="b3674-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3674-117">-DefaultProfile</span></span>
<span data-ttu-id="b3674-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b3674-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3674-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="b3674-119">-SendToServiceOwner</span></span>
<span data-ttu-id="b3674-120">Указывает на то, что при отправке правила владельцам службы отправляется сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b3674-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="b3674-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3674-121">CommonParameters</span></span>
<span data-ttu-id="b3674-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3674-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3674-123">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3674-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3674-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3674-124">INPUTS</span></span>

### <span data-ttu-id="b3674-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b3674-125">System.String[]</span></span>

### <span data-ttu-id="b3674-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3674-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3674-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3674-127">OUTPUTS</span></span>

### <span data-ttu-id="b3674-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="b3674-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="b3674-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3674-129">NOTES</span></span>

## <span data-ttu-id="b3674-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3674-130">RELATED LINKS</span></span>


[<span data-ttu-id="b3674-131">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3674-131">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="b3674-132">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3674-132">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="b3674-133">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="b3674-133">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


