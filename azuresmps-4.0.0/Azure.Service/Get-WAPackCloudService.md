---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077353"
---
# <span data-ttu-id="efbe8-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="efbe8-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="efbe8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="efbe8-102">SYNOPSIS</span></span>
<span data-ttu-id="efbe8-103">Возвращает объекты облачной службы.</span><span class="sxs-lookup"><span data-stu-id="efbe8-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="efbe8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="efbe8-104">SYNTAX</span></span>

### <span data-ttu-id="efbe8-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="efbe8-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="efbe8-106">FromName</span><span class="sxs-lookup"><span data-stu-id="efbe8-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="efbe8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efbe8-107">DESCRIPTION</span></span>
<span data-ttu-id="efbe8-108">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="efbe8-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="efbe8-109">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="efbe8-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="efbe8-110">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="efbe8-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="efbe8-111">Командлет **Get-WAPackCloudService** получает объекты облачной службы.</span><span class="sxs-lookup"><span data-stu-id="efbe8-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="efbe8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="efbe8-112">EXAMPLES</span></span>

## <span data-ttu-id="efbe8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="efbe8-113">PARAMETERS</span></span>

### <span data-ttu-id="efbe8-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="efbe8-114">-Name</span></span>
<span data-ttu-id="efbe8-115">Указывает имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="efbe8-115">Specifies the name of a cloud service.</span></span>

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

### <span data-ttu-id="efbe8-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="efbe8-116">-Profile</span></span>
<span data-ttu-id="efbe8-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="efbe8-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="efbe8-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="efbe8-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="efbe8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efbe8-119">CommonParameters</span></span>
<span data-ttu-id="efbe8-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="efbe8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efbe8-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efbe8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efbe8-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="efbe8-122">INPUTS</span></span>

## <span data-ttu-id="efbe8-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="efbe8-123">OUTPUTS</span></span>

## <span data-ttu-id="efbe8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="efbe8-124">NOTES</span></span>

## <span data-ttu-id="efbe8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efbe8-125">RELATED LINKS</span></span>

[<span data-ttu-id="efbe8-126">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="efbe8-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="efbe8-127">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="efbe8-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


