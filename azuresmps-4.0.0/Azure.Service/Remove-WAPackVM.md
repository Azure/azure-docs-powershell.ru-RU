---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077408"
---
# <span data-ttu-id="f7a91-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f7a91-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="f7a91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7a91-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a91-103">Удаление объектов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7a91-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="f7a91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7a91-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7a91-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7a91-105">DESCRIPTION</span></span>
<span data-ttu-id="f7a91-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="f7a91-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="f7a91-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7a91-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f7a91-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f7a91-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f7a91-109">Командлет **Remove-WAPackVM** удаляет объекты виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7a91-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="f7a91-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7a91-110">EXAMPLES</span></span>

### <span data-ttu-id="f7a91-111">Пример 1: Удаление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f7a91-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="f7a91-112">Первая команда получает виртуальную машину с именем ContosoV126 с помощью командлета **Get-WAPackVM** , а затем сохраняет этот объект в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f7a91-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="f7a91-113">Вторая команда удаляет виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f7a91-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="f7a91-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f7a91-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="f7a91-115">Пример 2: Удаление виртуальной машины без подтверждения</span><span class="sxs-lookup"><span data-stu-id="f7a91-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="f7a91-116">Первая команда получает виртуальную машину с именем ContosoV126 с помощью командлета **Get-WAPackVM** , а затем сохраняет этот объект в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f7a91-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="f7a91-117">Вторая команда удаляет виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f7a91-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="f7a91-118">Эта команда включает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="f7a91-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="f7a91-119">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f7a91-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f7a91-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7a91-120">PARAMETERS</span></span>

### <span data-ttu-id="f7a91-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f7a91-121">-Force</span></span>
<span data-ttu-id="f7a91-122">Указывает, что командлет удаляет виртуальную машину без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f7a91-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f7a91-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7a91-123">-PassThru</span></span>
<span data-ttu-id="f7a91-124">Указывает на то, что командлет возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="f7a91-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="f7a91-125">Если операция выполнена успешно, командлет возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="f7a91-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="f7a91-126">В противном случае возвращается значение $False.</span><span class="sxs-lookup"><span data-stu-id="f7a91-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="f7a91-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f7a91-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f7a91-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="f7a91-128">-Profile</span></span>
<span data-ttu-id="f7a91-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f7a91-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f7a91-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f7a91-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f7a91-131">-VM</span><span class="sxs-lookup"><span data-stu-id="f7a91-131">-VM</span></span>
<span data-ttu-id="f7a91-132">Указывает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f7a91-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="f7a91-133">Чтобы получить виртуальную машину, используйте командлет **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="f7a91-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="f7a91-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7a91-134">-Confirm</span></span>
<span data-ttu-id="f7a91-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7a91-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a91-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7a91-136">-WhatIf</span></span>
<span data-ttu-id="f7a91-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7a91-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7a91-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7a91-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a91-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a91-139">CommonParameters</span></span>
<span data-ttu-id="f7a91-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7a91-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a91-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7a91-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a91-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7a91-142">INPUTS</span></span>

## <span data-ttu-id="f7a91-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7a91-143">OUTPUTS</span></span>

## <span data-ttu-id="f7a91-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7a91-144">NOTES</span></span>

## <span data-ttu-id="f7a91-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7a91-145">RELATED LINKS</span></span>

[<span data-ttu-id="f7a91-146">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f7a91-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="f7a91-147">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f7a91-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="f7a91-148">Restarting-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f7a91-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="f7a91-149">Возобновить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f7a91-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="f7a91-150">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f7a91-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="f7a91-151">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f7a91-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="f7a91-152">Остановить-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f7a91-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="f7a91-153">Приостановить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f7a91-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


