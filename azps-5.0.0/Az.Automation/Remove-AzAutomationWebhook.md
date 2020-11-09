---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317309"
---
# <span data-ttu-id="7a0e2-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7a0e2-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="7a0e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a0e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0e2-103">Удаляет веб-перехватчик из модуля автоматизации Runbook.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="7a0e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a0e2-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a0e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a0e2-105">DESCRIPTION</span></span>
<span data-ttu-id="7a0e2-106">Командлет **Remove-AzAutomationWebhook** удаляет обработчик для Azure Automation Runbook.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="7a0e2-107">Веб-перехватчик удален.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-107">The webhook is deleted.</span></span>

## <span data-ttu-id="7a0e2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a0e2-108">EXAMPLES</span></span>

### <span data-ttu-id="7a0e2-109">Пример 1: удаление веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="7a0e2-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="7a0e2-110">Эта команда удаляет веб-перехватчик с именем Webhook11 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="7a0e2-111">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="7a0e2-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7a0e2-112">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7a0e2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a0e2-113">PARAMETERS</span></span>

### <span data-ttu-id="7a0e2-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a0e2-114">-AutomationAccountName</span></span>
<span data-ttu-id="7a0e2-115">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="7a0e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0e2-116">-DefaultProfile</span></span>
<span data-ttu-id="7a0e2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7a0e2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a0e2-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a0e2-118">-Name</span></span>
<span data-ttu-id="7a0e2-119">Указывает имя веб-перехватчика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a0e2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0e2-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a0e2-121">Указывает имя группы ресурсов, для которой этот командлет удаляет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="7a0e2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a0e2-122">-Confirm</span></span>
<span data-ttu-id="7a0e2-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0e2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0e2-124">-WhatIf</span></span>
<span data-ttu-id="7a0e2-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0e2-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0e2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0e2-127">CommonParameters</span></span>
<span data-ttu-id="7a0e2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a0e2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0e2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0e2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0e2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a0e2-130">INPUTS</span></span>

### <span data-ttu-id="7a0e2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7a0e2-131">System.String</span></span>

## <span data-ttu-id="7a0e2-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a0e2-132">OUTPUTS</span></span>

### <span data-ttu-id="7a0e2-133">System. void</span><span class="sxs-lookup"><span data-stu-id="7a0e2-133">System.Void</span></span>

## <span data-ttu-id="7a0e2-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a0e2-134">NOTES</span></span>

## <span data-ttu-id="7a0e2-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a0e2-135">RELATED LINKS</span></span>

[<span data-ttu-id="7a0e2-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7a0e2-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="7a0e2-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7a0e2-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="7a0e2-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7a0e2-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


