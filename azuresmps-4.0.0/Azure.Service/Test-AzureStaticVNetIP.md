---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075936"
---
# <span data-ttu-id="7f986-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="7f986-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="7f986-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f986-102">SYNOPSIS</span></span>
<span data-ttu-id="7f986-103">Проверяет доступность статического IP-адреса виртуальной сети и получает список предложений, если запрашиваемый адрес недоступен.</span><span class="sxs-lookup"><span data-stu-id="7f986-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="7f986-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f986-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7f986-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f986-105">DESCRIPTION</span></span>
<span data-ttu-id="7f986-106">Командлет **Test-AzureStaticVNetIP** проверяет доступность статического IP-адреса виртуальной сети и возвращает список предложений, если запрашиваемый адрес недоступен.</span><span class="sxs-lookup"><span data-stu-id="7f986-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="7f986-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f986-107">EXAMPLES</span></span>

### <span data-ttu-id="7f986-108">1:</span><span class="sxs-lookup"><span data-stu-id="7f986-108">1:</span></span>
```

```

## <span data-ttu-id="7f986-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f986-109">PARAMETERS</span></span>

### <span data-ttu-id="7f986-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7f986-110">-InformationAction</span></span>
<span data-ttu-id="7f986-111">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="7f986-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7f986-112">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7f986-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f986-113">Продолжал</span><span class="sxs-lookup"><span data-stu-id="7f986-113">Continue</span></span>
- <span data-ttu-id="7f986-114">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="7f986-114">Ignore</span></span>
- <span data-ttu-id="7f986-115">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="7f986-115">Inquire</span></span>
- <span data-ttu-id="7f986-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7f986-116">SilentlyContinue</span></span>
- <span data-ttu-id="7f986-117">Остановить</span><span class="sxs-lookup"><span data-stu-id="7f986-117">Stop</span></span>
- <span data-ttu-id="7f986-118">Рвать</span><span class="sxs-lookup"><span data-stu-id="7f986-118">Suspend</span></span>

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

### <span data-ttu-id="7f986-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7f986-119">-InformationVariable</span></span>
<span data-ttu-id="7f986-120">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="7f986-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7f986-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="7f986-121">-IPAddress</span></span>
<span data-ttu-id="7f986-122">Задает статический IP-адрес виртуальной сети для запроса.</span><span class="sxs-lookup"><span data-stu-id="7f986-122">Specifies the static virtual network IP address to query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f986-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="7f986-123">-Profile</span></span>
<span data-ttu-id="7f986-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7f986-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f986-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f986-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f986-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="7f986-126">-VNetName</span></span>
<span data-ttu-id="7f986-127">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7f986-127">Specifies the Name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f986-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f986-128">CommonParameters</span></span>
<span data-ttu-id="7f986-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f986-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f986-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f986-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f986-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f986-131">INPUTS</span></span>

## <span data-ttu-id="7f986-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f986-132">OUTPUTS</span></span>

## <span data-ttu-id="7f986-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f986-133">NOTES</span></span>

## <span data-ttu-id="7f986-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f986-134">RELATED LINKS</span></span>

[<span data-ttu-id="7f986-135">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="7f986-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="7f986-136">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="7f986-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


