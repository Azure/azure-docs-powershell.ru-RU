---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: 4036261cd333194a71d302e57e97a1f017554da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556875"
---
# <span data-ttu-id="3423e-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3423e-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="3423e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3423e-102">SYNOPSIS</span></span>
<span data-ttu-id="3423e-103">Создает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3423e-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3423e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3423e-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3423e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3423e-105">DESCRIPTION</span></span>
<span data-ttu-id="3423e-106">Командлет **New-AzureRmAutomationVariable** создает переменную в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3423e-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="3423e-107">Чтобы зашифровать переменную, укажите *зашифрованный* параметр.</span><span class="sxs-lookup"><span data-stu-id="3423e-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="3423e-108">После создания переменной невозможно изменить зашифрованное состояние.</span><span class="sxs-lookup"><span data-stu-id="3423e-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="3423e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3423e-109">EXAMPLES</span></span>

### <span data-ttu-id="3423e-110">Пример 1: создание переменной с простым значением</span><span class="sxs-lookup"><span data-stu-id="3423e-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3423e-111">Эта команда создает переменную с именем StringVariable22, которая имеет строковое значение в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3423e-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3423e-112">Пример 2: создание переменной со сложным значением</span><span class="sxs-lookup"><span data-stu-id="3423e-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3423e-113">Первая команда получает виртуальную машину с помощью командлета Get-AzureVM.</span><span class="sxs-lookup"><span data-stu-id="3423e-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="3423e-114">Команда сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="3423e-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="3423e-115">Вторая команда создает переменную с именем ComplexVariable01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3423e-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="3423e-116">Эта команда использует сложный объект для его значения (в данном случае — виртуальная машина в $VirtualMachine).</span><span class="sxs-lookup"><span data-stu-id="3423e-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="3423e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3423e-117">PARAMETERS</span></span>

### <span data-ttu-id="3423e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3423e-118">-AutomationAccountName</span></span>
<span data-ttu-id="3423e-119">Указывает имя учетной записи автоматизации, в которой будет храниться переменная.</span><span class="sxs-lookup"><span data-stu-id="3423e-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="3423e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3423e-120">-DefaultProfile</span></span>
<span data-ttu-id="3423e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3423e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3423e-122">-Описание</span><span class="sxs-lookup"><span data-stu-id="3423e-122">-Description</span></span>
<span data-ttu-id="3423e-123">Задает описание переменной.</span><span class="sxs-lookup"><span data-stu-id="3423e-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="3423e-124">С шифрованием</span><span class="sxs-lookup"><span data-stu-id="3423e-124">-Encrypted</span></span>
<span data-ttu-id="3423e-125">Указывает, шифрует ли этот командлет значение переменной для хранения.</span><span class="sxs-lookup"><span data-stu-id="3423e-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3423e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3423e-126">-Name</span></span>
<span data-ttu-id="3423e-127">Задает имя переменной.</span><span class="sxs-lookup"><span data-stu-id="3423e-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="3423e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3423e-128">-ResourceGroupName</span></span>
<span data-ttu-id="3423e-129">Указывает группу ресурсов, для которой этот командлет создает переменную.</span><span class="sxs-lookup"><span data-stu-id="3423e-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="3423e-130">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="3423e-130">-Value</span></span>
<span data-ttu-id="3423e-131">Задает значение переменной.</span><span class="sxs-lookup"><span data-stu-id="3423e-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3423e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3423e-132">CommonParameters</span></span>
<span data-ttu-id="3423e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3423e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3423e-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3423e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3423e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3423e-135">INPUTS</span></span>

### <span data-ttu-id="3423e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3423e-136">System.String</span></span>

### <span data-ttu-id="3423e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3423e-137">System.Boolean</span></span>

### <span data-ttu-id="3423e-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="3423e-138">System.Object</span></span>

## <span data-ttu-id="3423e-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3423e-139">OUTPUTS</span></span>

### <span data-ttu-id="3423e-140">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="3423e-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="3423e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3423e-141">NOTES</span></span>

## <span data-ttu-id="3423e-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3423e-142">RELATED LINKS</span></span>

[<span data-ttu-id="3423e-143">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3423e-143">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="3423e-144">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3423e-144">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="3423e-145">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3423e-145">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


