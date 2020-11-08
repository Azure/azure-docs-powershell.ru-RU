---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076068"
---
# <span data-ttu-id="3d220-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3d220-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="3d220-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d220-102">SYNOPSIS</span></span>

<span data-ttu-id="3d220-103">Изменяет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3d220-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="3d220-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d220-104">SYNTAX</span></span>

### <span data-ttu-id="3d220-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="3d220-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d220-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="3d220-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d220-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d220-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3d220-108">Командлет **Set-AzureAutomationVariable** изменяет значение или описание переменной в Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3d220-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="3d220-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d220-109">EXAMPLES</span></span>

### <span data-ttu-id="3d220-110">Пример 1: Установка значения переменной</span><span class="sxs-lookup"><span data-stu-id="3d220-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="3d220-111">Эта команда задает новое значение переменной с именем MyStringVariable в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3d220-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3d220-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d220-112">PARAMETERS</span></span>

### <span data-ttu-id="3d220-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d220-113">-AutomationAccountName</span></span>
<span data-ttu-id="3d220-114">Указывает имя учетной записи автоматизации с переменной.</span><span class="sxs-lookup"><span data-stu-id="3d220-114">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="3d220-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="3d220-115">-Description</span></span>
<span data-ttu-id="3d220-116">Задает описание переменной.</span><span class="sxs-lookup"><span data-stu-id="3d220-116">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d220-117">С шифрованием</span><span class="sxs-lookup"><span data-stu-id="3d220-117">-Encrypted</span></span>
<span data-ttu-id="3d220-118">Указывает, следует ли шифровать переменную.</span><span class="sxs-lookup"><span data-stu-id="3d220-118">Indicates whether to encrypt the variable.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d220-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d220-119">-Name</span></span>
<span data-ttu-id="3d220-120">Указывает имя переменной.</span><span class="sxs-lookup"><span data-stu-id="3d220-120">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="3d220-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d220-121">-Profile</span></span>
<span data-ttu-id="3d220-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d220-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d220-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d220-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d220-124">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="3d220-124">-Value</span></span>
<span data-ttu-id="3d220-125">Задает значение переменной.</span><span class="sxs-lookup"><span data-stu-id="3d220-125">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d220-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d220-126">CommonParameters</span></span>
<span data-ttu-id="3d220-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d220-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d220-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d220-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d220-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d220-129">INPUTS</span></span>

## <span data-ttu-id="3d220-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d220-130">OUTPUTS</span></span>

### <span data-ttu-id="3d220-131">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="3d220-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="3d220-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d220-132">NOTES</span></span>

## <span data-ttu-id="3d220-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d220-133">RELATED LINKS</span></span>

[<span data-ttu-id="3d220-134">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3d220-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="3d220-135">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3d220-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="3d220-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3d220-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


