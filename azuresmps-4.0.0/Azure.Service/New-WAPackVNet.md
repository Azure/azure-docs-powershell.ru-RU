---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CB2936E4-E403-44B3-9CB8-617308E54C50
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9059e5bad8441f25846cf98a12c5e8dada2e814a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077397"
---
# <span data-ttu-id="ce8cb-101">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="ce8cb-101">New-WAPackVNet</span></span>

## <span data-ttu-id="ce8cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8cb-103">Создание виртуализированной сети.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-103">Creates a virtualized network.</span></span>

## <span data-ttu-id="ce8cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce8cb-104">SYNTAX</span></span>

```
New-WAPackVNet -LogicalNetwork <LogicalNetwork> -Name <String> [-Description <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ce8cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce8cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ce8cb-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ce8cb-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ce8cb-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ce8cb-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ce8cb-109">Командлет **New-WAPackVNet** создает виртуализированную сеть.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-109">The **New-WAPackVNet** cmdlet creates a virtualized network.</span></span>

## <span data-ttu-id="ce8cb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce8cb-110">EXAMPLES</span></span>

### <span data-ttu-id="ce8cb-111">Пример 1: создание виртуализированной сети</span><span class="sxs-lookup"><span data-stu-id="ce8cb-111">Example 1: Create a virtualized network</span></span>
```
PS C:\> $LogicalNetwork = Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
PS C:\> New-WAPackVNet -LogicalNetwork $LogicalNetwork -Name "ContosoVNett01" -Description "A description"
```

<span data-ttu-id="ce8cb-112">Первая команда сначала извлекает логическую сеть, к которой требуется добавить новую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-112">The first command first retrieves the logical network to which we want to add a new virtualized network.</span></span>
<span data-ttu-id="ce8cb-113">Эта логическая сеть называется ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-113">This logical network is named ContosoLogicalNetwork01.</span></span>

<span data-ttu-id="ce8cb-114">Вторая и последняя команды создают виртуализованную сеть, используя ранее извлеченную логическую сеть, имя (ContosoVNett01) и описание (описание).</span><span class="sxs-lookup"><span data-stu-id="ce8cb-114">The second and last command creates a virtualized network using the previously retrieved logical network, a name (ContosoVNett01) and a description (A description).</span></span>

## <span data-ttu-id="ce8cb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce8cb-115">PARAMETERS</span></span>

### <span data-ttu-id="ce8cb-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="ce8cb-116">-Description</span></span>
<span data-ttu-id="ce8cb-117">Задает описание виртуализированной сети.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-117">Specifies a description for the virtualized network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8cb-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="ce8cb-118">-LogicalNetwork</span></span>
<span data-ttu-id="ce8cb-119">Указывает LogicalNetwork, связанный с виртуализированной сетью.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-119">Specifies a LogicalNetwork associated with the virtualized network.</span></span>

```yaml
Type: LogicalNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8cb-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce8cb-120">-Name</span></span>
<span data-ttu-id="ce8cb-121">Указывает имя виртуализированной сети.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-121">Specifies a name for the virtualized network.</span></span>

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

### <span data-ttu-id="ce8cb-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="ce8cb-122">-Profile</span></span>
<span data-ttu-id="ce8cb-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce8cb-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce8cb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8cb-125">CommonParameters</span></span>
<span data-ttu-id="ce8cb-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce8cb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8cb-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce8cb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8cb-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce8cb-128">INPUTS</span></span>

## <span data-ttu-id="ce8cb-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce8cb-129">OUTPUTS</span></span>

## <span data-ttu-id="ce8cb-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce8cb-130">NOTES</span></span>

## <span data-ttu-id="ce8cb-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce8cb-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce8cb-132">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="ce8cb-132">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="ce8cb-133">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="ce8cb-133">Remove-WAPackVNet</span></span>](./Remove-WAPackVNet.md)


