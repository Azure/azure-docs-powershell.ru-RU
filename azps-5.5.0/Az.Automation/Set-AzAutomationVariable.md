---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216185"
---
# <span data-ttu-id="ff46b-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ff46b-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="ff46b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff46b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff46b-103">Изменяет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ff46b-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="ff46b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff46b-104">SYNTAX</span></span>

### <span data-ttu-id="ff46b-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="ff46b-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff46b-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="ff46b-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff46b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff46b-107">DESCRIPTION</span></span>
<span data-ttu-id="ff46b-108">**Cmdlet Set-AzAutomationVariable** изменяет значение или описание переменной в автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ff46b-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="ff46b-109">Чтобы зашифровать переменную, укажите параметр *Encrypted.*</span><span class="sxs-lookup"><span data-stu-id="ff46b-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="ff46b-110">Состояние шифрованной переменной после создания изменить невозможно.</span><span class="sxs-lookup"><span data-stu-id="ff46b-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="ff46b-111">Не удается *указать зашифрованную* переменную для существующей переменной, которая не шифруется.</span><span class="sxs-lookup"><span data-stu-id="ff46b-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="ff46b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff46b-112">EXAMPLES</span></span>

### <span data-ttu-id="ff46b-113">Пример 1. Настройка значения переменной</span><span class="sxs-lookup"><span data-stu-id="ff46b-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="ff46b-114">Эта команда задает новое значение для переменной StringVariable22 в учетной записи автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ff46b-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ff46b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff46b-115">PARAMETERS</span></span>

### <span data-ttu-id="ff46b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ff46b-116">-AutomationAccountName</span></span>
<span data-ttu-id="ff46b-117">Указывает имя учетной записи автоматизации, в которой хранится переменная.</span><span class="sxs-lookup"><span data-stu-id="ff46b-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="ff46b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff46b-118">-DefaultProfile</span></span>
<span data-ttu-id="ff46b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ff46b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff46b-120">-Description</span><span class="sxs-lookup"><span data-stu-id="ff46b-120">-Description</span></span>
<span data-ttu-id="ff46b-121">Описание переменной.</span><span class="sxs-lookup"><span data-stu-id="ff46b-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="ff46b-122">-Encrypted</span><span class="sxs-lookup"><span data-stu-id="ff46b-122">-Encrypted</span></span>
<span data-ttu-id="ff46b-123">Определяет, шифрует ли cmdlet значение переменной для хранения.</span><span class="sxs-lookup"><span data-stu-id="ff46b-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="ff46b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ff46b-124">-Name</span></span>
<span data-ttu-id="ff46b-125">Указывает имя переменной, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff46b-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ff46b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff46b-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff46b-127">Определяет группу ресурсов, для которой этот cmdlet изменяет переменную.</span><span class="sxs-lookup"><span data-stu-id="ff46b-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="ff46b-128">-Значение</span><span class="sxs-lookup"><span data-stu-id="ff46b-128">-Value</span></span>
<span data-ttu-id="ff46b-129">Указывает значение переменной.</span><span class="sxs-lookup"><span data-stu-id="ff46b-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="ff46b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff46b-130">CommonParameters</span></span>
<span data-ttu-id="ff46b-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff46b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff46b-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff46b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff46b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff46b-133">INPUTS</span></span>

### <span data-ttu-id="ff46b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ff46b-134">System.String</span></span>

### <span data-ttu-id="ff46b-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff46b-135">System.Boolean</span></span>

### <span data-ttu-id="ff46b-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="ff46b-136">System.Object</span></span>

## <span data-ttu-id="ff46b-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff46b-137">OUTPUTS</span></span>

### <span data-ttu-id="ff46b-138">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="ff46b-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="ff46b-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff46b-139">NOTES</span></span>

## <span data-ttu-id="ff46b-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff46b-140">RELATED LINKS</span></span>

[<span data-ttu-id="ff46b-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ff46b-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="ff46b-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ff46b-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="ff46b-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ff46b-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


