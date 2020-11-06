---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: c2e03cae02c776b69c424ea3ff685a4118ed94bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566332"
---
# <span data-ttu-id="f7a7a-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f7a7a-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="f7a7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a7a-103">Создает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7a7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7a7a-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7a7a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="f7a7a-106">Командлет **New-AzureRmAutomationVariable** создает переменную в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="f7a7a-107">Чтобы зашифровать переменную, укажите *зашифрованный* параметр.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="f7a7a-108">После создания переменной невозможно изменить зашифрованное состояние.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="f7a7a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7a7a-109">EXAMPLES</span></span>

### <span data-ttu-id="f7a7a-110">Пример 1: создание переменной с простым значением</span><span class="sxs-lookup"><span data-stu-id="f7a7a-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f7a7a-111">Эта команда создает переменную с именем StringVariable22, которая имеет строковое значение в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f7a7a-112">Пример 2: создание переменной со сложным значением</span><span class="sxs-lookup"><span data-stu-id="f7a7a-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f7a7a-113">Первая команда получает виртуальную машину с помощью командлета Get-AzureVM.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="f7a7a-114">Команда сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="f7a7a-115">Вторая команда создает переменную с именем ComplexVariable01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f7a7a-116">Эта команда использует сложный объект для его значения (в данном случае — виртуальная машина в $VirtualMachine).</span><span class="sxs-lookup"><span data-stu-id="f7a7a-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="f7a7a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7a7a-117">PARAMETERS</span></span>

### <span data-ttu-id="f7a7a-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f7a7a-118">-AutomationAccountName</span></span>
<span data-ttu-id="f7a7a-119">Указывает имя учетной записи автоматизации, в которой будет храниться переменная.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="f7a7a-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="f7a7a-120">-Description</span></span>
<span data-ttu-id="f7a7a-121">Задает описание переменной.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="f7a7a-122">С шифрованием</span><span class="sxs-lookup"><span data-stu-id="f7a7a-122">-Encrypted</span></span>
<span data-ttu-id="f7a7a-123">Указывает, шифрует ли этот командлет значение переменной для хранения.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-123">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="f7a7a-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7a7a-124">-Name</span></span>
<span data-ttu-id="f7a7a-125">Задает имя переменной.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-125">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="f7a7a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7a7a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7a7a-127">Указывает группу ресурсов, для которой этот командлет создает переменную.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-127">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="f7a7a-128">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="f7a7a-128">-Value</span></span>
<span data-ttu-id="f7a7a-129">Задает значение переменной.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="f7a7a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a7a-130">-DefaultProfile</span></span>
<span data-ttu-id="f7a7a-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7a7a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a7a-132">CommonParameters</span></span>
<span data-ttu-id="f7a7a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a7a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7a7a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a7a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7a7a-135">INPUTS</span></span>

## <span data-ttu-id="f7a7a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7a7a-136">OUTPUTS</span></span>

### <span data-ttu-id="f7a7a-137">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="f7a7a-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f7a7a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7a7a-138">NOTES</span></span>

## <span data-ttu-id="f7a7a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7a7a-139">RELATED LINKS</span></span>

[<span data-ttu-id="f7a7a-140">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f7a7a-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="f7a7a-141">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f7a7a-141">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="f7a7a-142">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f7a7a-142">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


