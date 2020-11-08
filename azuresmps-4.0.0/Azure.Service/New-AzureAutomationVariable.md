---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075931"
---
# <span data-ttu-id="a18a4-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a18a4-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="a18a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a18a4-102">SYNOPSIS</span></span>

<span data-ttu-id="a18a4-103">Создает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a18a4-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="a18a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a18a4-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a18a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a18a4-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a18a4-106">Командлет **New-AzureAutomationVariable** создает переменную в службе автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a18a4-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="a18a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a18a4-107">EXAMPLES</span></span>

### <span data-ttu-id="a18a4-108">Пример 1: создание новой переменной с простым значением</span><span class="sxs-lookup"><span data-stu-id="a18a4-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="a18a4-109">Эта команда создает новую переменную с именем MyStringVariable и строковое значение в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a18a4-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="a18a4-110">Пример 2: создание новой переменной со сложным значением</span><span class="sxs-lookup"><span data-stu-id="a18a4-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="a18a4-111">Эти команды создают новую переменную с именем MyComplexVariable в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a18a4-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="a18a4-112">Для его значения используется сложный объект, в данном случае объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a18a4-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="a18a4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a18a4-113">PARAMETERS</span></span>

### <span data-ttu-id="a18a4-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a18a4-114">-AutomationAccountName</span></span>
<span data-ttu-id="a18a4-115">Указывает имя учетной записи автоматизации, в которой будет храниться переменная.</span><span class="sxs-lookup"><span data-stu-id="a18a4-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18a4-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="a18a4-116">-Description</span></span>
<span data-ttu-id="a18a4-117">Задает описание переменной.</span><span class="sxs-lookup"><span data-stu-id="a18a4-117">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="a18a4-118">С шифрованием</span><span class="sxs-lookup"><span data-stu-id="a18a4-118">-Encrypted</span></span>
<span data-ttu-id="a18a4-119">Указывает, следует ли хранить значение переменной в зашифрованном виде.</span><span class="sxs-lookup"><span data-stu-id="a18a4-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

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

### <span data-ttu-id="a18a4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a18a4-120">-Name</span></span>
<span data-ttu-id="a18a4-121">Задает имя переменной.</span><span class="sxs-lookup"><span data-stu-id="a18a4-121">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a18a4-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="a18a4-122">-Profile</span></span>
<span data-ttu-id="a18a4-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a18a4-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a18a4-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a18a4-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18a4-125">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="a18a4-125">-Value</span></span>
<span data-ttu-id="a18a4-126">Указывает значение, которое нужно сохранить в переменной.</span><span class="sxs-lookup"><span data-stu-id="a18a4-126">Specifies a value to store in the variable.</span></span>

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

### <span data-ttu-id="a18a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18a4-127">CommonParameters</span></span>
<span data-ttu-id="a18a4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a18a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18a4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a18a4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18a4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a18a4-130">INPUTS</span></span>

## <span data-ttu-id="a18a4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a18a4-131">OUTPUTS</span></span>

### <span data-ttu-id="a18a4-132">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="a18a4-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="a18a4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a18a4-133">NOTES</span></span>

## <span data-ttu-id="a18a4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a18a4-134">RELATED LINKS</span></span>

[<span data-ttu-id="a18a4-135">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a18a4-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="a18a4-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a18a4-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="a18a4-137">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a18a4-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


