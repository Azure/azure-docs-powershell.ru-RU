---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 71d66c6440091e50da2809f4b8c0669410d09d50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567180"
---
# <span data-ttu-id="4bb4e-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="4bb4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4bb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb4e-103">Публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="4bb4e-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bb4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4bb4e-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bb4e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bb4e-105">DESCRIPTION</span></span>
<span data-ttu-id="4bb4e-106">Командлет **Publish-AzureRmAutomationRunbook** публикует Runbook для использования в производственной среде службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb4e-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="4bb4e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4bb4e-107">EXAMPLES</span></span>

### <span data-ttu-id="4bb4e-108">Пример 1: публикация Runbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4bb4e-109">Эта команда публикует Runbook с именем Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4bb4e-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4bb4e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4bb4e-110">PARAMETERS</span></span>

### <span data-ttu-id="4bb4e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4bb4e-111">-AutomationAccountName</span></span>
<span data-ttu-id="4bb4e-112">Указывает имя учетной записи автоматизации, в которой этот командлет публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="4bb4e-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="4bb4e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4bb4e-113">-Name</span></span>
<span data-ttu-id="4bb4e-114">Указывает имя Runbook, который публикует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4bb4e-114">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb4e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb4e-115">-ResourceGroupName</span></span>
<span data-ttu-id="4bb4e-116">Указывает имя группы ресурсов, для которой этот командлет публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="4bb4e-116">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="4bb4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb4e-117">-DefaultProfile</span></span>
<span data-ttu-id="4bb4e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb4e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bb4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb4e-119">CommonParameters</span></span>
<span data-ttu-id="4bb4e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4bb4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb4e-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bb4e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb4e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4bb4e-122">INPUTS</span></span>

## <span data-ttu-id="4bb4e-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bb4e-123">OUTPUTS</span></span>

### <span data-ttu-id="4bb4e-124">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-124">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="4bb4e-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="4bb4e-125">NOTES</span></span>

## <span data-ttu-id="4bb4e-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bb4e-126">RELATED LINKS</span></span>

[<span data-ttu-id="4bb4e-127">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-127">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4bb4e-128">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-128">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4bb4e-129">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-129">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4bb4e-130">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-130">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4bb4e-131">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4bb4e-132">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-132">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4bb4e-133">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-133">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4bb4e-134">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4bb4e-134">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


