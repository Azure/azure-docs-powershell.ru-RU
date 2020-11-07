---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 30ecb11822e622457600eb2a126171d431372f07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731585"
---
# <span data-ttu-id="dcf7b-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="dcf7b-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="dcf7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcf7b-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf7b-103">Получает веб-перехватчики из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="dcf7b-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="dcf7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcf7b-104">SYNTAX</span></span>

### <span data-ttu-id="dcf7b-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcf7b-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcf7b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dcf7b-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcf7b-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="dcf7b-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcf7b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcf7b-108">DESCRIPTION</span></span>
<span data-ttu-id="dcf7b-109">Командлет **Get-AzAutomationWebhook — это внешние** перехватчики.</span><span class="sxs-lookup"><span data-stu-id="dcf7b-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="dcf7b-110">Чтобы получить доступ к определенным веб-перехватчикам, укажите имя веб-перехватчика или укажите имя Runbook службы автоматизации Azure для подключения веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="dcf7b-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="dcf7b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcf7b-111">EXAMPLES</span></span>

### <span data-ttu-id="dcf7b-112">Пример 1: получение всех веб-перехватчиков для Runbook</span><span class="sxs-lookup"><span data-stu-id="dcf7b-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="dcf7b-113">Эта команда получает все веб-перехватчики для Runbook с именем Runbook03 в учетной записи автоматизации с именем AutomationAccount01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="dcf7b-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="dcf7b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcf7b-114">PARAMETERS</span></span>

### <span data-ttu-id="dcf7b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dcf7b-115">-AutomationAccountName</span></span>
<span data-ttu-id="dcf7b-116">Указывает имя учетной записи автоматизации, в которой этот командлет получает веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="dcf7b-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="dcf7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf7b-117">-DefaultProfile</span></span>
<span data-ttu-id="dcf7b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dcf7b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcf7b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcf7b-119">-Name</span></span>
<span data-ttu-id="dcf7b-120">Указывает имя веб-перехватчика, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dcf7b-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf7b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf7b-121">-ResourceGroupName</span></span>
<span data-ttu-id="dcf7b-122">Указывает имя группы ресурсов, для которой этот командлет получает веб-перехватчики.</span><span class="sxs-lookup"><span data-stu-id="dcf7b-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="dcf7b-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="dcf7b-123">-RunbookName</span></span>
<span data-ttu-id="dcf7b-124">Указывает имя Runbook, для которого этот командлет получает веб-перехватчики.</span><span class="sxs-lookup"><span data-stu-id="dcf7b-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf7b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf7b-125">CommonParameters</span></span>
<span data-ttu-id="dcf7b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcf7b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf7b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf7b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf7b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcf7b-128">INPUTS</span></span>

### <span data-ttu-id="dcf7b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf7b-129">System.String</span></span>

## <span data-ttu-id="dcf7b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcf7b-130">OUTPUTS</span></span>

### <span data-ttu-id="dcf7b-131">Microsoft. Azure. Commands. Automation. Model. веб-перехватчик</span><span class="sxs-lookup"><span data-stu-id="dcf7b-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="dcf7b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcf7b-132">NOTES</span></span>

## <span data-ttu-id="dcf7b-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcf7b-133">RELATED LINKS</span></span>

[<span data-ttu-id="dcf7b-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="dcf7b-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="dcf7b-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="dcf7b-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="dcf7b-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="dcf7b-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


