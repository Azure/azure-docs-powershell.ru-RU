---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 80820C11-92BB-4E75-8722-496CF21C779E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a92ff041f5a3eb245b76501e7758ca62b24887f9
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077387"
---
# <span data-ttu-id="91cca-101">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="91cca-101">Restart-WAPackVM</span></span>

## <span data-ttu-id="91cca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91cca-102">SYNOPSIS</span></span>
<span data-ttu-id="91cca-103">Перезапускает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="91cca-103">Restarts virtual machines.</span></span>

## <span data-ttu-id="91cca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91cca-104">SYNTAX</span></span>

```
Restart-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="91cca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91cca-105">DESCRIPTION</span></span>
<span data-ttu-id="91cca-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="91cca-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="91cca-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91cca-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="91cca-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="91cca-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="91cca-109">Командлет **restarting-WAPackVM** перезапускает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="91cca-109">The **Restart-WAPackVM** cmdlet restarts virtual machines.</span></span>

## <span data-ttu-id="91cca-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91cca-110">EXAMPLES</span></span>

### <span data-ttu-id="91cca-111">Пример 1: перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="91cca-111">Example 1: Restart a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Restart-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="91cca-112">Первая команда получает виртуальную машину с именем ContosoV126 с помощью командлета **Get-WAPackVM** , а затем сохраняет этот объект в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="91cca-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="91cca-113">Вторая команда перезапускает виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="91cca-113">The second command restarts the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="91cca-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91cca-114">PARAMETERS</span></span>

### <span data-ttu-id="91cca-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91cca-115">-PassThru</span></span>
<span data-ttu-id="91cca-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="91cca-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="91cca-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="91cca-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="91cca-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="91cca-118">-Profile</span></span>
<span data-ttu-id="91cca-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="91cca-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91cca-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91cca-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91cca-121">-VM</span><span class="sxs-lookup"><span data-stu-id="91cca-121">-VM</span></span>
<span data-ttu-id="91cca-122">Указывает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="91cca-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="91cca-123">Чтобы получить виртуальную машину, используйте командлет **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="91cca-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="91cca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cca-124">CommonParameters</span></span>
<span data-ttu-id="91cca-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91cca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cca-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91cca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cca-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91cca-127">INPUTS</span></span>

## <span data-ttu-id="91cca-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91cca-128">OUTPUTS</span></span>

## <span data-ttu-id="91cca-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="91cca-129">NOTES</span></span>

## <span data-ttu-id="91cca-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91cca-130">RELATED LINKS</span></span>

[<span data-ttu-id="91cca-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="91cca-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="91cca-132">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="91cca-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="91cca-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="91cca-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="91cca-134">Возобновить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="91cca-134">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="91cca-135">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="91cca-135">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="91cca-136">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="91cca-136">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="91cca-137">Остановить-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="91cca-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="91cca-138">Приостановить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="91cca-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


