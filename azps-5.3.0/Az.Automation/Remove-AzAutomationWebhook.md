---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509881"
---
# <span data-ttu-id="1b14e-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1b14e-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="1b14e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b14e-102">SYNOPSIS</span></span>
<span data-ttu-id="1b14e-103">Удаляет веб-сайт из книги автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1b14e-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="1b14e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b14e-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b14e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b14e-105">DESCRIPTION</span></span>
<span data-ttu-id="1b14e-106">При **этом из книги автоматизации** Azure удаляется веб-ook.</span><span class="sxs-lookup"><span data-stu-id="1b14e-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="1b14e-107">Веб-сайт будет удален.</span><span class="sxs-lookup"><span data-stu-id="1b14e-107">The webhook is deleted.</span></span>

## <span data-ttu-id="1b14e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b14e-108">EXAMPLES</span></span>

### <span data-ttu-id="1b14e-109">Пример 1. Удаление веб-приложения</span><span class="sxs-lookup"><span data-stu-id="1b14e-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="1b14e-110">Эта команда удаляет веб-сайт Webhook11 из учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="1b14e-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="1b14e-111">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="1b14e-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1b14e-112">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="1b14e-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1b14e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b14e-113">PARAMETERS</span></span>

### <span data-ttu-id="1b14e-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1b14e-114">-AutomationAccountName</span></span>
<span data-ttu-id="1b14e-115">Указывает имя учетной записи автоматизации, из которой этот cmdlet удаляет webhook.</span><span class="sxs-lookup"><span data-stu-id="1b14e-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="1b14e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b14e-116">-DefaultProfile</span></span>
<span data-ttu-id="1b14e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1b14e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b14e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1b14e-118">-Name</span></span>
<span data-ttu-id="1b14e-119">Определяет имя веб-приложения, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b14e-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1b14e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b14e-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b14e-121">Имя группы ресурсов, для которой этот cmdlet удаляет webhook.</span><span class="sxs-lookup"><span data-stu-id="1b14e-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="1b14e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b14e-122">-Confirm</span></span>
<span data-ttu-id="1b14e-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1b14e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b14e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b14e-124">-WhatIf</span></span>
<span data-ttu-id="1b14e-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b14e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b14e-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1b14e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b14e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b14e-127">CommonParameters</span></span>
<span data-ttu-id="1b14e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b14e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b14e-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b14e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b14e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b14e-130">INPUTS</span></span>

### <span data-ttu-id="1b14e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1b14e-131">System.String</span></span>

## <span data-ttu-id="1b14e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b14e-132">OUTPUTS</span></span>

### <span data-ttu-id="1b14e-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="1b14e-133">System.Void</span></span>

## <span data-ttu-id="1b14e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b14e-134">NOTES</span></span>

## <span data-ttu-id="1b14e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b14e-135">RELATED LINKS</span></span>

[<span data-ttu-id="1b14e-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1b14e-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="1b14e-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1b14e-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="1b14e-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1b14e-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


