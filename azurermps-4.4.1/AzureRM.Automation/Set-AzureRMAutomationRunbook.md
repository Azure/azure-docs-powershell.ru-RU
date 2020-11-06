---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 69fe223a7b574e370ed58385ed21ab2462e4420f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560560"
---
# <span data-ttu-id="98c44-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98c44-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="98c44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98c44-102">SYNOPSIS</span></span>
<span data-ttu-id="98c44-103">Изменение модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="98c44-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98c44-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c44-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98c44-105">DESCRIPTION</span></span>
<span data-ttu-id="98c44-106">Командлет **Set-AzureRmAutomationRunbook** изменяет конфигурацию Azure Automation RUNBOOK в ТД.</span><span class="sxs-lookup"><span data-stu-id="98c44-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="98c44-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98c44-107">EXAMPLES</span></span>

### <span data-ttu-id="98c44-108">Пример 1: включение подробного ведения журнала для модуля Runbook</span><span class="sxs-lookup"><span data-stu-id="98c44-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="98c44-109">Эта команда включает подробный журнал для заданий указанного Runbook в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="98c44-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="98c44-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98c44-110">PARAMETERS</span></span>

### <span data-ttu-id="98c44-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="98c44-111">-AutomationAccountName</span></span>
<span data-ttu-id="98c44-112">Указывает имя учетной записи автоматизации, в которой этот командлет изменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="98c44-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="98c44-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="98c44-113">-Description</span></span>
<span data-ttu-id="98c44-114">Задает описание для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="98c44-114">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c44-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="98c44-115">-LogProgress</span></span>
<span data-ttu-id="98c44-116">Указывает, выполняется ли журнал Runbook.</span><span class="sxs-lookup"><span data-stu-id="98c44-116">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c44-117">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="98c44-117">-LogVerbose</span></span>
<span data-ttu-id="98c44-118">Указывает, включаются ли в ведение журнала подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="98c44-118">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c44-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98c44-119">-Name</span></span>
<span data-ttu-id="98c44-120">Указывает имя Runbook, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="98c44-120">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="98c44-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c44-121">-ResourceGroupName</span></span>
<span data-ttu-id="98c44-122">Указывает имя группы ресурсов, для которой этот командлет изменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="98c44-122">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="98c44-123">-Теги</span><span class="sxs-lookup"><span data-stu-id="98c44-123">-Tags</span></span>
<span data-ttu-id="98c44-124">Указывает словарь тегов для замены текущих тегов измененного Runbook.</span><span class="sxs-lookup"><span data-stu-id="98c44-124">Specifies a dictionary of tags to replace the current tags of the modified runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c44-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c44-125">-DefaultProfile</span></span>
<span data-ttu-id="98c44-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98c44-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98c44-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c44-127">CommonParameters</span></span>
<span data-ttu-id="98c44-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98c44-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c44-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c44-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c44-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98c44-130">INPUTS</span></span>

## <span data-ttu-id="98c44-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98c44-131">OUTPUTS</span></span>

### <span data-ttu-id="98c44-132">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="98c44-132">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="98c44-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="98c44-133">NOTES</span></span>

## <span data-ttu-id="98c44-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98c44-134">RELATED LINKS</span></span>

[<span data-ttu-id="98c44-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98c44-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98c44-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98c44-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98c44-137">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98c44-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98c44-138">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98c44-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98c44-139">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98c44-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98c44-140">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98c44-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98c44-141">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98c44-141">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98c44-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98c44-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


