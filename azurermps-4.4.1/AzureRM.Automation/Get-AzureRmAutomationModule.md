---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: dcd84c47ff9a6dae06daaf05bde6dd6f4af86553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565693"
---
# <span data-ttu-id="17a67-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="17a67-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="17a67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17a67-102">SYNOPSIS</span></span>
<span data-ttu-id="17a67-103">Получает метаданные для модулей из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="17a67-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17a67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17a67-104">SYNTAX</span></span>

### <span data-ttu-id="17a67-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17a67-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17a67-106">ByName</span><span class="sxs-lookup"><span data-stu-id="17a67-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17a67-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17a67-107">DESCRIPTION</span></span>
<span data-ttu-id="17a67-108">Командлет **Get-AzureRmAutomationModule** получает метаданные для модулей из службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="17a67-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="17a67-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17a67-109">EXAMPLES</span></span>

### <span data-ttu-id="17a67-110">Пример 1: получение всех модулей</span><span class="sxs-lookup"><span data-stu-id="17a67-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="17a67-111">Эта команда получает все модули в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="17a67-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="17a67-112">Пример 2: получение модуля</span><span class="sxs-lookup"><span data-stu-id="17a67-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="17a67-113">Эта команда получает модуль с именем ContosoModule в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="17a67-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="17a67-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17a67-114">PARAMETERS</span></span>

### <span data-ttu-id="17a67-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17a67-115">-AutomationAccountName</span></span>
<span data-ttu-id="17a67-116">Указывает имя учетной записи автоматизации, для которой этот командлет получает метаданные модуля.</span><span class="sxs-lookup"><span data-stu-id="17a67-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="17a67-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17a67-117">-Name</span></span>
<span data-ttu-id="17a67-118">Указывает имя модуля, для которого этот командлет получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="17a67-118">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="17a67-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17a67-119">-ResourceGroupName</span></span>
<span data-ttu-id="17a67-120">Указывает имя группы ресурсов, для которой этот командлет получает метаданные модуля.</span><span class="sxs-lookup"><span data-stu-id="17a67-120">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="17a67-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17a67-121">-DefaultProfile</span></span>
<span data-ttu-id="17a67-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17a67-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17a67-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a67-123">CommonParameters</span></span>
<span data-ttu-id="17a67-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17a67-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a67-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17a67-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a67-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17a67-126">INPUTS</span></span>

## <span data-ttu-id="17a67-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17a67-127">OUTPUTS</span></span>

### <span data-ttu-id="17a67-128">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="17a67-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="17a67-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="17a67-129">NOTES</span></span>

## <span data-ttu-id="17a67-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17a67-130">RELATED LINKS</span></span>

[<span data-ttu-id="17a67-131">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="17a67-131">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="17a67-132">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="17a67-132">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="17a67-133">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="17a67-133">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


