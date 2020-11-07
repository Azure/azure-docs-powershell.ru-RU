---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912901"
---
# <span data-ttu-id="d101b-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d101b-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="d101b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d101b-102">SYNOPSIS</span></span>
<span data-ttu-id="d101b-103">Изменяет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d101b-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="d101b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d101b-104">SYNTAX</span></span>

### <span data-ttu-id="d101b-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="d101b-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d101b-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="d101b-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d101b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d101b-107">DESCRIPTION</span></span>
<span data-ttu-id="d101b-108">Командлет **Set-AzAutomationVariable** изменяет значение или описание переменной в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d101b-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="d101b-109">Чтобы зашифровать переменную, укажите *зашифрованный* параметр.</span><span class="sxs-lookup"><span data-stu-id="d101b-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="d101b-110">После создания переменной невозможно изменить зашифрованное состояние.</span><span class="sxs-lookup"><span data-stu-id="d101b-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="d101b-111">Если задать для существующей, незашифрованной переменной значение *Encrypted* , то переменная не будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="d101b-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="d101b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d101b-112">EXAMPLES</span></span>

### <span data-ttu-id="d101b-113">Пример 1: Установка значения переменной</span><span class="sxs-lookup"><span data-stu-id="d101b-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="d101b-114">Эта команда задает новое значение переменной с именем StringVariable22 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d101b-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d101b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d101b-115">PARAMETERS</span></span>

### <span data-ttu-id="d101b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d101b-116">-AutomationAccountName</span></span>
<span data-ttu-id="d101b-117">Указывает имя учетной записи автоматизации, в которой хранится переменная.</span><span class="sxs-lookup"><span data-stu-id="d101b-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="d101b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d101b-118">-DefaultProfile</span></span>
<span data-ttu-id="d101b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d101b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d101b-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="d101b-120">-Description</span></span>
<span data-ttu-id="d101b-121">Задает описание переменной.</span><span class="sxs-lookup"><span data-stu-id="d101b-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="d101b-122">С шифрованием</span><span class="sxs-lookup"><span data-stu-id="d101b-122">-Encrypted</span></span>
<span data-ttu-id="d101b-123">Указывает, шифрует ли командлет значение переменной для хранения.</span><span class="sxs-lookup"><span data-stu-id="d101b-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="d101b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d101b-124">-Name</span></span>
<span data-ttu-id="d101b-125">Указывает имя переменной, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d101b-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d101b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d101b-126">-ResourceGroupName</span></span>
<span data-ttu-id="d101b-127">Указывает группу ресурсов, для которой этот командлет изменяет переменную.</span><span class="sxs-lookup"><span data-stu-id="d101b-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="d101b-128">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="d101b-128">-Value</span></span>
<span data-ttu-id="d101b-129">Задает значение переменной.</span><span class="sxs-lookup"><span data-stu-id="d101b-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="d101b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d101b-130">CommonParameters</span></span>
<span data-ttu-id="d101b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d101b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d101b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d101b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d101b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d101b-133">INPUTS</span></span>

### <span data-ttu-id="d101b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d101b-134">System.String</span></span>

### <span data-ttu-id="d101b-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d101b-135">System.Boolean</span></span>

### <span data-ttu-id="d101b-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="d101b-136">System.Object</span></span>

## <span data-ttu-id="d101b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d101b-137">OUTPUTS</span></span>

### <span data-ttu-id="d101b-138">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="d101b-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="d101b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d101b-139">NOTES</span></span>

## <span data-ttu-id="d101b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d101b-140">RELATED LINKS</span></span>

[<span data-ttu-id="d101b-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d101b-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="d101b-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d101b-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="d101b-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d101b-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


