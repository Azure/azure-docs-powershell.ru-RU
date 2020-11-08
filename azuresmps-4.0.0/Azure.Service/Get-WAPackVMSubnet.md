---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077355"
---
# <span data-ttu-id="633c7-101">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="633c7-101">Get-WAPackVMSubnet</span></span>

## <span data-ttu-id="633c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="633c7-102">SYNOPSIS</span></span>
<span data-ttu-id="633c7-103">Получает объекты подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="633c7-103">Gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="633c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="633c7-104">SYNTAX</span></span>

### <span data-ttu-id="633c7-105">FromVMNetworkObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="633c7-105">FromVMNetworkObject (Default)</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="633c7-106">FromName</span><span class="sxs-lookup"><span data-stu-id="633c7-106">FromName</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="633c7-107">FromId</span><span class="sxs-lookup"><span data-stu-id="633c7-107">FromId</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="633c7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="633c7-108">DESCRIPTION</span></span>
<span data-ttu-id="633c7-109">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="633c7-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="633c7-110">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="633c7-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="633c7-111">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="633c7-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="633c7-112">Командлет **Get-WAPackVMSubnet** получает объекты подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="633c7-112">The **Get-WAPackVMSubnet** cmdlet gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="633c7-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="633c7-113">EXAMPLES</span></span>

### <span data-ttu-id="633c7-114">Пример 1: получение подсети виртуальной машины с помощью имени</span><span class="sxs-lookup"><span data-stu-id="633c7-114">Example 1: Get a virtual machine subnet by using a name</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

<span data-ttu-id="633c7-115">Эта команда получает подсеть виртуальной машины с именем ContosoSubnet01.</span><span class="sxs-lookup"><span data-stu-id="633c7-115">This command gets the virtual machine subnet named ContosoSubnet01.</span></span>

### <span data-ttu-id="633c7-116">Пример 2: получение подсети виртуальной машины с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="633c7-116">Example 2: Get a virtual machine subnet by using an ID</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="633c7-117">Эта команда получает подсеть виртуальной машины с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="633c7-117">This command gets the virtual machine subnet that has the specified ID.</span></span>

### <span data-ttu-id="633c7-118">Пример 3: получение всех подсетей виртуальной машины из данной виртуализированной сети</span><span class="sxs-lookup"><span data-stu-id="633c7-118">Example 3: Get all virtual machine subnets from a given virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

<span data-ttu-id="633c7-119">Эта команда получает все подсети виртуальной машины из данной виртуализированной сети.</span><span class="sxs-lookup"><span data-stu-id="633c7-119">This command gets all the virtual machine subnets from a given virtualized network.</span></span>

## <span data-ttu-id="633c7-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="633c7-120">PARAMETERS</span></span>

### <span data-ttu-id="633c7-121">-ID</span><span class="sxs-lookup"><span data-stu-id="633c7-121">-ID</span></span>
<span data-ttu-id="633c7-122">Указывает уникальный идентификатор подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="633c7-122">Specifies the unique ID of a virtual machine subnet.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633c7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="633c7-123">-Name</span></span>
<span data-ttu-id="633c7-124">Указывает имя подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="633c7-124">Specifies the name of a virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633c7-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="633c7-125">-Profile</span></span>
<span data-ttu-id="633c7-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="633c7-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="633c7-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="633c7-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="633c7-128">-VNet</span><span class="sxs-lookup"><span data-stu-id="633c7-128">-VNet</span></span>
<span data-ttu-id="633c7-129">Указывает виртуальную сеть, связанную с подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="633c7-129">Specifies the VNet associated with a virtual machine subnet.</span></span>

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

### <span data-ttu-id="633c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633c7-130">CommonParameters</span></span>
<span data-ttu-id="633c7-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="633c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633c7-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="633c7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633c7-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="633c7-133">INPUTS</span></span>

## <span data-ttu-id="633c7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="633c7-134">OUTPUTS</span></span>

## <span data-ttu-id="633c7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="633c7-135">NOTES</span></span>

## <span data-ttu-id="633c7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="633c7-136">RELATED LINKS</span></span>

[<span data-ttu-id="633c7-137">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="633c7-137">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="633c7-138">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="633c7-138">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)

[<span data-ttu-id="633c7-139">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="633c7-139">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


