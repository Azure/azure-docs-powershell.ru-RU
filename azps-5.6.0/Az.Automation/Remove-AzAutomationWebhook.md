---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 93c370eaefa83c5e1be4692cb41ea0793b8f4681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009843"
---
# <span data-ttu-id="a7164-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a7164-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="a7164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7164-102">SYNOPSIS</span></span>
<span data-ttu-id="a7164-103">Удаляет веб-сайт из книги автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a7164-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="a7164-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7164-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7164-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7164-105">DESCRIPTION</span></span>
<span data-ttu-id="a7164-106">При **этом из книги автоматизации** Azure удаляется веб-ook.</span><span class="sxs-lookup"><span data-stu-id="a7164-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="a7164-107">Веб-сайт будет удален.</span><span class="sxs-lookup"><span data-stu-id="a7164-107">The webhook is deleted.</span></span>

## <span data-ttu-id="a7164-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7164-108">EXAMPLES</span></span>

### <span data-ttu-id="a7164-109">Пример 1. Удаление веб-приложения</span><span class="sxs-lookup"><span data-stu-id="a7164-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="a7164-110">Эта команда удаляет веб-сайт Webhook11 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a7164-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a7164-111">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="a7164-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a7164-112">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="a7164-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a7164-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7164-113">PARAMETERS</span></span>

### <span data-ttu-id="a7164-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a7164-114">-AutomationAccountName</span></span>
<span data-ttu-id="a7164-115">Указывает имя учетной записи автоматизации, из которой этот cmdlet удаляет webhook.</span><span class="sxs-lookup"><span data-stu-id="a7164-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7164-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7164-116">-DefaultProfile</span></span>
<span data-ttu-id="a7164-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a7164-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7164-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a7164-118">-Name</span></span>
<span data-ttu-id="a7164-119">Указывает имя веб-приложения, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7164-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7164-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7164-120">-ResourceGroupName</span></span>
<span data-ttu-id="a7164-121">Имя группы ресурсов, для которой этот cmdlet удаляет webhook.</span><span class="sxs-lookup"><span data-stu-id="a7164-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="a7164-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7164-122">-Confirm</span></span>
<span data-ttu-id="a7164-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a7164-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7164-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7164-124">-WhatIf</span></span>
<span data-ttu-id="a7164-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7164-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7164-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7164-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7164-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7164-127">CommonParameters</span></span>
<span data-ttu-id="a7164-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7164-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7164-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7164-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7164-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7164-130">INPUTS</span></span>

### <span data-ttu-id="a7164-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a7164-131">System.String</span></span>

## <span data-ttu-id="a7164-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7164-132">OUTPUTS</span></span>

### <span data-ttu-id="a7164-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="a7164-133">System.Void</span></span>

## <span data-ttu-id="a7164-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7164-134">NOTES</span></span>

## <span data-ttu-id="a7164-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7164-135">RELATED LINKS</span></span>

[<span data-ttu-id="a7164-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a7164-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="a7164-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a7164-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="a7164-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a7164-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


