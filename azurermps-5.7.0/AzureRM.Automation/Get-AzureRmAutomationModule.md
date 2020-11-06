---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: 2011b0ec99e2ef2287e5b74a08a11fdc1e4ef149
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557608"
---
# <span data-ttu-id="61a6e-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="61a6e-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="61a6e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="61a6e-103">Получает метаданные для модулей из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="61a6e-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61a6e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61a6e-104">SYNTAX</span></span>

### <span data-ttu-id="61a6e-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61a6e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61a6e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="61a6e-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61a6e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61a6e-107">DESCRIPTION</span></span>
<span data-ttu-id="61a6e-108">Командлет **Get-AzureRmAutomationModule** получает метаданные для модулей из службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="61a6e-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="61a6e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61a6e-109">EXAMPLES</span></span>

### <span data-ttu-id="61a6e-110">Пример 1: получение всех модулей</span><span class="sxs-lookup"><span data-stu-id="61a6e-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="61a6e-111">Эта команда получает все модули в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="61a6e-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="61a6e-112">Пример 2: получение модуля</span><span class="sxs-lookup"><span data-stu-id="61a6e-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="61a6e-113">Эта команда получает модуль с именем ContosoModule в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="61a6e-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="61a6e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61a6e-114">PARAMETERS</span></span>

### <span data-ttu-id="61a6e-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="61a6e-115">-AutomationAccountName</span></span>
<span data-ttu-id="61a6e-116">Указывает имя учетной записи автоматизации, для которой этот командлет получает метаданные модуля.</span><span class="sxs-lookup"><span data-stu-id="61a6e-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="61a6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a6e-117">-DefaultProfile</span></span>
<span data-ttu-id="61a6e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="61a6e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61a6e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61a6e-119">-Name</span></span>
<span data-ttu-id="61a6e-120">Указывает имя модуля, для которого этот командлет получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="61a6e-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61a6e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a6e-121">-ResourceGroupName</span></span>
<span data-ttu-id="61a6e-122">Указывает имя группы ресурсов, для которой этот командлет получает метаданные модуля.</span><span class="sxs-lookup"><span data-stu-id="61a6e-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="61a6e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a6e-123">CommonParameters</span></span>
<span data-ttu-id="61a6e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61a6e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a6e-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a6e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a6e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61a6e-126">INPUTS</span></span>

### <span data-ttu-id="61a6e-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="61a6e-127">None</span></span>
<span data-ttu-id="61a6e-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="61a6e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61a6e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61a6e-129">OUTPUTS</span></span>

### <span data-ttu-id="61a6e-130">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="61a6e-130">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="61a6e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="61a6e-131">NOTES</span></span>

## <span data-ttu-id="61a6e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61a6e-132">RELATED LINKS</span></span>

[<span data-ttu-id="61a6e-133">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="61a6e-133">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="61a6e-134">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="61a6e-134">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="61a6e-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="61a6e-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


