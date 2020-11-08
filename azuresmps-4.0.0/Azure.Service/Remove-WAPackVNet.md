---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077406"
---
# <span data-ttu-id="9f8df-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="9f8df-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="9f8df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f8df-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8df-103">Удаление объектов виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9f8df-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="9f8df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f8df-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9f8df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f8df-105">DESCRIPTION</span></span>
<span data-ttu-id="9f8df-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="9f8df-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9f8df-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9f8df-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9f8df-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9f8df-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9f8df-109">Командлет **Remove-WAPackVNet** удаляет объекты виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9f8df-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="9f8df-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f8df-110">EXAMPLES</span></span>

### <span data-ttu-id="9f8df-111">Пример 1: удаление виртуализированной сети</span><span class="sxs-lookup"><span data-stu-id="9f8df-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="9f8df-112">Первая команда получает виртуальную сеть с именем ContosoVNet01 с помощью командлета **Get-WAPackVNet** , а затем сохраняет этот объект в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="9f8df-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="9f8df-113">Вторая команда удаляет виртуализированную сеть, хранящуюся в $VNet.</span><span class="sxs-lookup"><span data-stu-id="9f8df-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="9f8df-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9f8df-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="9f8df-115">Пример 2: удаление виртуализированной сети без подтверждения</span><span class="sxs-lookup"><span data-stu-id="9f8df-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="9f8df-116">Первая команда получает облачную службу с именем ContosoVNet02 с помощью командлета **Get-WAPackVNet** , а затем сохраняет этот объект в переменной $VNet.</span><span class="sxs-lookup"><span data-stu-id="9f8df-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="9f8df-117">Вторая команда удаляет виртуализированную сеть, хранящуюся в $VNet.</span><span class="sxs-lookup"><span data-stu-id="9f8df-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="9f8df-118">Эта команда включает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="9f8df-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="9f8df-119">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9f8df-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9f8df-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f8df-120">PARAMETERS</span></span>

### <span data-ttu-id="9f8df-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9f8df-121">-Force</span></span>
<span data-ttu-id="9f8df-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9f8df-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f8df-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f8df-123">-PassThru</span></span>
<span data-ttu-id="9f8df-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9f8df-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9f8df-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9f8df-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f8df-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="9f8df-126">-Profile</span></span>
<span data-ttu-id="9f8df-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9f8df-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9f8df-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9f8df-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9f8df-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="9f8df-129">-VNet</span></span>
<span data-ttu-id="9f8df-130">Указывает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="9f8df-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="9f8df-131">Чтобы получить виртуальную сеть, используйте командлет **Get-WAPackVNet** .</span><span class="sxs-lookup"><span data-stu-id="9f8df-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f8df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8df-132">CommonParameters</span></span>
<span data-ttu-id="9f8df-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f8df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8df-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f8df-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8df-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f8df-135">INPUTS</span></span>

## <span data-ttu-id="9f8df-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f8df-136">OUTPUTS</span></span>

## <span data-ttu-id="9f8df-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f8df-137">NOTES</span></span>

## <span data-ttu-id="9f8df-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f8df-138">RELATED LINKS</span></span>

[<span data-ttu-id="9f8df-139">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="9f8df-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="9f8df-140">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="9f8df-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


