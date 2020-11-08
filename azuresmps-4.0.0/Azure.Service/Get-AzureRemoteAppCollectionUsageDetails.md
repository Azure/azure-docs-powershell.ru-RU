---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075632"
---
# <span data-ttu-id="25352-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="25352-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="25352-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25352-102">SYNOPSIS</span></span>
<span data-ttu-id="25352-103">Получение сведений об использовании коллекции RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="25352-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="25352-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25352-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="25352-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25352-105">DESCRIPTION</span></span>
<span data-ttu-id="25352-106">Командлет **Get-AzureRemoteAppCollectionUsageDetails** извлекает сведения об использовании коллекции RemoteApp из Azure.</span><span class="sxs-lookup"><span data-stu-id="25352-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="25352-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25352-107">EXAMPLES</span></span>

### <span data-ttu-id="25352-108">Пример 1: получение сведений об использовании для коллекции</span><span class="sxs-lookup"><span data-stu-id="25352-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="25352-109">Эта команда возвращает сведения об использовании для семейства Azure RemoteApp с именем Contoso за декабрь в 2014.</span><span class="sxs-lookup"><span data-stu-id="25352-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="25352-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25352-110">PARAMETERS</span></span>

### <span data-ttu-id="25352-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25352-111">-AsJob</span></span>
<span data-ttu-id="25352-112">Указывает на то, что командлет выполняется в фоновом режиме в виде задания Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25352-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25352-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="25352-113">-CollectionName</span></span>
<span data-ttu-id="25352-114">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="25352-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="25352-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="25352-115">-Profile</span></span>
<span data-ttu-id="25352-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="25352-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25352-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25352-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25352-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="25352-118">-UsageMonth</span></span>
<span data-ttu-id="25352-119">Задает двузначное число для месяца, для которого требуется получить сведения об использовании.</span><span class="sxs-lookup"><span data-stu-id="25352-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

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

### <span data-ttu-id="25352-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="25352-120">-UsageYear</span></span>
<span data-ttu-id="25352-121">Задает четырехзначный год, для которого требуется получить сведения об использовании.</span><span class="sxs-lookup"><span data-stu-id="25352-121">Specifies the four-digit year for which to get usage details.</span></span>

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

### <span data-ttu-id="25352-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25352-122">CommonParameters</span></span>
<span data-ttu-id="25352-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25352-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25352-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25352-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25352-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25352-125">INPUTS</span></span>

## <span data-ttu-id="25352-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25352-126">OUTPUTS</span></span>

## <span data-ttu-id="25352-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="25352-127">NOTES</span></span>

## <span data-ttu-id="25352-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25352-128">RELATED LINKS</span></span>

[<span data-ttu-id="25352-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="25352-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="25352-130">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="25352-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


