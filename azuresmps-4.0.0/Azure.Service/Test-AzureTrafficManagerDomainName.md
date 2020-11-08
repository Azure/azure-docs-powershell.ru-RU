---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075935"
---
# <span data-ttu-id="fa872-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="fa872-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="fa872-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa872-102">SYNOPSIS</span></span>
<span data-ttu-id="fa872-103">Проверяет, доступно ли имя домена в качестве профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="fa872-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="fa872-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa872-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fa872-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa872-105">DESCRIPTION</span></span>
<span data-ttu-id="fa872-106">Командлет **Test-AzureTrafficManagerDomainName** проверяет, доступно ли имя домена в качестве профиля диспетчера трафика Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fa872-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="fa872-107">Если доменное имя доступно, этот командлет возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="fa872-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="fa872-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa872-108">EXAMPLES</span></span>

### <span data-ttu-id="fa872-109">Пример 1: Проверка наличия доменного имени</span><span class="sxs-lookup"><span data-stu-id="fa872-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="fa872-110">Эта команда проверяет, доступен ли доменное имя ContosoApp.trafficmanager.net в качестве профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="fa872-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="fa872-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa872-111">PARAMETERS</span></span>

### <span data-ttu-id="fa872-112">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="fa872-112">-DomainName</span></span>
<span data-ttu-id="fa872-113">Указывает имя доменного имени для проверки.</span><span class="sxs-lookup"><span data-stu-id="fa872-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="fa872-114">Необходимо включить следующую строку:</span><span class="sxs-lookup"><span data-stu-id="fa872-114">You must include the following string:</span></span> 

<span data-ttu-id="fa872-115">. trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="fa872-115">.trafficmanager.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa872-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="fa872-116">-Profile</span></span>
<span data-ttu-id="fa872-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fa872-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="fa872-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa872-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa872-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa872-119">CommonParameters</span></span>
<span data-ttu-id="fa872-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa872-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa872-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa872-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa872-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa872-122">INPUTS</span></span>

## <span data-ttu-id="fa872-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa872-123">OUTPUTS</span></span>

### <span data-ttu-id="fa872-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa872-124">System.Boolean</span></span>
<span data-ttu-id="fa872-125">Этот командлет создает $True или $False.</span><span class="sxs-lookup"><span data-stu-id="fa872-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="fa872-126">Если доменное имя доступно, этот командлет возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="fa872-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="fa872-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa872-127">NOTES</span></span>

## <span data-ttu-id="fa872-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa872-128">RELATED LINKS</span></span>

