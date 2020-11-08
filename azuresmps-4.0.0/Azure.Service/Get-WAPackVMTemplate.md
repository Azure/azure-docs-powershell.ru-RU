---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077391"
---
# <span data-ttu-id="f97cc-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="f97cc-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="f97cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f97cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f97cc-103">Получение шаблонов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f97cc-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="f97cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f97cc-104">SYNTAX</span></span>

### <span data-ttu-id="f97cc-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f97cc-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f97cc-106">FromId</span><span class="sxs-lookup"><span data-stu-id="f97cc-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f97cc-107">FromName</span><span class="sxs-lookup"><span data-stu-id="f97cc-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f97cc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f97cc-108">DESCRIPTION</span></span>
<span data-ttu-id="f97cc-109">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="f97cc-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="f97cc-110">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f97cc-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f97cc-111">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f97cc-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f97cc-112">Командлет **Get-WAPackVMTemplate** получает шаблоны виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f97cc-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="f97cc-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f97cc-113">EXAMPLES</span></span>

### <span data-ttu-id="f97cc-114">Пример 1: получение шаблона виртуальной машины с помощью имени</span><span class="sxs-lookup"><span data-stu-id="f97cc-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="f97cc-115">Эта команда получает шаблон виртуальной машины с именем ContosoTemplate04.</span><span class="sxs-lookup"><span data-stu-id="f97cc-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="f97cc-116">Пример 2: получение шаблона виртуальной машины с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="f97cc-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="f97cc-117">Эта команда получает шаблон виртуальной машины с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="f97cc-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="f97cc-118">Пример 3: получение всех шаблонов виртуальных машин</span><span class="sxs-lookup"><span data-stu-id="f97cc-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="f97cc-119">Эта команда возвращает все шаблоны виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f97cc-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="f97cc-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f97cc-120">PARAMETERS</span></span>

### <span data-ttu-id="f97cc-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f97cc-121">-ID</span></span>
<span data-ttu-id="f97cc-122">Указывает уникальный идентификатор шаблона.</span><span class="sxs-lookup"><span data-stu-id="f97cc-122">Specifies the unique ID of a template.</span></span>

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

### <span data-ttu-id="f97cc-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f97cc-123">-Name</span></span>
<span data-ttu-id="f97cc-124">Указывает имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="f97cc-124">Specifies the name of a template.</span></span>

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

### <span data-ttu-id="f97cc-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="f97cc-125">-Profile</span></span>
<span data-ttu-id="f97cc-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f97cc-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f97cc-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f97cc-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f97cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97cc-128">CommonParameters</span></span>
<span data-ttu-id="f97cc-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f97cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97cc-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f97cc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97cc-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f97cc-131">INPUTS</span></span>

## <span data-ttu-id="f97cc-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f97cc-132">OUTPUTS</span></span>

## <span data-ttu-id="f97cc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f97cc-133">NOTES</span></span>

## <span data-ttu-id="f97cc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f97cc-134">RELATED LINKS</span></span>

[<span data-ttu-id="f97cc-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f97cc-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


