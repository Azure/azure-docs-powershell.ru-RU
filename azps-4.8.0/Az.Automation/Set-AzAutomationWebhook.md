---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243720"
---
# <span data-ttu-id="5aa48-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5aa48-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="5aa48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5aa48-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa48-103">Изменяет веб-перехватчик для модуля автоматизации Runbook.</span><span class="sxs-lookup"><span data-stu-id="5aa48-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="5aa48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5aa48-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5aa48-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aa48-105">DESCRIPTION</span></span>
<span data-ttu-id="5aa48-106">Командлет **Set-AzAutomationWebhook** изменяет интерфейс для Azure Automation Runbook.</span><span class="sxs-lookup"><span data-stu-id="5aa48-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="5aa48-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5aa48-107">EXAMPLES</span></span>

### <span data-ttu-id="5aa48-108">Пример 1: Отключение веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="5aa48-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="5aa48-109">Эта команда отключает веб-перехватчик с именем Webhook01 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="5aa48-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="5aa48-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5aa48-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="5aa48-111">Эта команда задает значение Run on для веб-перехватчика и принудительное выполнение модуля Runbook на группе гибридного рабочего процесса под названием Windows.</span><span class="sxs-lookup"><span data-stu-id="5aa48-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="5aa48-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5aa48-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="5aa48-113">Эта команда обновляет значение Run on для веб-перехватчика и принудительно запускает Runbook для исполнителя Azure Runbook.</span><span class="sxs-lookup"><span data-stu-id="5aa48-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="5aa48-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5aa48-114">PARAMETERS</span></span>

### <span data-ttu-id="5aa48-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5aa48-115">-AutomationAccountName</span></span>
<span data-ttu-id="5aa48-116">Указывает имя учетной записи автоматизации, в которой этот командлет изменяет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="5aa48-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="5aa48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa48-117">-DefaultProfile</span></span>
<span data-ttu-id="5aa48-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5aa48-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aa48-119">-Включено</span><span class="sxs-lookup"><span data-stu-id="5aa48-119">-IsEnabled</span></span>
<span data-ttu-id="5aa48-120">Указывает, включен ли веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="5aa48-120">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aa48-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5aa48-121">-Name</span></span>
<span data-ttu-id="5aa48-122">Указывает имя веб-перехватчика, измененного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5aa48-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5aa48-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="5aa48-123">-Parameters</span></span>
<span data-ttu-id="5aa48-124">Указывает словарь пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="5aa48-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="5aa48-125">Ключи — это имена параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="5aa48-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="5aa48-126">Значения — это значения параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="5aa48-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="5aa48-127">При запуске модуля Runbook в ответ на веб-перехватчик эти параметры передаются в модуль Runbook.</span><span class="sxs-lookup"><span data-stu-id="5aa48-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aa48-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa48-128">-ResourceGroupName</span></span>
<span data-ttu-id="5aa48-129">Указывает имя группы ресурсов, для которой этот командлет изменяет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="5aa48-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="5aa48-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="5aa48-130">-RunOn</span></span>
<span data-ttu-id="5aa48-131">Необязательное имя гибридного агента, который должен выполнить Runbook.</span><span class="sxs-lookup"><span data-stu-id="5aa48-131">Optional name of the hybrid agent which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa48-132">CommonParameters</span></span>
<span data-ttu-id="5aa48-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5aa48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa48-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5aa48-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa48-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5aa48-135">INPUTS</span></span>

### <span data-ttu-id="5aa48-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5aa48-136">System.String</span></span>

### <span data-ttu-id="5aa48-137">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5aa48-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5aa48-138">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="5aa48-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="5aa48-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aa48-139">OUTPUTS</span></span>

### <span data-ttu-id="5aa48-140">Microsoft. Azure. Commands. Automation. Model. веб-перехватчик</span><span class="sxs-lookup"><span data-stu-id="5aa48-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="5aa48-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="5aa48-141">NOTES</span></span>

## <span data-ttu-id="5aa48-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5aa48-142">RELATED LINKS</span></span>

[<span data-ttu-id="5aa48-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5aa48-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="5aa48-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5aa48-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="5aa48-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5aa48-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


