---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235108"
---
# <span data-ttu-id="49a38-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="49a38-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="49a38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49a38-102">SYNOPSIS</span></span>
<span data-ttu-id="49a38-103">Получает метаданные для модулей из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="49a38-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="49a38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49a38-104">SYNTAX</span></span>

### <span data-ttu-id="49a38-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49a38-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49a38-106">ByName</span><span class="sxs-lookup"><span data-stu-id="49a38-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49a38-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49a38-107">DESCRIPTION</span></span>
<span data-ttu-id="49a38-108">Командлет **Get-AzAutomationModule** получает метаданные для модулей из службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="49a38-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="49a38-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49a38-109">EXAMPLES</span></span>

### <span data-ttu-id="49a38-110">Пример 1: получение всех модулей</span><span class="sxs-lookup"><span data-stu-id="49a38-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="49a38-111">Эта команда получает все модули в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="49a38-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="49a38-112">Пример 2: получение модуля</span><span class="sxs-lookup"><span data-stu-id="49a38-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="49a38-113">Эта команда получает модуль с именем ContosoModule в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="49a38-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="49a38-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49a38-114">PARAMETERS</span></span>

### <span data-ttu-id="49a38-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="49a38-115">-AutomationAccountName</span></span>
<span data-ttu-id="49a38-116">Указывает имя учетной записи автоматизации, для которой этот командлет получает метаданные модуля.</span><span class="sxs-lookup"><span data-stu-id="49a38-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="49a38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a38-117">-DefaultProfile</span></span>
<span data-ttu-id="49a38-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="49a38-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49a38-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49a38-119">-Name</span></span>
<span data-ttu-id="49a38-120">Указывает имя модуля, для которого этот командлет получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="49a38-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a38-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a38-121">-ResourceGroupName</span></span>
<span data-ttu-id="49a38-122">Указывает имя группы ресурсов, для которой этот командлет получает метаданные модуля.</span><span class="sxs-lookup"><span data-stu-id="49a38-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="49a38-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a38-123">CommonParameters</span></span>
<span data-ttu-id="49a38-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49a38-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a38-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a38-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a38-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49a38-126">INPUTS</span></span>

### <span data-ttu-id="49a38-127">System. String</span><span class="sxs-lookup"><span data-stu-id="49a38-127">System.String</span></span>

## <span data-ttu-id="49a38-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49a38-128">OUTPUTS</span></span>

### <span data-ttu-id="49a38-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="49a38-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="49a38-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="49a38-130">NOTES</span></span>

## <span data-ttu-id="49a38-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49a38-131">RELATED LINKS</span></span>

[<span data-ttu-id="49a38-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="49a38-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="49a38-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="49a38-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="49a38-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="49a38-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


