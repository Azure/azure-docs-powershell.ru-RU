---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 08A7556E-C07F-4B3B-B9D6-B241C72860FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b01ac318982b62499164cd54c9d9a51356ad9830
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077385"
---
# <span data-ttu-id="8614f-101">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8614f-101">Set-WAPackVM</span></span>

## <span data-ttu-id="8614f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8614f-102">SYNOPSIS</span></span>
<span data-ttu-id="8614f-103">Изменение свойств размера виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8614f-103">Changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="8614f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8614f-104">SYNTAX</span></span>

```
Set-WAPackVM -VM <VirtualMachine> -VMSizeProfile <HardwareProfile> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8614f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8614f-105">DESCRIPTION</span></span>
<span data-ttu-id="8614f-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="8614f-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8614f-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8614f-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8614f-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8614f-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8614f-109">Командлет **Set-WAPackVM** изменяет свойства размера виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8614f-109">The **Set-WAPackVM** cmdlet changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="8614f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8614f-110">EXAMPLES</span></span>

### <span data-ttu-id="8614f-111">Пример 1: указание размера виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="8614f-111">Example 1: Specify the size for a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> Set-WAPackVM -VM $VirtualMachine -VMSizeProfile $SizeProfile
```

<span data-ttu-id="8614f-112">Первая команда получает виртуальную машину с именем ContosoV126 с помощью командлета **Get-WAPackVM** , а затем сохраняет этот объект в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8614f-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="8614f-113">Вторая команда получает профиль размера с именем MediumSizeVM с помощью командлета **Get-WAPackVMSizeProfile** , а затем сохраняет этот объект в переменной $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="8614f-113">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores that object in the $SizeProfile variable.</span></span>

<span data-ttu-id="8614f-114">Последняя команда назначает профиль размера, хранящийся в $SizeProfile, виртуальной машине, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8614f-114">The final command assigns the size profile stored in $SizeProfile to the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="8614f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8614f-115">PARAMETERS</span></span>

### <span data-ttu-id="8614f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8614f-116">-PassThru</span></span>
<span data-ttu-id="8614f-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8614f-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8614f-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8614f-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8614f-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="8614f-119">-Profile</span></span>
<span data-ttu-id="8614f-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8614f-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8614f-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8614f-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8614f-122">-VM</span><span class="sxs-lookup"><span data-stu-id="8614f-122">-VM</span></span>
<span data-ttu-id="8614f-123">Указывает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="8614f-123">Specifies a virtual machine.</span></span>
<span data-ttu-id="8614f-124">Чтобы получить виртуальную машину, используйте командлет **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="8614f-124">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="8614f-125">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="8614f-125">-VMSizeProfile</span></span>
<span data-ttu-id="8614f-126">Задает в качестве объекта **HardwareProfile** профиль размера для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8614f-126">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="8614f-127">Чтобы получить профиль размера, используйте командлет **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="8614f-127">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8614f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8614f-128">CommonParameters</span></span>
<span data-ttu-id="8614f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8614f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8614f-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8614f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8614f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8614f-131">INPUTS</span></span>

## <span data-ttu-id="8614f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8614f-132">OUTPUTS</span></span>

## <span data-ttu-id="8614f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8614f-133">NOTES</span></span>

## <span data-ttu-id="8614f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8614f-134">RELATED LINKS</span></span>

[<span data-ttu-id="8614f-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8614f-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="8614f-136">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8614f-136">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="8614f-137">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8614f-137">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="8614f-138">Restarting-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8614f-138">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="8614f-139">Возобновить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8614f-139">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="8614f-140">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8614f-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="8614f-141">Остановить-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8614f-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="8614f-142">Приостановить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8614f-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="8614f-143">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="8614f-143">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)


