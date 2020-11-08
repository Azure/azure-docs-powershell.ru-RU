---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076330"
---
# <span data-ttu-id="9447e-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="9447e-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="9447e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9447e-102">SYNOPSIS</span></span>
<span data-ttu-id="9447e-103">Извлекает сведения об использовании коллекции RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="9447e-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9447e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9447e-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9447e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9447e-105">DESCRIPTION</span></span>
<span data-ttu-id="9447e-106">Командлет **Get-AzureRemoteAppCollectionUsageSummary** извлекает сведения об использовании коллекции RemoteApp из Azure.</span><span class="sxs-lookup"><span data-stu-id="9447e-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9447e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9447e-107">EXAMPLES</span></span>

### <span data-ttu-id="9447e-108">Пример 1: получение сводки об использовании</span><span class="sxs-lookup"><span data-stu-id="9447e-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="9447e-109">Эта команда возвращает сводку по использованию за декабрь в 2014 г. для коллекции с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="9447e-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="9447e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9447e-110">PARAMETERS</span></span>

### <span data-ttu-id="9447e-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="9447e-111">-CollectionName</span></span>
<span data-ttu-id="9447e-112">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="9447e-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9447e-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="9447e-113">-Profile</span></span>
<span data-ttu-id="9447e-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9447e-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9447e-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9447e-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9447e-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="9447e-116">-UsageMonth</span></span>
<span data-ttu-id="9447e-117">Задает двузначное число для месяца, для которого требуется получить сведения об использовании.</span><span class="sxs-lookup"><span data-stu-id="9447e-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="9447e-118">Если этот параметр не указан, этот командлет предоставляет использование для текущего месяца.</span><span class="sxs-lookup"><span data-stu-id="9447e-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9447e-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="9447e-119">-UsageYear</span></span>
<span data-ttu-id="9447e-120">Указывает четырехзначный год, для которого требуется получить сведения об использовании.</span><span class="sxs-lookup"><span data-stu-id="9447e-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="9447e-121">Если этот параметр не указан, будет использоваться сводка по использованию за текущий год.</span><span class="sxs-lookup"><span data-stu-id="9447e-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9447e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9447e-122">CommonParameters</span></span>
<span data-ttu-id="9447e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9447e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9447e-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9447e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9447e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9447e-125">INPUTS</span></span>

## <span data-ttu-id="9447e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9447e-126">OUTPUTS</span></span>

## <span data-ttu-id="9447e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="9447e-127">NOTES</span></span>

## <span data-ttu-id="9447e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9447e-128">RELATED LINKS</span></span>

[<span data-ttu-id="9447e-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9447e-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="9447e-130">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="9447e-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


