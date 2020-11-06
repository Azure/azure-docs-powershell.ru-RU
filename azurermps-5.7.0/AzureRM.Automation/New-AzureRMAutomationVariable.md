---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: 217a6553a21871e79998dcad0630f4c0e1b6aec4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568255"
---
# <span data-ttu-id="1e2e9-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1e2e9-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="1e2e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2e9-103">Создает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e2e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e2e9-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e2e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e2e9-105">DESCRIPTION</span></span>
<span data-ttu-id="1e2e9-106">Командлет **New-AzureRmAutomationVariable** создает переменную в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="1e2e9-107">Чтобы зашифровать переменную, укажите *зашифрованный* параметр.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="1e2e9-108">После создания переменной невозможно изменить зашифрованное состояние.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="1e2e9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e2e9-109">EXAMPLES</span></span>

### <span data-ttu-id="1e2e9-110">Пример 1: создание переменной с простым значением</span><span class="sxs-lookup"><span data-stu-id="1e2e9-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1e2e9-111">Эта команда создает переменную с именем StringVariable22, которая имеет строковое значение в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1e2e9-112">Пример 2: создание переменной со сложным значением</span><span class="sxs-lookup"><span data-stu-id="1e2e9-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1e2e9-113">Первая команда получает виртуальную машину с помощью командлета Get-AzureVM.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="1e2e9-114">Команда сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="1e2e9-115">Вторая команда создает переменную с именем ComplexVariable01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="1e2e9-116">Эта команда использует сложный объект для его значения (в данном случае — виртуальная машина в $VirtualMachine).</span><span class="sxs-lookup"><span data-stu-id="1e2e9-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="1e2e9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e2e9-117">PARAMETERS</span></span>

### <span data-ttu-id="1e2e9-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1e2e9-118">-AutomationAccountName</span></span>
<span data-ttu-id="1e2e9-119">Указывает имя учетной записи автоматизации, в которой будет храниться переменная.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="1e2e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2e9-120">-DefaultProfile</span></span>
<span data-ttu-id="1e2e9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1e2e9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e2e9-122">-Описание</span><span class="sxs-lookup"><span data-stu-id="1e2e9-122">-Description</span></span>
<span data-ttu-id="1e2e9-123">Задает описание переменной.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-123">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2e9-124">С шифрованием</span><span class="sxs-lookup"><span data-stu-id="1e2e9-124">-Encrypted</span></span>
<span data-ttu-id="1e2e9-125">Указывает, шифрует ли этот командлет значение переменной для хранения.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2e9-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e2e9-126">-Name</span></span>
<span data-ttu-id="1e2e9-127">Задает имя переменной.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-127">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2e9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e2e9-128">-ResourceGroupName</span></span>
<span data-ttu-id="1e2e9-129">Указывает группу ресурсов, для которой этот командлет создает переменную.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="1e2e9-130">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="1e2e9-130">-Value</span></span>
<span data-ttu-id="1e2e9-131">Задает значение переменной.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-131">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2e9-132">CommonParameters</span></span>
<span data-ttu-id="1e2e9-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2e9-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e2e9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2e9-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e2e9-135">INPUTS</span></span>

### <span data-ttu-id="1e2e9-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="1e2e9-136">None</span></span>
<span data-ttu-id="1e2e9-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1e2e9-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e2e9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e2e9-138">OUTPUTS</span></span>

### <span data-ttu-id="1e2e9-139">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="1e2e9-139">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="1e2e9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e2e9-140">NOTES</span></span>

## <span data-ttu-id="1e2e9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e2e9-141">RELATED LINKS</span></span>

[<span data-ttu-id="1e2e9-142">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1e2e9-142">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="1e2e9-143">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1e2e9-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="1e2e9-144">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1e2e9-144">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


