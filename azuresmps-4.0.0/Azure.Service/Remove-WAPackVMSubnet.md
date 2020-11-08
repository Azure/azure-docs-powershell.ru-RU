---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077407"
---
# <span data-ttu-id="127ea-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="127ea-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="127ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="127ea-102">SYNOPSIS</span></span>
<span data-ttu-id="127ea-103">Удаляет объекты подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="127ea-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="127ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="127ea-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="127ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="127ea-105">DESCRIPTION</span></span>
<span data-ttu-id="127ea-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="127ea-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="127ea-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="127ea-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="127ea-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="127ea-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="127ea-109">Командлет **Remove-WAPackVMSubnet** удаляет объекты подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="127ea-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="127ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="127ea-110">EXAMPLES</span></span>

### <span data-ttu-id="127ea-111">Пример 1: Удаление подсети виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="127ea-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="127ea-112">Первая команда получает подсеть виртуальной машины с именем ContosoVMSubnet01 с помощью командлета **Get-WAPackVMSubnet** и сохраняет этот объект в переменной $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="127ea-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="127ea-113">Вторая команда удаляет подсеть виртуальной машины, хранящуюся в $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="127ea-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="127ea-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="127ea-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="127ea-115">Пример 2: Удаление виртуальной машины без подтверждения</span><span class="sxs-lookup"><span data-stu-id="127ea-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="127ea-116">Первая команда получает облачную службу с именем ContosoVMSubnet02 с помощью командлета **Get-WAPackVMSubnet** , а затем сохраняет этот объект в переменной $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="127ea-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="127ea-117">Вторая команда удаляет подсеть виртуальной машины, хранящуюся в $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="127ea-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="127ea-118">Эта команда включает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="127ea-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="127ea-119">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="127ea-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="127ea-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="127ea-120">PARAMETERS</span></span>

### <span data-ttu-id="127ea-121">-Force</span><span class="sxs-lookup"><span data-stu-id="127ea-121">-Force</span></span>
<span data-ttu-id="127ea-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="127ea-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="127ea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="127ea-123">-PassThru</span></span>
<span data-ttu-id="127ea-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="127ea-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="127ea-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="127ea-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="127ea-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="127ea-126">-Profile</span></span>
<span data-ttu-id="127ea-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="127ea-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="127ea-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="127ea-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="127ea-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="127ea-129">-VMSubnet</span></span>
<span data-ttu-id="127ea-130">Указывает подсеть виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="127ea-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="127ea-131">Чтобы получить подсеть виртуальной машины, используйте командлет **Get-WAPackVMSubnet** .</span><span class="sxs-lookup"><span data-stu-id="127ea-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="127ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127ea-132">CommonParameters</span></span>
<span data-ttu-id="127ea-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="127ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127ea-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="127ea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127ea-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="127ea-135">INPUTS</span></span>

## <span data-ttu-id="127ea-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="127ea-136">OUTPUTS</span></span>

## <span data-ttu-id="127ea-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="127ea-137">NOTES</span></span>

## <span data-ttu-id="127ea-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="127ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="127ea-139">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="127ea-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="127ea-140">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="127ea-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


