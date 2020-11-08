---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 94D20309-5F72-4BE5-A150-2D6DD754286A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a9d793bb9bc8d96150b812474bed9f8997adbe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076104"
---
# <span data-ttu-id="7e1e9-101">Remove-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="7e1e9-101">Remove-AzureStaticVNetIP</span></span>

## <span data-ttu-id="7e1e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1e9-103">Удаляет данные об IP-адресе статической виртуальной сети из объекта виртуальной машины, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="7e1e9-103">Removes the static virtual network IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="7e1e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e1e9-104">SYNTAX</span></span>

```
Remove-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7e1e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="7e1e9-106">Командлет **Remove-AzureStaticVNetIP** удаляет статические сведения о IP-адресе виртуальной сети (VNet) из объекта виртуальной машины, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="7e1e9-106">The **Remove-AzureStaticVNetIP** cmdlet removes the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="7e1e9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e1e9-107">EXAMPLES</span></span>

### <span data-ttu-id="7e1e9-108">1:</span><span class="sxs-lookup"><span data-stu-id="7e1e9-108">1:</span></span>
```

```

## <span data-ttu-id="7e1e9-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e1e9-109">PARAMETERS</span></span>

### <span data-ttu-id="7e1e9-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7e1e9-110">-InformationAction</span></span>
<span data-ttu-id="7e1e9-111">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="7e1e9-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7e1e9-112">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7e1e9-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e1e9-113">Продолжал</span><span class="sxs-lookup"><span data-stu-id="7e1e9-113">Continue</span></span>
- <span data-ttu-id="7e1e9-114">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="7e1e9-114">Ignore</span></span>
- <span data-ttu-id="7e1e9-115">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="7e1e9-115">Inquire</span></span>
- <span data-ttu-id="7e1e9-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7e1e9-116">SilentlyContinue</span></span>
- <span data-ttu-id="7e1e9-117">Остановить</span><span class="sxs-lookup"><span data-stu-id="7e1e9-117">Stop</span></span>
- <span data-ttu-id="7e1e9-118">Рвать</span><span class="sxs-lookup"><span data-stu-id="7e1e9-118">Suspend</span></span>

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

### <span data-ttu-id="7e1e9-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7e1e9-119">-InformationVariable</span></span>
<span data-ttu-id="7e1e9-120">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="7e1e9-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7e1e9-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="7e1e9-121">-Profile</span></span>
<span data-ttu-id="7e1e9-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7e1e9-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e1e9-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e1e9-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e1e9-124">-VM</span><span class="sxs-lookup"><span data-stu-id="7e1e9-124">-VM</span></span>
<span data-ttu-id="7e1e9-125">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7e1e9-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="7e1e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1e9-126">CommonParameters</span></span>
<span data-ttu-id="7e1e9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e1e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1e9-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e1e9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1e9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e1e9-129">INPUTS</span></span>

## <span data-ttu-id="7e1e9-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e1e9-130">OUTPUTS</span></span>

## <span data-ttu-id="7e1e9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e1e9-131">NOTES</span></span>

## <span data-ttu-id="7e1e9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e1e9-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e1e9-133">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="7e1e9-133">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="7e1e9-134">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="7e1e9-134">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


