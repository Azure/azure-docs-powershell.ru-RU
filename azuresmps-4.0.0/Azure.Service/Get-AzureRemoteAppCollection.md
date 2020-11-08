---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076329"
---
# <span data-ttu-id="c424d-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c424d-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="c424d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c424d-102">SYNOPSIS</span></span>
<span data-ttu-id="c424d-103">Получение сведений о коллекции RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="c424d-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c424d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c424d-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c424d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c424d-105">DESCRIPTION</span></span>
<span data-ttu-id="c424d-106">Командлет **Get-AzureRemoteAppCollection** извлекает сведения о коллекциях RemoteApp Azure в Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c424d-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="c424d-107">Он возвращает объект со сведениями о конкретной коллекции или не указан ни одной коллекцией для всех коллекций в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="c424d-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="c424d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c424d-108">EXAMPLES</span></span>

### <span data-ttu-id="c424d-109">Пример 1: получение списка всех коллекций</span><span class="sxs-lookup"><span data-stu-id="c424d-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="c424d-110">Эта команда возвращает список всех коллекций RemoteApp Azure в подписке.</span><span class="sxs-lookup"><span data-stu-id="c424d-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="c424d-111">Пример 2: получение сведений об указанной коллекции</span><span class="sxs-lookup"><span data-stu-id="c424d-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="c424d-112">Эта команда возвращает сведения о коллекции RemoteApp Azure с именем ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="c424d-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="c424d-113">Пример 3: получение списка коллекций с использованием подстановочных знаков</span><span class="sxs-lookup"><span data-stu-id="c424d-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="c424d-114">Эта команда возвращает список всех коллекций RemoteApp Azure, отвечающих финансовому запросу \*.</span><span class="sxs-lookup"><span data-stu-id="c424d-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="c424d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c424d-115">PARAMETERS</span></span>

### <span data-ttu-id="c424d-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="c424d-116">-CollectionName</span></span>
<span data-ttu-id="c424d-117">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c424d-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c424d-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="c424d-118">-Profile</span></span>
<span data-ttu-id="c424d-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c424d-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c424d-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c424d-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c424d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c424d-121">CommonParameters</span></span>
<span data-ttu-id="c424d-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c424d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c424d-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c424d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c424d-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c424d-124">INPUTS</span></span>

## <span data-ttu-id="c424d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c424d-125">OUTPUTS</span></span>

## <span data-ttu-id="c424d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c424d-126">NOTES</span></span>

## <span data-ttu-id="c424d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c424d-127">RELATED LINKS</span></span>

[<span data-ttu-id="c424d-128">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c424d-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="c424d-129">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c424d-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="c424d-130">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c424d-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="c424d-131">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="c424d-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


