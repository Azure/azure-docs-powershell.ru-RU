---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418207"
---
# <span data-ttu-id="df0fa-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="df0fa-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="df0fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="df0fa-103">Изменяет webhook для книги автоматизации.</span><span class="sxs-lookup"><span data-stu-id="df0fa-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="df0fa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="df0fa-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df0fa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df0fa-105">DESCRIPTION</span></span>
<span data-ttu-id="df0fa-106">**Cmdlet Set-AzAutomationWebhook** изменяет webhook для книги автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="df0fa-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="df0fa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="df0fa-107">EXAMPLES</span></span>

### <span data-ttu-id="df0fa-108">Пример 1. Отключение веб-приложения</span><span class="sxs-lookup"><span data-stu-id="df0fa-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="df0fa-109">Эта команда отключает веб-сайт Webhook01 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="df0fa-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="df0fa-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df0fa-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="df0fa-111">Эта команда задает значение запуска веб-приложения и отправляет запуск книги в группу гибридных рабочих под названием Windows.</span><span class="sxs-lookup"><span data-stu-id="df0fa-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="df0fa-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="df0fa-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="df0fa-113">Эта команда обновляет значение, заданное для webhook, и принудит запуск книги к сотруднику книги Azure.</span><span class="sxs-lookup"><span data-stu-id="df0fa-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="df0fa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df0fa-114">PARAMETERS</span></span>

### <span data-ttu-id="df0fa-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df0fa-115">-AutomationAccountName</span></span>
<span data-ttu-id="df0fa-116">Указывает имя учетной записи автоматизации, в которой этот cmdlet изменяет webhook.</span><span class="sxs-lookup"><span data-stu-id="df0fa-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="df0fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df0fa-117">-DefaultProfile</span></span>
<span data-ttu-id="df0fa-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="df0fa-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df0fa-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="df0fa-119">-IsEnabled</span></span>
<span data-ttu-id="df0fa-120">Указывает, включен ли веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="df0fa-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="df0fa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="df0fa-121">-Name</span></span>
<span data-ttu-id="df0fa-122">Указывает имя веб-приложения, которое изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df0fa-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="df0fa-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="df0fa-123">-Parameters</span></span>
<span data-ttu-id="df0fa-124">Словарь пар ключей и значений.</span><span class="sxs-lookup"><span data-stu-id="df0fa-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="df0fa-125">Ключами являются имена параметров книги запуска.</span><span class="sxs-lookup"><span data-stu-id="df0fa-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="df0fa-126">Значениями являются значения параметров книги запуска.</span><span class="sxs-lookup"><span data-stu-id="df0fa-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="df0fa-127">Когда запуск книги запускается с учетом веб-приложения WebHook, эти параметры передаются в книгу.</span><span class="sxs-lookup"><span data-stu-id="df0fa-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="df0fa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df0fa-128">-ResourceGroupName</span></span>
<span data-ttu-id="df0fa-129">Имя группы ресурсов, для которой этот cmdlet изменяет веб-часть.</span><span class="sxs-lookup"><span data-stu-id="df0fa-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="df0fa-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="df0fa-130">-RunOn</span></span>
<span data-ttu-id="df0fa-131">Необязательное имя гибридного агента, который должен выполнить книгу</span><span class="sxs-lookup"><span data-stu-id="df0fa-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="df0fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0fa-132">CommonParameters</span></span>
<span data-ttu-id="df0fa-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df0fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0fa-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df0fa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0fa-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df0fa-135">INPUTS</span></span>

### <span data-ttu-id="df0fa-136">System.String</span><span class="sxs-lookup"><span data-stu-id="df0fa-136">System.String</span></span>

### <span data-ttu-id="df0fa-137">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="df0fa-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="df0fa-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="df0fa-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="df0fa-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="df0fa-139">OUTPUTS</span></span>

### <span data-ttu-id="df0fa-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="df0fa-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="df0fa-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="df0fa-141">NOTES</span></span>

## <span data-ttu-id="df0fa-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df0fa-142">RELATED LINKS</span></span>

[<span data-ttu-id="df0fa-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="df0fa-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="df0fa-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="df0fa-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="df0fa-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="df0fa-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


