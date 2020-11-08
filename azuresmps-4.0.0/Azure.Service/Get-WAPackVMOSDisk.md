---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077352"
---
# <span data-ttu-id="13d20-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="13d20-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="13d20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13d20-102">SYNOPSIS</span></span>
<span data-ttu-id="13d20-103">Возвращает дисковые объекты операционной системы для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="13d20-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="13d20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13d20-104">SYNTAX</span></span>

### <span data-ttu-id="13d20-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13d20-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13d20-106">FromId</span><span class="sxs-lookup"><span data-stu-id="13d20-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13d20-107">FromName</span><span class="sxs-lookup"><span data-stu-id="13d20-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13d20-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13d20-108">DESCRIPTION</span></span>
<span data-ttu-id="13d20-109">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="13d20-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="13d20-110">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13d20-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="13d20-111">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="13d20-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="13d20-112">Командлет **Get-WAPackVMOSDisk** получает объекты диска операционной системы для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="13d20-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="13d20-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13d20-113">EXAMPLES</span></span>

### <span data-ttu-id="13d20-114">Пример 1: Загрузка диска с операционной системой с использованием имени</span><span class="sxs-lookup"><span data-stu-id="13d20-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="13d20-115">Эта команда получает диск операционной системы с именем ContosoOSDisk.</span><span class="sxs-lookup"><span data-stu-id="13d20-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="13d20-116">Пример 2: получение диска операционной системы с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="13d20-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="13d20-117">Эта команда получает диск операционной системы с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="13d20-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="13d20-118">Пример 3: получение всех дисков операционной системы</span><span class="sxs-lookup"><span data-stu-id="13d20-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="13d20-119">Эта команда возвращает все диски операционной системы.</span><span class="sxs-lookup"><span data-stu-id="13d20-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="13d20-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13d20-120">PARAMETERS</span></span>

### <span data-ttu-id="13d20-121">-ID</span><span class="sxs-lookup"><span data-stu-id="13d20-121">-ID</span></span>
<span data-ttu-id="13d20-122">Указывает уникальный идентификатор диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="13d20-122">Specifies the unique ID of an operating system disk.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13d20-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13d20-123">-Name</span></span>
<span data-ttu-id="13d20-124">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="13d20-124">Specifies the name of an operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13d20-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="13d20-125">-Profile</span></span>
<span data-ttu-id="13d20-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="13d20-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13d20-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13d20-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13d20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d20-128">CommonParameters</span></span>
<span data-ttu-id="13d20-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13d20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d20-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d20-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d20-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13d20-131">INPUTS</span></span>

## <span data-ttu-id="13d20-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13d20-132">OUTPUTS</span></span>

## <span data-ttu-id="13d20-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="13d20-133">NOTES</span></span>

## <span data-ttu-id="13d20-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13d20-134">RELATED LINKS</span></span>

[<span data-ttu-id="13d20-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13d20-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


