---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076527"
---
# <span data-ttu-id="85378-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="85378-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="85378-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85378-102">SYNOPSIS</span></span>
<span data-ttu-id="85378-103">Получает объект списка со сведениями об виртуальных сетях Azure.</span><span class="sxs-lookup"><span data-stu-id="85378-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="85378-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85378-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="85378-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85378-105">DESCRIPTION</span></span>
<span data-ttu-id="85378-106">Командлет **Get-AzureVNetSite** получает объект списка со сведениями о виртуальных сетях Azure для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="85378-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="85378-107">Если указать имя виртуальной сети, будет возвращена только информация для этой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="85378-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="85378-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85378-108">EXAMPLES</span></span>

### <span data-ttu-id="85378-109">Пример 1: получение сведений обо всех виртуальных сетях в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="85378-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="85378-110">Эта команда получает сведения обо всех виртуальных сетях в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="85378-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="85378-111">Пример 2: получение сведений о конкретной виртуальной сети в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="85378-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="85378-112">Эта команда извлекает сведения только о виртуальной сети MyProductionNetwork.</span><span class="sxs-lookup"><span data-stu-id="85378-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="85378-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85378-113">PARAMETERS</span></span>

### <span data-ttu-id="85378-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="85378-114">-InformationAction</span></span>
<span data-ttu-id="85378-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="85378-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="85378-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="85378-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85378-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="85378-117">Continue</span></span>
- <span data-ttu-id="85378-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="85378-118">Ignore</span></span>
- <span data-ttu-id="85378-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="85378-119">Inquire</span></span>
- <span data-ttu-id="85378-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="85378-120">SilentlyContinue</span></span>
- <span data-ttu-id="85378-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="85378-121">Stop</span></span>
- <span data-ttu-id="85378-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="85378-122">Suspend</span></span>

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

### <span data-ttu-id="85378-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="85378-123">-InformationVariable</span></span>
<span data-ttu-id="85378-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="85378-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="85378-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="85378-125">-Profile</span></span>
<span data-ttu-id="85378-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="85378-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="85378-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85378-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="85378-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="85378-128">-VNetName</span></span>
<span data-ttu-id="85378-129">Указывает имя виртуальной сети, сведения о котором нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="85378-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85378-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85378-130">CommonParameters</span></span>
<span data-ttu-id="85378-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85378-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85378-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85378-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85378-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85378-133">INPUTS</span></span>

## <span data-ttu-id="85378-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85378-134">OUTPUTS</span></span>

## <span data-ttu-id="85378-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="85378-135">NOTES</span></span>

## <span data-ttu-id="85378-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85378-136">RELATED LINKS</span></span>

[<span data-ttu-id="85378-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="85378-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="85378-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="85378-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="85378-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="85378-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


