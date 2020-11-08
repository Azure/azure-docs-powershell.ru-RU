---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077430"
---
# <span data-ttu-id="8748e-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="8748e-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="8748e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8748e-102">SYNOPSIS</span></span>
<span data-ttu-id="8748e-103">Получает объекты профиля размера.</span><span class="sxs-lookup"><span data-stu-id="8748e-103">Gets size profile objects.</span></span>

## <span data-ttu-id="8748e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8748e-104">SYNTAX</span></span>

### <span data-ttu-id="8748e-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8748e-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8748e-106">FromId</span><span class="sxs-lookup"><span data-stu-id="8748e-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8748e-107">FromName</span><span class="sxs-lookup"><span data-stu-id="8748e-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8748e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8748e-108">DESCRIPTION</span></span>
<span data-ttu-id="8748e-109">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="8748e-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8748e-110">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8748e-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8748e-111">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8748e-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8748e-112">Командлет **Get-WAPackVMSizeProfile** получает объекты профиля размера для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8748e-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="8748e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8748e-113">EXAMPLES</span></span>

### <span data-ttu-id="8748e-114">Пример 1: получение профиля размера с помощью имени</span><span class="sxs-lookup"><span data-stu-id="8748e-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="8748e-115">Эта команда получает профиль размера с именем ContosoSizeProfile07.</span><span class="sxs-lookup"><span data-stu-id="8748e-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="8748e-116">Пример 2: получение профиля размера с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="8748e-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="8748e-117">Эта команда получает профиль размера с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="8748e-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="8748e-118">Пример 3: получение всех профилей размера</span><span class="sxs-lookup"><span data-stu-id="8748e-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="8748e-119">Эта команда получает все профили размера.</span><span class="sxs-lookup"><span data-stu-id="8748e-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="8748e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8748e-120">PARAMETERS</span></span>

### <span data-ttu-id="8748e-121">-ID</span><span class="sxs-lookup"><span data-stu-id="8748e-121">-ID</span></span>
<span data-ttu-id="8748e-122">Указывает уникальный идентификатор профиля размера.</span><span class="sxs-lookup"><span data-stu-id="8748e-122">Specifies the unique ID of a size profile.</span></span>

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

### <span data-ttu-id="8748e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8748e-123">-Name</span></span>
<span data-ttu-id="8748e-124">Задает имя профиля размера.</span><span class="sxs-lookup"><span data-stu-id="8748e-124">Specifies the name of a size profile.</span></span>

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

### <span data-ttu-id="8748e-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="8748e-125">-Profile</span></span>
<span data-ttu-id="8748e-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8748e-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8748e-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8748e-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8748e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8748e-128">CommonParameters</span></span>
<span data-ttu-id="8748e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8748e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8748e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8748e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8748e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8748e-131">INPUTS</span></span>

## <span data-ttu-id="8748e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8748e-132">OUTPUTS</span></span>

## <span data-ttu-id="8748e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8748e-133">NOTES</span></span>

## <span data-ttu-id="8748e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8748e-134">RELATED LINKS</span></span>

[<span data-ttu-id="8748e-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8748e-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


