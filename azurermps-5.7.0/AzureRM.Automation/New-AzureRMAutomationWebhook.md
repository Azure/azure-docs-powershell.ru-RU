---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: 417ab3f7f787a76041caceebbfcf32f9733717b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569068"
---
# <span data-ttu-id="d3872-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d3872-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="d3872-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3872-102">SYNOPSIS</span></span>
<span data-ttu-id="d3872-103">Создает веб-перехватчик для модуля автоматизации Runbook.</span><span class="sxs-lookup"><span data-stu-id="d3872-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3872-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3872-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3872-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3872-105">DESCRIPTION</span></span>
<span data-ttu-id="d3872-106">Командлет **New-AzureRmAutomationWebhook** создает интерфейс для Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d3872-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="d3872-107">Не забудьте сохранить URL-адрес веб-перехватчика, возвращаемый этим командлетом, так как он не может быть извлечен еще раз.</span><span class="sxs-lookup"><span data-stu-id="d3872-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="d3872-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3872-108">EXAMPLES</span></span>

### <span data-ttu-id="d3872-109">Пример 1: создание веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="d3872-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="d3872-110">Эта команда создает веб-перехватчик с именем Webhook06 для модуля Runbook с именем ContosoRunbook в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="d3872-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="d3872-111">Команда сохраняет веб-перехватчик в переменной $Webhook.</span><span class="sxs-lookup"><span data-stu-id="d3872-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="d3872-112">Веб-перехватчик включен.</span><span class="sxs-lookup"><span data-stu-id="d3872-112">The webhook is enabled.</span></span>
<span data-ttu-id="d3872-113">Веб-перехватчик истекает в указанное время.</span><span class="sxs-lookup"><span data-stu-id="d3872-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="d3872-114">Эта команда не предоставляет никаких значений для параметров веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="d3872-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="d3872-115">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="d3872-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d3872-116">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d3872-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="d3872-117">Пример 2: создание веб-перехватчика с параметрами</span><span class="sxs-lookup"><span data-stu-id="d3872-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="d3872-118">Первая команда создает словарь параметров и сохраняет их в переменной $Params.</span><span class="sxs-lookup"><span data-stu-id="d3872-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="d3872-119">Вторая команда создает веб-перехватчик с именем Webhook11 для модуля Runbook с именем ContosoRunbook в учетной записи автоматизации под названием AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="d3872-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="d3872-120">Команда назначает параметры в $Params веб-перехватчику.</span><span class="sxs-lookup"><span data-stu-id="d3872-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="d3872-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3872-121">PARAMETERS</span></span>

### <span data-ttu-id="d3872-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d3872-122">-AutomationAccountName</span></span>
<span data-ttu-id="d3872-123">Указывает имя учетной записи автоматизации, в которой этот командлет создает веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="d3872-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3872-124">-DefaultProfile</span></span>
<span data-ttu-id="d3872-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d3872-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d3872-126">-ExpiryTime</span></span>
<span data-ttu-id="d3872-127">Задает время истечения срока действия веб-перехватчика в качестве объекта **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="d3872-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="d3872-128">Вы можете указать строку или **значение даты и времени** , которое можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="d3872-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-129">-Force</span><span class="sxs-lookup"><span data-stu-id="d3872-129">-Force</span></span>
<span data-ttu-id="d3872-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="d3872-130">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-131">-Включено</span><span class="sxs-lookup"><span data-stu-id="d3872-131">-IsEnabled</span></span>
<span data-ttu-id="d3872-132">Указывает, включен ли веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="d3872-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3872-133">-Name</span></span>
<span data-ttu-id="d3872-134">Задает имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="d3872-134">Specifies a name for the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="d3872-135">-Parameters</span></span>
<span data-ttu-id="d3872-136">Указывает словарь пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="d3872-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="d3872-137">Ключи — это имена параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="d3872-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="d3872-138">Значения — это значения параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="d3872-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="d3872-139">При запуске модуля Runbook в ответ на веб-перехватчик эти параметры передаются в модуль Runbook.</span><span class="sxs-lookup"><span data-stu-id="d3872-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3872-140">-ResourceGroupName</span></span>
<span data-ttu-id="d3872-141">Указывает имя группы ресурсов, для которой этот командлет создает веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="d3872-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="d3872-142">-RunbookName</span></span>
<span data-ttu-id="d3872-143">Указывает имя модуля Runbook, который нужно связать с веб-перехватчиком.</span><span class="sxs-lookup"><span data-stu-id="d3872-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="d3872-144">-RunOn</span></span>
<span data-ttu-id="d3872-145">Необязательное имя группы гибридного рабочего процесса, которое должно выполнять Runbook</span><span class="sxs-lookup"><span data-stu-id="d3872-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3872-146">-Confirm</span></span>
<span data-ttu-id="d3872-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d3872-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3872-148">-WhatIf</span></span>
<span data-ttu-id="d3872-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d3872-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3872-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d3872-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3872-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3872-151">CommonParameters</span></span>
<span data-ttu-id="d3872-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3872-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3872-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3872-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3872-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3872-154">INPUTS</span></span>

### <span data-ttu-id="d3872-155">Ничего</span><span class="sxs-lookup"><span data-stu-id="d3872-155">None</span></span>
<span data-ttu-id="d3872-156">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d3872-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3872-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3872-157">OUTPUTS</span></span>

### <span data-ttu-id="d3872-158">Microsoft. Azure. Commands. Automation. Model. веб-перехватчик</span><span class="sxs-lookup"><span data-stu-id="d3872-158">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="d3872-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3872-159">NOTES</span></span>

## <span data-ttu-id="d3872-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3872-160">RELATED LINKS</span></span>

[<span data-ttu-id="d3872-161">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d3872-161">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="d3872-162">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d3872-162">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="d3872-163">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d3872-163">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


