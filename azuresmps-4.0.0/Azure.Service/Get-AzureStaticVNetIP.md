---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 12BF47AA-9E82-425E-A1EB-BAD64D800943
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3be6496993ed6de248103b9a222df4cbe15ed2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076557"
---
# <span data-ttu-id="c89d2-101">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c89d2-101">Get-AzureStaticVNetIP</span></span>

## <span data-ttu-id="c89d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c89d2-102">SYNOPSIS</span></span>
<span data-ttu-id="c89d2-103">Получает данные статического IP-адреса VNet из объекта виртуальной машины, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="c89d2-103">Gets the static VNet IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="c89d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c89d2-104">SYNTAX</span></span>

```
Get-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c89d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c89d2-105">DESCRIPTION</span></span>
<span data-ttu-id="c89d2-106">Командлет **Get-AzureStaticVNetIP** получает сведения о статических IP-адресах виртуальных сетей (VNet) из объекта виртуальной машины, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="c89d2-106">The **Get-AzureStaticVNetIP** cmdlet gets the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="c89d2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c89d2-107">EXAMPLES</span></span>

### <span data-ttu-id="c89d2-108">1:</span><span class="sxs-lookup"><span data-stu-id="c89d2-108">1:</span></span>
```

```

## <span data-ttu-id="c89d2-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c89d2-109">PARAMETERS</span></span>

### <span data-ttu-id="c89d2-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c89d2-110">-InformationAction</span></span>
<span data-ttu-id="c89d2-111">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="c89d2-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c89d2-112">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c89d2-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c89d2-113">Продолжал</span><span class="sxs-lookup"><span data-stu-id="c89d2-113">Continue</span></span>
- <span data-ttu-id="c89d2-114">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="c89d2-114">Ignore</span></span>
- <span data-ttu-id="c89d2-115">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c89d2-115">Inquire</span></span>
- <span data-ttu-id="c89d2-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c89d2-116">SilentlyContinue</span></span>
- <span data-ttu-id="c89d2-117">Остановить</span><span class="sxs-lookup"><span data-stu-id="c89d2-117">Stop</span></span>
- <span data-ttu-id="c89d2-118">Рвать</span><span class="sxs-lookup"><span data-stu-id="c89d2-118">Suspend</span></span>

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

### <span data-ttu-id="c89d2-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c89d2-119">-InformationVariable</span></span>
<span data-ttu-id="c89d2-120">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="c89d2-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c89d2-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="c89d2-121">-Profile</span></span>
<span data-ttu-id="c89d2-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c89d2-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c89d2-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c89d2-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c89d2-124">-VM</span><span class="sxs-lookup"><span data-stu-id="c89d2-124">-VM</span></span>
<span data-ttu-id="c89d2-125">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c89d2-125">Specifies a persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c89d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c89d2-126">CommonParameters</span></span>
<span data-ttu-id="c89d2-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c89d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c89d2-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c89d2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c89d2-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c89d2-129">INPUTS</span></span>

## <span data-ttu-id="c89d2-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c89d2-130">OUTPUTS</span></span>

## <span data-ttu-id="c89d2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c89d2-131">NOTES</span></span>

## <span data-ttu-id="c89d2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c89d2-132">RELATED LINKS</span></span>

[<span data-ttu-id="c89d2-133">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c89d2-133">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


