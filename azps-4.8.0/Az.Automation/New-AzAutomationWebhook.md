---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235107"
---
# <span data-ttu-id="698f1-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="698f1-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="698f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="698f1-102">SYNOPSIS</span></span>
<span data-ttu-id="698f1-103">Создает веб-перехватчик для модуля автоматизации Runbook.</span><span class="sxs-lookup"><span data-stu-id="698f1-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="698f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="698f1-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="698f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="698f1-105">DESCRIPTION</span></span>
<span data-ttu-id="698f1-106">Командлет **New-AzAutomationWebhook** создает интерфейс для Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="698f1-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="698f1-107">Не забудьте сохранить URL-адрес веб-перехватчика, возвращаемый этим командлетом, так как он не может быть извлечен еще раз.</span><span class="sxs-lookup"><span data-stu-id="698f1-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="698f1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="698f1-108">EXAMPLES</span></span>

### <span data-ttu-id="698f1-109">Пример 1: создание веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="698f1-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="698f1-110">Эта команда создает веб-перехватчик с именем Webhook06 для модуля Runbook с именем ContosoRunbook в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="698f1-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="698f1-111">Команда сохраняет веб-перехватчик в переменной $Webhook.</span><span class="sxs-lookup"><span data-stu-id="698f1-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="698f1-112">Веб-перехватчик включен.</span><span class="sxs-lookup"><span data-stu-id="698f1-112">The webhook is enabled.</span></span>
<span data-ttu-id="698f1-113">Веб-перехватчик истекает в указанное время.</span><span class="sxs-lookup"><span data-stu-id="698f1-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="698f1-114">Эта команда не предоставляет никаких значений для параметров веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="698f1-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="698f1-115">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="698f1-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="698f1-116">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="698f1-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="698f1-117">Пример 2: создание веб-перехватчика с параметрами</span><span class="sxs-lookup"><span data-stu-id="698f1-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="698f1-118">Первая команда создает словарь параметров и сохраняет их в переменной $Params.</span><span class="sxs-lookup"><span data-stu-id="698f1-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="698f1-119">Вторая команда создает веб-перехватчик с именем Webhook11 для модуля Runbook с именем ContosoRunbook в учетной записи автоматизации под названием AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="698f1-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="698f1-120">Команда назначает параметры в $Params веб-перехватчику.</span><span class="sxs-lookup"><span data-stu-id="698f1-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="698f1-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="698f1-121">PARAMETERS</span></span>

### <span data-ttu-id="698f1-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="698f1-122">-AutomationAccountName</span></span>
<span data-ttu-id="698f1-123">Указывает имя учетной записи автоматизации, в которой этот командлет создает веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="698f1-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="698f1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698f1-124">-DefaultProfile</span></span>
<span data-ttu-id="698f1-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="698f1-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="698f1-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="698f1-126">-ExpiryTime</span></span>
<span data-ttu-id="698f1-127">Задает время истечения срока действия веб-перехватчика в качестве объекта **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="698f1-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="698f1-128">Вы можете указать строку или **значение даты и времени** , которое можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="698f1-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698f1-129">-Force</span><span class="sxs-lookup"><span data-stu-id="698f1-129">-Force</span></span>
<span data-ttu-id="698f1-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="698f1-130">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698f1-131">-Включено</span><span class="sxs-lookup"><span data-stu-id="698f1-131">-IsEnabled</span></span>
<span data-ttu-id="698f1-132">Указывает, включен ли веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="698f1-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698f1-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="698f1-133">-Name</span></span>
<span data-ttu-id="698f1-134">Задает имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="698f1-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="698f1-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="698f1-135">-Parameters</span></span>
<span data-ttu-id="698f1-136">Указывает словарь пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="698f1-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="698f1-137">Ключи — это имена параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="698f1-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="698f1-138">Значения — это значения параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="698f1-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="698f1-139">При запуске модуля Runbook в ответ на веб-перехватчик эти параметры передаются в модуль Runbook.</span><span class="sxs-lookup"><span data-stu-id="698f1-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698f1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="698f1-140">-ResourceGroupName</span></span>
<span data-ttu-id="698f1-141">Указывает имя группы ресурсов, для которой этот командлет создает веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="698f1-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="698f1-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="698f1-142">-RunbookName</span></span>
<span data-ttu-id="698f1-143">Указывает имя модуля Runbook, который нужно связать с веб-перехватчиком.</span><span class="sxs-lookup"><span data-stu-id="698f1-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698f1-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="698f1-144">-RunOn</span></span>
<span data-ttu-id="698f1-145">Необязательное имя группы гибридного рабочего процесса, которое должно выполнять Runbook</span><span class="sxs-lookup"><span data-stu-id="698f1-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="698f1-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="698f1-146">-Confirm</span></span>
<span data-ttu-id="698f1-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="698f1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="698f1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="698f1-148">-WhatIf</span></span>
<span data-ttu-id="698f1-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="698f1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="698f1-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="698f1-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="698f1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698f1-151">CommonParameters</span></span>
<span data-ttu-id="698f1-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="698f1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698f1-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="698f1-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698f1-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="698f1-154">INPUTS</span></span>

### <span data-ttu-id="698f1-155">System. String</span><span class="sxs-lookup"><span data-stu-id="698f1-155">System.String</span></span>

### <span data-ttu-id="698f1-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="698f1-156">System.Boolean</span></span>

### <span data-ttu-id="698f1-157">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="698f1-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="698f1-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="698f1-158">OUTPUTS</span></span>

### <span data-ttu-id="698f1-159">Microsoft. Azure. Commands. Automation. Model. веб-перехватчик</span><span class="sxs-lookup"><span data-stu-id="698f1-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="698f1-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="698f1-160">NOTES</span></span>

## <span data-ttu-id="698f1-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="698f1-161">RELATED LINKS</span></span>

[<span data-ttu-id="698f1-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="698f1-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="698f1-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="698f1-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="698f1-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="698f1-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


