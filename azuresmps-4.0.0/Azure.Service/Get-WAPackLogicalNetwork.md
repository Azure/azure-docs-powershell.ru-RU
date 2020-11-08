---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D51BE56-C0A2-4A32-BB7F-8FA9CC67F8F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 986d4998119c4ede1780fa35ad6baadce4574a81
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077354"
---
# <span data-ttu-id="7c146-101">Get-WAPackLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="7c146-101">Get-WAPackLogicalNetwork</span></span>

## <span data-ttu-id="7c146-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c146-102">SYNOPSIS</span></span>
<span data-ttu-id="7c146-103">Получает логические объекты сети.</span><span class="sxs-lookup"><span data-stu-id="7c146-103">Gets logical network objects.</span></span>

## <span data-ttu-id="7c146-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c146-104">SYNTAX</span></span>

### <span data-ttu-id="7c146-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c146-105">Empty (Default)</span></span>
```
Get-WAPackLogicalNetwork [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7c146-106">FromName</span><span class="sxs-lookup"><span data-stu-id="7c146-106">FromName</span></span>
```
Get-WAPackLogicalNetwork [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7c146-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c146-107">DESCRIPTION</span></span>
<span data-ttu-id="7c146-108">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="7c146-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7c146-109">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c146-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7c146-110">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7c146-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7c146-111">Командлет **Get-WAPackLogicalNetwork** получает логические объекты сети.</span><span class="sxs-lookup"><span data-stu-id="7c146-111">The **Get-WAPackLogicalNetwork** cmdlet gets logical network objects.</span></span>

## <span data-ttu-id="7c146-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c146-112">EXAMPLES</span></span>

### <span data-ttu-id="7c146-113">Пример 1: получение логической сети с помощью имени</span><span class="sxs-lookup"><span data-stu-id="7c146-113">Example 1: Get a logical network by using a name</span></span>
```
PS C:\> Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
```

<span data-ttu-id="7c146-114">Эта команда возвращает логическую сеть с именем ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="7c146-114">This command gets a logical network named ContosoLogicalNetwork01.</span></span>

### <span data-ttu-id="7c146-115">Пример 2: получение всех логических сетей</span><span class="sxs-lookup"><span data-stu-id="7c146-115">Example 2: Get all logical networks</span></span>
```
PS C:\> Get-WAPackLogicalNetwork
```

<span data-ttu-id="7c146-116">Эта команда возвращает все логические сети.</span><span class="sxs-lookup"><span data-stu-id="7c146-116">This command gets all logical networks.</span></span>

## <span data-ttu-id="7c146-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c146-117">PARAMETERS</span></span>

### <span data-ttu-id="7c146-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c146-118">-Name</span></span>
<span data-ttu-id="7c146-119">Указывает имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="7c146-119">Specifies the name of a logical network.</span></span>

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

### <span data-ttu-id="7c146-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="7c146-120">-Profile</span></span>
<span data-ttu-id="7c146-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7c146-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c146-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c146-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c146-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c146-123">CommonParameters</span></span>
<span data-ttu-id="7c146-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c146-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c146-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c146-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c146-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c146-126">INPUTS</span></span>

## <span data-ttu-id="7c146-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c146-127">OUTPUTS</span></span>

## <span data-ttu-id="7c146-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c146-128">NOTES</span></span>

## <span data-ttu-id="7c146-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c146-129">RELATED LINKS</span></span>

