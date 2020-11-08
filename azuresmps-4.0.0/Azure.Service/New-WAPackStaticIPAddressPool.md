---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077381"
---
# <span data-ttu-id="743d3-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="743d3-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="743d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="743d3-102">SYNOPSIS</span></span>
<span data-ttu-id="743d3-103">Создание статического пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="743d3-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="743d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="743d3-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="743d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="743d3-105">DESCRIPTION</span></span>
<span data-ttu-id="743d3-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="743d3-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="743d3-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="743d3-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="743d3-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="743d3-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="743d3-109">Командлет **New-WAPackStaticIPAddressPool** создает статический пул IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="743d3-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="743d3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="743d3-110">EXAMPLES</span></span>

### <span data-ttu-id="743d3-111">Пример 1: Создание статического пула IP-адресов</span><span class="sxs-lookup"><span data-stu-id="743d3-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="743d3-112">Первая команда сначала извлекает сеть виртуальной машины, к которой нужно добавить статический пул IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="743d3-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="743d3-113">Эта сеть виртуальной машины называется ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="743d3-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="743d3-114">Вторая команда использует ранее извлеченную сеть виртуальной машины для получения подсети виртуальной машины с именем ContosoVMSubnet01, к которой нужно добавить статический пул IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="743d3-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="743d3-115">Последняя команда создает новый пул статических IP-адресов с именем ContosoStaticIpAddressPool01, а диапазон Start — 192.168.1.0 и End 192.168.1.10 диапазона.</span><span class="sxs-lookup"><span data-stu-id="743d3-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="743d3-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="743d3-116">PARAMETERS</span></span>

### <span data-ttu-id="743d3-117">-IPAddressRangeEnd</span><span class="sxs-lookup"><span data-stu-id="743d3-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="743d3-118">Указывает конец диапазона IP-адресов для пула статических IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="743d3-118">Specifies an IP address range end for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743d3-119">-IPAddressRangeStart</span><span class="sxs-lookup"><span data-stu-id="743d3-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="743d3-120">Задает начало диапазона IP-адресов для пула статических IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="743d3-120">Specifies an IP address range start for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743d3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="743d3-121">-Name</span></span>
<span data-ttu-id="743d3-122">Задает имя пула статических IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="743d3-122">Specifies a name for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743d3-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="743d3-123">-Profile</span></span>
<span data-ttu-id="743d3-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="743d3-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="743d3-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="743d3-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="743d3-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="743d3-126">-VMSubnet</span></span>
<span data-ttu-id="743d3-127">Указывает подсеть VMSubnet, связанную с пулом статических IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="743d3-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

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

### <span data-ttu-id="743d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743d3-128">CommonParameters</span></span>
<span data-ttu-id="743d3-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="743d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743d3-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743d3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743d3-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="743d3-131">INPUTS</span></span>

## <span data-ttu-id="743d3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="743d3-132">OUTPUTS</span></span>

## <span data-ttu-id="743d3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="743d3-133">NOTES</span></span>

## <span data-ttu-id="743d3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="743d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="743d3-135">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="743d3-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="743d3-136">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="743d3-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


