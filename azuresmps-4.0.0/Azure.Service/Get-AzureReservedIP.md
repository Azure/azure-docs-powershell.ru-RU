---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075618"
---
# <span data-ttu-id="3c941-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3c941-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="3c941-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c941-102">SYNOPSIS</span></span>
<span data-ttu-id="3c941-103">Получает зарезервированный IP-адрес по его имени или список всех зарезервированных IP-адресов в подписке.</span><span class="sxs-lookup"><span data-stu-id="3c941-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="3c941-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c941-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3c941-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c941-105">DESCRIPTION</span></span>
<span data-ttu-id="3c941-106">Командлет **Get-AzureReservedIP** получает зарезервированный IP-адрес по его имени или список всех зарезервированных IP-адресов в подписке.</span><span class="sxs-lookup"><span data-stu-id="3c941-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="3c941-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c941-107">EXAMPLES</span></span>

### <span data-ttu-id="3c941-108">Пример 1: получение всех зарезервированных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="3c941-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="3c941-109">Эта команда получает все зарезервированные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3c941-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="3c941-110">Пример 2: получение зарезервированного IP-адреса с указанным именем</span><span class="sxs-lookup"><span data-stu-id="3c941-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="3c941-111">Эта команда получает зарезервированный IP-адрес с именем, указанным в переменной $IpName.</span><span class="sxs-lookup"><span data-stu-id="3c941-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="3c941-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c941-112">PARAMETERS</span></span>

### <span data-ttu-id="3c941-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3c941-113">-InformationAction</span></span>
<span data-ttu-id="3c941-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="3c941-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3c941-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3c941-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c941-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="3c941-116">Continue</span></span>
- <span data-ttu-id="3c941-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="3c941-117">Ignore</span></span>
- <span data-ttu-id="3c941-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="3c941-118">Inquire</span></span>
- <span data-ttu-id="3c941-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3c941-119">SilentlyContinue</span></span>
- <span data-ttu-id="3c941-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="3c941-120">Stop</span></span>
- <span data-ttu-id="3c941-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="3c941-121">Suspend</span></span>

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

### <span data-ttu-id="3c941-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3c941-122">-InformationVariable</span></span>
<span data-ttu-id="3c941-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="3c941-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3c941-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="3c941-124">-Profile</span></span>
<span data-ttu-id="3c941-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3c941-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c941-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c941-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c941-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="3c941-127">-ReservedIPName</span></span>
<span data-ttu-id="3c941-128">Задает зарезервированное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3c941-128">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c941-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c941-129">CommonParameters</span></span>
<span data-ttu-id="3c941-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c941-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c941-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c941-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c941-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c941-132">INPUTS</span></span>

## <span data-ttu-id="3c941-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c941-133">OUTPUTS</span></span>

## <span data-ttu-id="3c941-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c941-134">NOTES</span></span>

## <span data-ttu-id="3c941-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c941-135">RELATED LINKS</span></span>

[<span data-ttu-id="3c941-136">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3c941-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="3c941-137">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3c941-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


