---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076263"
---
# <span data-ttu-id="bf929-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="bf929-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="bf929-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf929-102">SYNOPSIS</span></span>
<span data-ttu-id="bf929-103">Получает виртуальные сети.</span><span class="sxs-lookup"><span data-stu-id="bf929-103">Gets virtual networks.</span></span>

## <span data-ttu-id="bf929-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf929-104">SYNTAX</span></span>

### <span data-ttu-id="bf929-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf929-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bf929-106">FromId</span><span class="sxs-lookup"><span data-stu-id="bf929-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bf929-107">FromName</span><span class="sxs-lookup"><span data-stu-id="bf929-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf929-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf929-108">DESCRIPTION</span></span>
<span data-ttu-id="bf929-109">Командлет **Get-WAPackVNet** получает виртуальные сети.</span><span class="sxs-lookup"><span data-stu-id="bf929-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="bf929-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf929-110">EXAMPLES</span></span>

### <span data-ttu-id="bf929-111">Пример 1: получение всех виртуальных сетей</span><span class="sxs-lookup"><span data-stu-id="bf929-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="bf929-112">Эта команда возвращает все виртуальные сети.</span><span class="sxs-lookup"><span data-stu-id="bf929-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="bf929-113">Пример 2: получение виртуальной сети с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="bf929-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="bf929-114">Эта команда возвращает виртуальную сеть с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="bf929-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="bf929-115">Пример 3: получение виртуальной сети с помощью имени</span><span class="sxs-lookup"><span data-stu-id="bf929-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="bf929-116">Эта команда возвращает виртуальную сеть с именем ContosoVNet08.</span><span class="sxs-lookup"><span data-stu-id="bf929-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="bf929-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf929-117">PARAMETERS</span></span>

### <span data-ttu-id="bf929-118">-ID</span><span class="sxs-lookup"><span data-stu-id="bf929-118">-ID</span></span>
<span data-ttu-id="bf929-119">Указывает уникальный идентификатор виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bf929-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf929-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf929-120">-Name</span></span>
<span data-ttu-id="bf929-121">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bf929-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf929-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="bf929-122">-Profile</span></span>
<span data-ttu-id="bf929-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bf929-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf929-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bf929-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf929-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf929-125">CommonParameters</span></span>
<span data-ttu-id="bf929-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf929-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf929-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf929-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf929-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf929-128">INPUTS</span></span>

## <span data-ttu-id="bf929-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf929-129">OUTPUTS</span></span>

## <span data-ttu-id="bf929-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf929-130">NOTES</span></span>

## <span data-ttu-id="bf929-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf929-131">RELATED LINKS</span></span>

