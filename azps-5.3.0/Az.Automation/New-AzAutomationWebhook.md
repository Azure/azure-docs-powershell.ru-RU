---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509957"
---
# <span data-ttu-id="e924a-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e924a-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="e924a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e924a-102">SYNOPSIS</span></span>
<span data-ttu-id="e924a-103">Создает веб-сайт для книги автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e924a-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="e924a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e924a-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e924a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e924a-105">DESCRIPTION</span></span>
<span data-ttu-id="e924a-106">**Из-за cmdlet New-AzAutomationWebhook** создается веб-ook для книги автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="e924a-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="e924a-107">Обязательно сохраните URL-адрес веб-приложения, который возвращает этот cmdlet, так как его нельзя будет восстановить снова.</span><span class="sxs-lookup"><span data-stu-id="e924a-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="e924a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e924a-108">EXAMPLES</span></span>

### <span data-ttu-id="e924a-109">Пример 1. Создание веб-приложения</span><span class="sxs-lookup"><span data-stu-id="e924a-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="e924a-110">Эта команда создает веб-сайт Webhook06 для книги с именем ContosoRunbook в учетной записи автоматизации AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="e924a-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="e924a-111">Команда сохраняет веб-сайт в переменной $Webhook.</span><span class="sxs-lookup"><span data-stu-id="e924a-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="e924a-112">Веб-сайт включен.</span><span class="sxs-lookup"><span data-stu-id="e924a-112">The webhook is enabled.</span></span>
<span data-ttu-id="e924a-113">Срок действия веб-приложения истекает в указанный срок.</span><span class="sxs-lookup"><span data-stu-id="e924a-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="e924a-114">Эта команда не дает значений для параметров webhook.</span><span class="sxs-lookup"><span data-stu-id="e924a-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="e924a-115">Эта команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="e924a-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e924a-116">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="e924a-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e924a-117">Пример 2. Создание веб-сайта с параметрами</span><span class="sxs-lookup"><span data-stu-id="e924a-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="e924a-118">Первая команда создает словарь параметров и сохраняет их в переменной $Params параметрами.</span><span class="sxs-lookup"><span data-stu-id="e924a-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="e924a-119">Вторая команда создает webhook с именем Webhook11 для книги ContosoRunbook в учетной записи автоматизации AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="e924a-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="e924a-120">Команда назначает параметры веб-$Params веб-сайту.</span><span class="sxs-lookup"><span data-stu-id="e924a-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="e924a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e924a-121">PARAMETERS</span></span>

### <span data-ttu-id="e924a-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e924a-122">-AutomationAccountName</span></span>
<span data-ttu-id="e924a-123">Указывает имя учетной записи автоматизации, в которой этот cmdlet создает веб-просмотр.</span><span class="sxs-lookup"><span data-stu-id="e924a-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="e924a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e924a-124">-DefaultProfile</span></span>
<span data-ttu-id="e924a-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e924a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e924a-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e924a-126">-ExpiryTime</span></span>
<span data-ttu-id="e924a-127">Время окончания срока действия для веб-приложения в качестве объекта **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="e924a-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="e924a-128">Вы можете указать строку или **дату и** время, которые можно преобразовать в допустимый **набор DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="e924a-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="e924a-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e924a-129">-Force</span></span>
<span data-ttu-id="e924a-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="e924a-130">ps_force</span></span>

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

### <span data-ttu-id="e924a-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e924a-131">-IsEnabled</span></span>
<span data-ttu-id="e924a-132">Указывает, включен ли веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="e924a-132">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="e924a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e924a-133">-Name</span></span>
<span data-ttu-id="e924a-134">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="e924a-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="e924a-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="e924a-135">-Parameters</span></span>
<span data-ttu-id="e924a-136">Словарь пар ключей и значений.</span><span class="sxs-lookup"><span data-stu-id="e924a-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="e924a-137">Ключами являются имена параметров книги запуска.</span><span class="sxs-lookup"><span data-stu-id="e924a-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="e924a-138">Значениями являются значения параметров книги запуска.</span><span class="sxs-lookup"><span data-stu-id="e924a-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="e924a-139">Когда запуск книги запускается с учетом веб-приложения WebHook, эти параметры передаются в книгу.</span><span class="sxs-lookup"><span data-stu-id="e924a-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="e924a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e924a-140">-ResourceGroupName</span></span>
<span data-ttu-id="e924a-141">Имя группы ресурсов, для которой этот cmdlet создает веб-просмотр.</span><span class="sxs-lookup"><span data-stu-id="e924a-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="e924a-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="e924a-142">-RunbookName</span></span>
<span data-ttu-id="e924a-143">Указывает имя книги, которая будет связываться с webhook.</span><span class="sxs-lookup"><span data-stu-id="e924a-143">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="e924a-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="e924a-144">-RunOn</span></span>
<span data-ttu-id="e924a-145">Необязательное имя гибридной группы рабочих, которая должна запустить книгу</span><span class="sxs-lookup"><span data-stu-id="e924a-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="e924a-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e924a-146">-Confirm</span></span>
<span data-ttu-id="e924a-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e924a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e924a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e924a-148">-WhatIf</span></span>
<span data-ttu-id="e924a-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e924a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e924a-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e924a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e924a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e924a-151">CommonParameters</span></span>
<span data-ttu-id="e924a-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e924a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e924a-153">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e924a-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e924a-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e924a-154">INPUTS</span></span>

### <span data-ttu-id="e924a-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e924a-155">System.String</span></span>

### <span data-ttu-id="e924a-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e924a-156">System.Boolean</span></span>

### <span data-ttu-id="e924a-157">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e924a-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="e924a-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e924a-158">OUTPUTS</span></span>

### <span data-ttu-id="e924a-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="e924a-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="e924a-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e924a-160">NOTES</span></span>

## <span data-ttu-id="e924a-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e924a-161">RELATED LINKS</span></span>

[<span data-ttu-id="e924a-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e924a-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="e924a-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e924a-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="e924a-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e924a-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


