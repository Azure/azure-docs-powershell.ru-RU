---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076336"
---
# <span data-ttu-id="a6204-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="a6204-101">Get-AzureLocation</span></span>

## <span data-ttu-id="a6204-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6204-102">SYNOPSIS</span></span>
<span data-ttu-id="a6204-103">Возвращает доступные расположения центра обработки данных для текущей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a6204-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="a6204-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6204-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a6204-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6204-105">DESCRIPTION</span></span>
<span data-ttu-id="a6204-106">Командлет **Get-AzureLocation** получает список доступных центров обработки данных Azure и их свойств для текущей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a6204-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="a6204-107">Перед запуском этого командлета необходимо настроить текущую подписку с помощью командлетов Select-AzureSubscription и Set-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="a6204-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="a6204-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6204-108">EXAMPLES</span></span>

### <span data-ttu-id="a6204-109">Пример 1: получение местоположений</span><span class="sxs-lookup"><span data-stu-id="a6204-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="a6204-110">Эта команда получает список доступных центров обработки данных и их свойств для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="a6204-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="a6204-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6204-111">PARAMETERS</span></span>

### <span data-ttu-id="a6204-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a6204-112">-InformationAction</span></span>
<span data-ttu-id="a6204-113">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a6204-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a6204-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a6204-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a6204-115">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a6204-115">Continue</span></span>
- <span data-ttu-id="a6204-116">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a6204-116">Ignore</span></span>
- <span data-ttu-id="a6204-117">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a6204-117">Inquire</span></span>
- <span data-ttu-id="a6204-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a6204-118">SilentlyContinue</span></span>
- <span data-ttu-id="a6204-119">Остановить</span><span class="sxs-lookup"><span data-stu-id="a6204-119">Stop</span></span>
- <span data-ttu-id="a6204-120">Рвать</span><span class="sxs-lookup"><span data-stu-id="a6204-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6204-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a6204-121">-InformationVariable</span></span>
<span data-ttu-id="a6204-122">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a6204-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6204-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="a6204-123">-Profile</span></span>
<span data-ttu-id="a6204-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6204-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a6204-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6204-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6204-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6204-126">CommonParameters</span></span>
<span data-ttu-id="a6204-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6204-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6204-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6204-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6204-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6204-129">INPUTS</span></span>

## <span data-ttu-id="a6204-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6204-130">OUTPUTS</span></span>

## <span data-ttu-id="a6204-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6204-131">NOTES</span></span>

## <span data-ttu-id="a6204-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6204-132">RELATED LINKS</span></span>

