---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 462566749ce0c55d4f892cc19e362f62b6fd0fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556848"
---
# <span data-ttu-id="5912b-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5912b-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="5912b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5912b-102">SYNOPSIS</span></span>
<span data-ttu-id="5912b-103">Изменяет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5912b-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5912b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5912b-104">SYNTAX</span></span>

### <span data-ttu-id="5912b-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="5912b-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5912b-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="5912b-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5912b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5912b-107">DESCRIPTION</span></span>
<span data-ttu-id="5912b-108">Командлет **Set-AzureRmAutomationVariable** изменяет значение или описание переменной в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5912b-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="5912b-109">Чтобы зашифровать переменную, укажите *зашифрованный* параметр.</span><span class="sxs-lookup"><span data-stu-id="5912b-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="5912b-110">После создания переменной невозможно изменить зашифрованное состояние.</span><span class="sxs-lookup"><span data-stu-id="5912b-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="5912b-111">Если задать для существующей, незашифрованной переменной значение *Encrypted* , то переменная не будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="5912b-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="5912b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5912b-112">EXAMPLES</span></span>

### <span data-ttu-id="5912b-113">Пример 1: Установка значения переменной</span><span class="sxs-lookup"><span data-stu-id="5912b-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="5912b-114">Эта команда задает новое значение переменной с именем StringVariable22 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5912b-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5912b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5912b-115">PARAMETERS</span></span>

### <span data-ttu-id="5912b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5912b-116">-AutomationAccountName</span></span>
<span data-ttu-id="5912b-117">Указывает имя учетной записи автоматизации, в которой хранится переменная.</span><span class="sxs-lookup"><span data-stu-id="5912b-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="5912b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5912b-118">-DefaultProfile</span></span>
<span data-ttu-id="5912b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5912b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5912b-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="5912b-120">-Description</span></span>
<span data-ttu-id="5912b-121">Задает описание переменной.</span><span class="sxs-lookup"><span data-stu-id="5912b-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5912b-122">С шифрованием</span><span class="sxs-lookup"><span data-stu-id="5912b-122">-Encrypted</span></span>
<span data-ttu-id="5912b-123">Указывает, шифрует ли командлет значение переменной для хранения.</span><span class="sxs-lookup"><span data-stu-id="5912b-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5912b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5912b-124">-Name</span></span>
<span data-ttu-id="5912b-125">Указывает имя переменной, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5912b-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5912b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5912b-126">-ResourceGroupName</span></span>
<span data-ttu-id="5912b-127">Указывает группу ресурсов, для которой этот командлет изменяет переменную.</span><span class="sxs-lookup"><span data-stu-id="5912b-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="5912b-128">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="5912b-128">-Value</span></span>
<span data-ttu-id="5912b-129">Задает значение переменной.</span><span class="sxs-lookup"><span data-stu-id="5912b-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5912b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5912b-130">CommonParameters</span></span>
<span data-ttu-id="5912b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5912b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5912b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5912b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5912b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5912b-133">INPUTS</span></span>

### <span data-ttu-id="5912b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5912b-134">System.String</span></span>

### <span data-ttu-id="5912b-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5912b-135">System.Boolean</span></span>

### <span data-ttu-id="5912b-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="5912b-136">System.Object</span></span>

## <span data-ttu-id="5912b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5912b-137">OUTPUTS</span></span>

### <span data-ttu-id="5912b-138">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="5912b-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="5912b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5912b-139">NOTES</span></span>

## <span data-ttu-id="5912b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5912b-140">RELATED LINKS</span></span>

[<span data-ttu-id="5912b-141">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5912b-141">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="5912b-142">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5912b-142">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="5912b-143">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5912b-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


