---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4FB7096E-DDA1-474C-BF0C-D910681BE58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4ef4660761ab29e738050c0445534602accda6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077396"
---
# <span data-ttu-id="4e83c-101">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4e83c-101">Stop-WAPackVM</span></span>

## <span data-ttu-id="4e83c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e83c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e83c-103">Остановка виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e83c-103">Stops a virtual machine.</span></span>

## <span data-ttu-id="4e83c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e83c-104">SYNTAX</span></span>

```
Stop-WAPackVM [-Shutdown] -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4e83c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e83c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e83c-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="4e83c-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="4e83c-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e83c-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4e83c-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4e83c-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4e83c-109">Командлет **Stop-WAPackVM** останавливает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="4e83c-109">The **Stop-WAPackVM** cmdlet stops a virtual machine.</span></span>

## <span data-ttu-id="4e83c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e83c-110">EXAMPLES</span></span>

### <span data-ttu-id="4e83c-111">Пример 1: остановка виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="4e83c-111">Example 1: Stop a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Stop-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="4e83c-112">Первая команда получает виртуальную машину с именем ContosoV126 с помощью командлета **Get-WAPackVM** , а затем сохраняет этот объект в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4e83c-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="4e83c-113">Вторая команда останавливает работу виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4e83c-113">The second command stops the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="4e83c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e83c-114">PARAMETERS</span></span>

### <span data-ttu-id="4e83c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e83c-115">-PassThru</span></span>
<span data-ttu-id="4e83c-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="4e83c-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4e83c-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4e83c-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e83c-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="4e83c-118">-Profile</span></span>
<span data-ttu-id="4e83c-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4e83c-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4e83c-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4e83c-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4e83c-121">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="4e83c-121">-Shutdown</span></span>
<span data-ttu-id="4e83c-122">Указывает, что командлет завершает работу операционной системы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e83c-122">Indicates that the cmdlet shuts down the operating system of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e83c-123">-VM</span><span class="sxs-lookup"><span data-stu-id="4e83c-123">-VM</span></span>
<span data-ttu-id="4e83c-124">Указывает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="4e83c-124">Specifies a virtual machine.</span></span>
<span data-ttu-id="4e83c-125">Чтобы получить виртуальную машину, используйте командлет **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="4e83c-125">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e83c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e83c-126">CommonParameters</span></span>
<span data-ttu-id="4e83c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e83c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e83c-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e83c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e83c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e83c-129">INPUTS</span></span>

## <span data-ttu-id="4e83c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e83c-130">OUTPUTS</span></span>

## <span data-ttu-id="4e83c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e83c-131">NOTES</span></span>

## <span data-ttu-id="4e83c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e83c-132">RELATED LINKS</span></span>

[<span data-ttu-id="4e83c-133">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4e83c-133">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="4e83c-134">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4e83c-134">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="4e83c-135">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4e83c-135">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="4e83c-136">Restarting-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4e83c-136">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="4e83c-137">Возобновить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4e83c-137">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="4e83c-138">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4e83c-138">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="4e83c-139">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4e83c-139">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="4e83c-140">Приостановить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="4e83c-140">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


