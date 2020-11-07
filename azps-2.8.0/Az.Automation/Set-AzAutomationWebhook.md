---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 39e0fda02eb41ed591562d9cfc1f7902fa43c38a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727724"
---
# <span data-ttu-id="69e7b-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="69e7b-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="69e7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="69e7b-103">Изменяет веб-перехватчик для модуля автоматизации Runbook.</span><span class="sxs-lookup"><span data-stu-id="69e7b-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="69e7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69e7b-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69e7b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="69e7b-106">Командлет **Set-AzAutomationWebhook** изменяет интерфейс для Azure Automation Runbook.</span><span class="sxs-lookup"><span data-stu-id="69e7b-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="69e7b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="69e7b-108">Пример 1: Отключение веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="69e7b-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="69e7b-109">Эта команда отключает веб-перехватчик с именем Webhook01 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="69e7b-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="69e7b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69e7b-110">PARAMETERS</span></span>

### <span data-ttu-id="69e7b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="69e7b-111">-AutomationAccountName</span></span>
<span data-ttu-id="69e7b-112">Указывает имя учетной записи автоматизации, в которой этот командлет изменяет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="69e7b-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="69e7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e7b-113">-DefaultProfile</span></span>
<span data-ttu-id="69e7b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="69e7b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69e7b-115">-Включено</span><span class="sxs-lookup"><span data-stu-id="69e7b-115">-IsEnabled</span></span>
<span data-ttu-id="69e7b-116">Указывает, включен ли веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="69e7b-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="69e7b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="69e7b-117">-Name</span></span>
<span data-ttu-id="69e7b-118">Указывает имя веб-перехватчика, измененного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="69e7b-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="69e7b-119">-Parameters</span><span class="sxs-lookup"><span data-stu-id="69e7b-119">-Parameters</span></span>
<span data-ttu-id="69e7b-120">Указывает словарь пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="69e7b-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="69e7b-121">Ключи — это имена параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="69e7b-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="69e7b-122">Значения — это значения параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="69e7b-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="69e7b-123">При запуске модуля Runbook в ответ на веб-перехватчик эти параметры передаются в модуль Runbook.</span><span class="sxs-lookup"><span data-stu-id="69e7b-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="69e7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="69e7b-125">Указывает имя группы ресурсов, для которой этот командлет изменяет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="69e7b-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="69e7b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e7b-126">CommonParameters</span></span>
<span data-ttu-id="69e7b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69e7b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e7b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69e7b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e7b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69e7b-129">INPUTS</span></span>

### <span data-ttu-id="69e7b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="69e7b-130">System.String</span></span>

### <span data-ttu-id="69e7b-131">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="69e7b-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="69e7b-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="69e7b-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="69e7b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69e7b-133">OUTPUTS</span></span>

### <span data-ttu-id="69e7b-134">Microsoft. Azure. Commands. Automation. Model. веб-перехватчик</span><span class="sxs-lookup"><span data-stu-id="69e7b-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="69e7b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="69e7b-135">NOTES</span></span>

## <span data-ttu-id="69e7b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69e7b-136">RELATED LINKS</span></span>

[<span data-ttu-id="69e7b-137">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="69e7b-137">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="69e7b-138">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="69e7b-138">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="69e7b-139">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="69e7b-139">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


