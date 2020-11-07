---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: 465e3ecd3f80b03eecb58309b18c91cd69c0d5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735112"
---
# <span data-ttu-id="b6fc9-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b6fc9-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="b6fc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fc9-103">Удаляет веб-перехватчик из модуля автоматизации Runbook.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6fc9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6fc9-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6fc9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="b6fc9-106">Командлет **Remove-AzureRmAutomationWebhook** удаляет обработчик для Azure Automation Runbook.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="b6fc9-107">Веб-перехватчик удален.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-107">The webhook is deleted.</span></span>

## <span data-ttu-id="b6fc9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6fc9-108">EXAMPLES</span></span>

### <span data-ttu-id="b6fc9-109">Пример 1: удаление веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="b6fc9-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="b6fc9-110">Эта команда удаляет веб-перехватчик с именем Webhook11 в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="b6fc9-111">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="b6fc9-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b6fc9-112">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b6fc9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6fc9-113">PARAMETERS</span></span>

### <span data-ttu-id="b6fc9-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b6fc9-114">-AutomationAccountName</span></span>
<span data-ttu-id="b6fc9-115">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="b6fc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6fc9-116">-DefaultProfile</span></span>
<span data-ttu-id="b6fc9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6fc9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6fc9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6fc9-118">-Name</span></span>
<span data-ttu-id="b6fc9-119">Указывает имя веб-перехватчика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6fc9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6fc9-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6fc9-121">Указывает имя группы ресурсов, для которой этот командлет удаляет веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="b6fc9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6fc9-122">-Confirm</span></span>
<span data-ttu-id="b6fc9-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6fc9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6fc9-124">-WhatIf</span></span>
<span data-ttu-id="b6fc9-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6fc9-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6fc9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fc9-127">CommonParameters</span></span>
<span data-ttu-id="b6fc9-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fc9-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6fc9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fc9-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6fc9-130">INPUTS</span></span>

### <span data-ttu-id="b6fc9-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="b6fc9-131">None</span></span>
<span data-ttu-id="b6fc9-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b6fc9-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6fc9-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6fc9-133">OUTPUTS</span></span>

## <span data-ttu-id="b6fc9-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6fc9-134">NOTES</span></span>

## <span data-ttu-id="b6fc9-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6fc9-135">RELATED LINKS</span></span>

[<span data-ttu-id="b6fc9-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b6fc9-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="b6fc9-137">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b6fc9-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="b6fc9-138">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b6fc9-138">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


