---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98510025"
---
# <span data-ttu-id="ade23-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ade23-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="ade23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade23-102">SYNOPSIS</span></span>
<span data-ttu-id="ade23-103">Получает веб-сайты из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ade23-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="ade23-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ade23-104">SYNTAX</span></span>

### <span data-ttu-id="ade23-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ade23-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ade23-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ade23-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ade23-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="ade23-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ade23-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ade23-108">DESCRIPTION</span></span>
<span data-ttu-id="ade23-109">Для **получения webhooks возвращается cmdlet Get-AzAutomationWebhook.**</span><span class="sxs-lookup"><span data-stu-id="ade23-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="ade23-110">Чтобы получить конкретные веб-части, укажите имя веб-приложения или имя книги автоматизации Azure, чтобы к ней подключались веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="ade23-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="ade23-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ade23-111">EXAMPLES</span></span>

### <span data-ttu-id="ade23-112">Пример 1. Получить все веб-сайты для книги</span><span class="sxs-lookup"><span data-stu-id="ade23-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="ade23-113">Эта команда получает все webhookы для книги Runbook03 в учетной записи автоматизации AutomationAccount01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ade23-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ade23-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ade23-114">PARAMETERS</span></span>

### <span data-ttu-id="ade23-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ade23-115">-AutomationAccountName</span></span>
<span data-ttu-id="ade23-116">Указывает имя учетной записи автоматизации, в которой этот cmdlet получает webhook.</span><span class="sxs-lookup"><span data-stu-id="ade23-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="ade23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade23-117">-DefaultProfile</span></span>
<span data-ttu-id="ade23-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ade23-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ade23-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ade23-119">-Name</span></span>
<span data-ttu-id="ade23-120">Определяет имя веб-приложения, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade23-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ade23-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade23-121">-ResourceGroupName</span></span>
<span data-ttu-id="ade23-122">Имя группы ресурсов, для которой этот cmdlet получает webhooks.</span><span class="sxs-lookup"><span data-stu-id="ade23-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="ade23-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="ade23-123">-RunbookName</span></span>
<span data-ttu-id="ade23-124">Определяет имя книги, для которой этот cmdlet получает webhooks.</span><span class="sxs-lookup"><span data-stu-id="ade23-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="ade23-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade23-125">CommonParameters</span></span>
<span data-ttu-id="ade23-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade23-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade23-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade23-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade23-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ade23-128">INPUTS</span></span>

### <span data-ttu-id="ade23-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ade23-129">System.String</span></span>

## <span data-ttu-id="ade23-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ade23-130">OUTPUTS</span></span>

### <span data-ttu-id="ade23-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="ade23-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="ade23-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ade23-132">NOTES</span></span>

## <span data-ttu-id="ade23-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ade23-133">RELATED LINKS</span></span>

[<span data-ttu-id="ade23-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ade23-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="ade23-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ade23-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="ade23-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ade23-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


