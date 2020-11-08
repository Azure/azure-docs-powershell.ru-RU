---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077431"
---
# <span data-ttu-id="8f7c5-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="8f7c5-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="8f7c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7c5-103">Получает объекты пула статических IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="8f7c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f7c5-104">SYNTAX</span></span>

### <span data-ttu-id="8f7c5-105">FromVMSubnetObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f7c5-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8f7c5-106">FromName</span><span class="sxs-lookup"><span data-stu-id="8f7c5-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f7c5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f7c5-107">DESCRIPTION</span></span>
<span data-ttu-id="8f7c5-108">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8f7c5-109">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8f7c5-110">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8f7c5-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8f7c5-111">Командлет **Get-WAPackStaticIPAddressPool** получает статические объекты пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="8f7c5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f7c5-112">EXAMPLES</span></span>

### <span data-ttu-id="8f7c5-113">Пример 1: получение статического пула IP-адресов из заданной подсети VMSubnet</span><span class="sxs-lookup"><span data-stu-id="8f7c5-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="8f7c5-114">Эта команда получает пул статических IP-адресов с именем ContosoStaticIPAddressPool01 из заданной подсети VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="8f7c5-115">Пример 2: получение всех пулов статических IP-адресов из данной подсети VMSubnet</span><span class="sxs-lookup"><span data-stu-id="8f7c5-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="8f7c5-116">Эта команда получает список всех статических IP-пулов из указанного VMSubet.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="8f7c5-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f7c5-117">PARAMETERS</span></span>

### <span data-ttu-id="8f7c5-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f7c5-118">-Name</span></span>
<span data-ttu-id="8f7c5-119">Указывает имя пула статических IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-119">Specifies the name of a static IP address pool.</span></span>

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

### <span data-ttu-id="8f7c5-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="8f7c5-120">-Profile</span></span>
<span data-ttu-id="8f7c5-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f7c5-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f7c5-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="8f7c5-123">-VMSubnet</span></span>
<span data-ttu-id="8f7c5-124">Указывает объект **VMSubnet** , связанный со статическим ПУЛОМ IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

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

### <span data-ttu-id="8f7c5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7c5-125">CommonParameters</span></span>
<span data-ttu-id="8f7c5-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7c5-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7c5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7c5-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f7c5-128">INPUTS</span></span>

## <span data-ttu-id="8f7c5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f7c5-129">OUTPUTS</span></span>

## <span data-ttu-id="8f7c5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f7c5-130">NOTES</span></span>

## <span data-ttu-id="8f7c5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f7c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="8f7c5-132">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="8f7c5-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="8f7c5-133">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="8f7c5-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


