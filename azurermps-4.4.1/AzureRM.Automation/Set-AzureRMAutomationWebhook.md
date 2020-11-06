---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: b889a3b061556fc6c5ad4be1dfd118dac49f1f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560552"
---
# <span data-ttu-id="f757f-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="f757f-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="f757f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f757f-102">SYNOPSIS</span></span>
<span data-ttu-id="f757f-103">Изменяет веб-перехватчик для модуля автоматизации Runbook.</span><span class="sxs-lookup"><span data-stu-id="f757f-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f757f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f757f-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f757f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f757f-105">DESCRIPTION</span></span>
<span data-ttu-id="f757f-106">Командлет **Set-AzureRmAutomationWebhook** изменяет интерфейс для Azure Automation Runbook.</span><span class="sxs-lookup"><span data-stu-id="f757f-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="f757f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f757f-107">EXAMPLES</span></span>

### <span data-ttu-id="f757f-108">Пример 1: Отключение веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="f757f-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="f757f-109">Эта команда отключает веб-перехватчик с именем Webhook01 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="f757f-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="f757f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f757f-110">PARAMETERS</span></span>

### <span data-ttu-id="f757f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f757f-111">-AutomationAccountName</span></span>
<span data-ttu-id="f757f-112">Указывает имя учетной записи автоматизации, в которой этот командлет изменяет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="f757f-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="f757f-113">-Включено</span><span class="sxs-lookup"><span data-stu-id="f757f-113">-IsEnabled</span></span>
<span data-ttu-id="f757f-114">Указывает, включен ли веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="f757f-114">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="f757f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f757f-115">-Name</span></span>
<span data-ttu-id="f757f-116">Указывает имя веб-перехватчика, измененного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f757f-116">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f757f-117">-Parameters</span><span class="sxs-lookup"><span data-stu-id="f757f-117">-Parameters</span></span>
<span data-ttu-id="f757f-118">Указывает словарь пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="f757f-118">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="f757f-119">Ключи — это имена параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="f757f-119">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="f757f-120">Значения — это значения параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="f757f-120">The values are the runbook parameter values.</span></span>
<span data-ttu-id="f757f-121">При запуске модуля Runbook в ответ на веб-перехватчик эти параметры передаются в модуль Runbook.</span><span class="sxs-lookup"><span data-stu-id="f757f-121">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="f757f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f757f-122">-ResourceGroupName</span></span>
<span data-ttu-id="f757f-123">Указывает имя группы ресурсов, для которой этот командлет изменяет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="f757f-123">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="f757f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f757f-124">-DefaultProfile</span></span>
<span data-ttu-id="f757f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f757f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f757f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f757f-126">CommonParameters</span></span>
<span data-ttu-id="f757f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f757f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f757f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f757f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f757f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f757f-129">INPUTS</span></span>

## <span data-ttu-id="f757f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f757f-130">OUTPUTS</span></span>

### <span data-ttu-id="f757f-131">Microsoft. Azure. Commands. Automation. Model. веб-перехватчик</span><span class="sxs-lookup"><span data-stu-id="f757f-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="f757f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f757f-132">NOTES</span></span>

## <span data-ttu-id="f757f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f757f-133">RELATED LINKS</span></span>

[<span data-ttu-id="f757f-134">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="f757f-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="f757f-135">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="f757f-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="f757f-136">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="f757f-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


