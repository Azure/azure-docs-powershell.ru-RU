---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: f1062f1e827e27ff891f5b2797fcda95e60f3427
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566331"
---
# <span data-ttu-id="35611-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="35611-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="35611-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35611-102">SYNOPSIS</span></span>
<span data-ttu-id="35611-103">Создает веб-перехватчик для модуля автоматизации Runbook.</span><span class="sxs-lookup"><span data-stu-id="35611-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35611-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35611-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35611-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35611-105">DESCRIPTION</span></span>
<span data-ttu-id="35611-106">Командлет **New-AzureRmAutomationWebhook** создает интерфейс для Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="35611-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="35611-107">Не забудьте сохранить URL-адрес веб-перехватчика, возвращаемый этим командлетом, так как он не может быть извлечен еще раз.</span><span class="sxs-lookup"><span data-stu-id="35611-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="35611-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35611-108">EXAMPLES</span></span>

### <span data-ttu-id="35611-109">Пример 1: создание веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="35611-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="35611-110">Эта команда создает веб-перехватчик с именем Webhook06 для модуля Runbook с именем ContosoRunbook в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="35611-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="35611-111">Команда сохраняет веб-перехватчик в переменной $Webhook.</span><span class="sxs-lookup"><span data-stu-id="35611-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="35611-112">Веб-перехватчик включен.</span><span class="sxs-lookup"><span data-stu-id="35611-112">The webhook is enabled.</span></span>
<span data-ttu-id="35611-113">Веб-перехватчик истекает в указанное время.</span><span class="sxs-lookup"><span data-stu-id="35611-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="35611-114">Эта команда не предоставляет никаких значений для параметров веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="35611-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="35611-115">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="35611-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="35611-116">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="35611-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="35611-117">Пример 2: создание веб-перехватчика с параметрами</span><span class="sxs-lookup"><span data-stu-id="35611-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="35611-118">Первая команда создает словарь параметров и сохраняет их в переменной $Params.</span><span class="sxs-lookup"><span data-stu-id="35611-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="35611-119">Вторая команда создает веб-перехватчик с именем Webhook11 для модуля Runbook с именем ContosoRunbook в учетной записи автоматизации под названием AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="35611-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="35611-120">Команда назначает параметры в $Params веб-перехватчику.</span><span class="sxs-lookup"><span data-stu-id="35611-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="35611-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35611-121">PARAMETERS</span></span>

### <span data-ttu-id="35611-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="35611-122">-AutomationAccountName</span></span>
<span data-ttu-id="35611-123">Указывает имя учетной записи автоматизации, в которой этот командлет создает веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="35611-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="35611-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="35611-124">-ExpiryTime</span></span>
<span data-ttu-id="35611-125">Задает время истечения срока действия веб-перехватчика в качестве объекта **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="35611-125">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="35611-126">Вы можете указать строку или **значение даты и времени** , которое можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="35611-126">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="35611-127">-Force</span><span class="sxs-lookup"><span data-stu-id="35611-127">-Force</span></span>
<span data-ttu-id="35611-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="35611-128">ps_force</span></span>

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

### <span data-ttu-id="35611-129">-Включено</span><span class="sxs-lookup"><span data-stu-id="35611-129">-IsEnabled</span></span>
<span data-ttu-id="35611-130">Указывает, включен ли веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="35611-130">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="35611-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35611-131">-Name</span></span>
<span data-ttu-id="35611-132">Задает имя веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="35611-132">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="35611-133">-Parameters</span><span class="sxs-lookup"><span data-stu-id="35611-133">-Parameters</span></span>
<span data-ttu-id="35611-134">Указывает словарь пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="35611-134">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="35611-135">Ключи — это имена параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="35611-135">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="35611-136">Значения — это значения параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="35611-136">The values are the runbook parameter values.</span></span>
<span data-ttu-id="35611-137">При запуске модуля Runbook в ответ на веб-перехватчик эти параметры передаются в модуль Runbook.</span><span class="sxs-lookup"><span data-stu-id="35611-137">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="35611-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35611-138">-ResourceGroupName</span></span>
<span data-ttu-id="35611-139">Указывает имя группы ресурсов, для которой этот командлет создает веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="35611-139">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="35611-140">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="35611-140">-RunbookName</span></span>
<span data-ttu-id="35611-141">Указывает имя модуля Runbook, который нужно связать с веб-перехватчиком.</span><span class="sxs-lookup"><span data-stu-id="35611-141">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="35611-142">-RunOn</span><span class="sxs-lookup"><span data-stu-id="35611-142">-RunOn</span></span>
<span data-ttu-id="35611-143">Необязательное имя гибридного агента, который должен выполнить Runbook.</span><span class="sxs-lookup"><span data-stu-id="35611-143">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="35611-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35611-144">-Confirm</span></span>
<span data-ttu-id="35611-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35611-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35611-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35611-146">-WhatIf</span></span>
<span data-ttu-id="35611-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35611-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35611-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35611-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35611-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35611-149">-DefaultProfile</span></span>
<span data-ttu-id="35611-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35611-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35611-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35611-151">CommonParameters</span></span>
<span data-ttu-id="35611-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35611-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35611-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35611-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35611-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35611-154">INPUTS</span></span>

## <span data-ttu-id="35611-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35611-155">OUTPUTS</span></span>

### <span data-ttu-id="35611-156">Microsoft. Azure. Commands. Automation. Model. веб-перехватчик</span><span class="sxs-lookup"><span data-stu-id="35611-156">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="35611-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="35611-157">NOTES</span></span>

## <span data-ttu-id="35611-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35611-158">RELATED LINKS</span></span>

[<span data-ttu-id="35611-159">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="35611-159">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="35611-160">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="35611-160">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="35611-161">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="35611-161">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


