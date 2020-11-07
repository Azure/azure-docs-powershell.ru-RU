---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
ms.openlocfilehash: a384753d6407eff7864cea6972ac03ab5bd12515
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733185"
---
# <span data-ttu-id="eafa4-101">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eafa4-101">Get-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="eafa4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eafa4-102">SYNOPSIS</span></span>
<span data-ttu-id="eafa4-103">Получает веб-перехватчики из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="eafa4-103">Gets webhooks from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eafa4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eafa4-104">SYNTAX</span></span>

### <span data-ttu-id="eafa4-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eafa4-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eafa4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="eafa4-106">ByName</span></span>
```
Get-AzureRmAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eafa4-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="eafa4-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eafa4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafa4-108">DESCRIPTION</span></span>
<span data-ttu-id="eafa4-109">Командлет **Get-AzureRmAutomationWebhook — это внешние** перехватчики.</span><span class="sxs-lookup"><span data-stu-id="eafa4-109">The **Get-AzureRmAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="eafa4-110">Чтобы получить доступ к определенным веб-перехватчикам, укажите имя веб-перехватчика или укажите имя Runbook службы автоматизации Azure для подключения веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="eafa4-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="eafa4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eafa4-111">EXAMPLES</span></span>

### <span data-ttu-id="eafa4-112">Пример 1: получение всех веб-перехватчиков для Runbook</span><span class="sxs-lookup"><span data-stu-id="eafa4-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="eafa4-113">Эта команда получает все веб-перехватчики для Runbook с именем Runbook03 в учетной записи автоматизации с именем AutomationAccount01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="eafa4-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="eafa4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eafa4-114">PARAMETERS</span></span>

### <span data-ttu-id="eafa4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eafa4-115">-AutomationAccountName</span></span>
<span data-ttu-id="eafa4-116">Указывает имя учетной записи автоматизации, в которой этот командлет получает веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="eafa4-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="eafa4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafa4-117">-DefaultProfile</span></span>
<span data-ttu-id="eafa4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eafa4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eafa4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eafa4-119">-Name</span></span>
<span data-ttu-id="eafa4-120">Указывает имя веб-перехватчика, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eafa4-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eafa4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eafa4-121">-ResourceGroupName</span></span>
<span data-ttu-id="eafa4-122">Указывает имя группы ресурсов, для которой этот командлет получает веб-перехватчики.</span><span class="sxs-lookup"><span data-stu-id="eafa4-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="eafa4-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="eafa4-123">-RunbookName</span></span>
<span data-ttu-id="eafa4-124">Указывает имя Runbook, для которого этот командлет получает веб-перехватчики.</span><span class="sxs-lookup"><span data-stu-id="eafa4-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="eafa4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafa4-125">CommonParameters</span></span>
<span data-ttu-id="eafa4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eafa4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafa4-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafa4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafa4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eafa4-128">INPUTS</span></span>

### <span data-ttu-id="eafa4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="eafa4-129">System.String</span></span>

## <span data-ttu-id="eafa4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafa4-130">OUTPUTS</span></span>

### <span data-ttu-id="eafa4-131">Microsoft. Azure. Commands. Automation. Model. веб-перехватчик</span><span class="sxs-lookup"><span data-stu-id="eafa4-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="eafa4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="eafa4-132">NOTES</span></span>

## <span data-ttu-id="eafa4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eafa4-133">RELATED LINKS</span></span>

[<span data-ttu-id="eafa4-134">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eafa4-134">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="eafa4-135">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eafa4-135">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="eafa4-136">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="eafa4-136">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


