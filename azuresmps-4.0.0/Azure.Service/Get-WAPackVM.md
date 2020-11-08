---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077356"
---
# <span data-ttu-id="cf544-101">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cf544-101">Get-WAPackVM</span></span>

## <span data-ttu-id="cf544-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf544-102">SYNOPSIS</span></span>
<span data-ttu-id="cf544-103">Получение объектов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cf544-103">Gets virtual machine objects.</span></span>

## <span data-ttu-id="cf544-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf544-104">SYNTAX</span></span>

### <span data-ttu-id="cf544-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf544-105">Empty (Default)</span></span>
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cf544-106">FromName</span><span class="sxs-lookup"><span data-stu-id="cf544-106">FromName</span></span>
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cf544-107">FromId</span><span class="sxs-lookup"><span data-stu-id="cf544-107">FromId</span></span>
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cf544-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf544-108">DESCRIPTION</span></span>
<span data-ttu-id="cf544-109">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="cf544-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="cf544-110">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cf544-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cf544-111">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cf544-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="cf544-112">Командлет **Get-WAPackVM** получает объекты виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cf544-112">The **Get-WAPackVM** cmdlet gets virtual machine objects.</span></span>

## <span data-ttu-id="cf544-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf544-113">EXAMPLES</span></span>

### <span data-ttu-id="cf544-114">Пример 1: получение виртуальной машины с помощью имени</span><span class="sxs-lookup"><span data-stu-id="cf544-114">Example 1: Get a virtual machine by using a name</span></span>
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

<span data-ttu-id="cf544-115">Эта команда получает виртуальную машину с именем ContosoV126.</span><span class="sxs-lookup"><span data-stu-id="cf544-115">This command gets the virtual machine named ContosoV126.</span></span>

### <span data-ttu-id="cf544-116">Пример 2: получение виртуальной машины с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="cf544-116">Example 2: Get a virtual machine by using an ID</span></span>
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="cf544-117">Эта команда возвращает виртуальную машину с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="cf544-117">This command gets the virtual machine that has the specified ID.</span></span>

### <span data-ttu-id="cf544-118">Пример 3: получение всех виртуальных машин</span><span class="sxs-lookup"><span data-stu-id="cf544-118">Example 3: Get all virtual machines</span></span>
```
PS C:\> Get-WAPackVM
```

<span data-ttu-id="cf544-119">Эта команда возвращает все виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="cf544-119">This command gets all virtual machines.</span></span>

## <span data-ttu-id="cf544-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf544-120">PARAMETERS</span></span>

### <span data-ttu-id="cf544-121">-ID</span><span class="sxs-lookup"><span data-stu-id="cf544-121">-ID</span></span>
<span data-ttu-id="cf544-122">Указывает уникальный идентификатор виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cf544-122">Specifies the unique ID of a virtual machine.</span></span>

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

### <span data-ttu-id="cf544-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf544-123">-Name</span></span>
<span data-ttu-id="cf544-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cf544-124">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="cf544-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="cf544-125">-Profile</span></span>
<span data-ttu-id="cf544-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cf544-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cf544-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf544-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf544-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf544-128">CommonParameters</span></span>
<span data-ttu-id="cf544-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf544-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf544-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf544-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf544-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf544-131">INPUTS</span></span>

## <span data-ttu-id="cf544-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf544-132">OUTPUTS</span></span>

## <span data-ttu-id="cf544-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf544-133">NOTES</span></span>

## <span data-ttu-id="cf544-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf544-134">RELATED LINKS</span></span>

[<span data-ttu-id="cf544-135">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cf544-135">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="cf544-136">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cf544-136">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="cf544-137">Restarting-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cf544-137">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="cf544-138">Возобновить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cf544-138">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="cf544-139">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cf544-139">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="cf544-140">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cf544-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="cf544-141">Остановить-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cf544-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="cf544-142">Приостановить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cf544-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="cf544-143">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="cf544-143">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


