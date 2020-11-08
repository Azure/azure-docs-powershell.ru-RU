---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076168"
---
# <span data-ttu-id="fcd0e-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fcd0e-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="fcd0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fcd0e-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd0e-103">Удаляет группу доступности из виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd0e-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="fcd0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fcd0e-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fcd0e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcd0e-105">DESCRIPTION</span></span>
<span data-ttu-id="fcd0e-106">Командлет **Remove-AzureAvailabilitySet** удаляет группу доступности из виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd0e-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="fcd0e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fcd0e-107">EXAMPLES</span></span>

### <span data-ttu-id="fcd0e-108">1:</span><span class="sxs-lookup"><span data-stu-id="fcd0e-108">1:</span></span>
```

```

## <span data-ttu-id="fcd0e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fcd0e-109">PARAMETERS</span></span>

### <span data-ttu-id="fcd0e-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fcd0e-110">-InformationAction</span></span>
<span data-ttu-id="fcd0e-111">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="fcd0e-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fcd0e-112">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fcd0e-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fcd0e-113">Продолжал</span><span class="sxs-lookup"><span data-stu-id="fcd0e-113">Continue</span></span>
- <span data-ttu-id="fcd0e-114">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="fcd0e-114">Ignore</span></span>
- <span data-ttu-id="fcd0e-115">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="fcd0e-115">Inquire</span></span>
- <span data-ttu-id="fcd0e-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fcd0e-116">SilentlyContinue</span></span>
- <span data-ttu-id="fcd0e-117">Остановить</span><span class="sxs-lookup"><span data-stu-id="fcd0e-117">Stop</span></span>
- <span data-ttu-id="fcd0e-118">Рвать</span><span class="sxs-lookup"><span data-stu-id="fcd0e-118">Suspend</span></span>

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

### <span data-ttu-id="fcd0e-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fcd0e-119">-InformationVariable</span></span>
<span data-ttu-id="fcd0e-120">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="fcd0e-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fcd0e-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="fcd0e-121">-Profile</span></span>
<span data-ttu-id="fcd0e-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fcd0e-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fcd0e-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fcd0e-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fcd0e-124">-VM</span><span class="sxs-lookup"><span data-stu-id="fcd0e-124">-VM</span></span>
<span data-ttu-id="fcd0e-125">Указывает виртуальную машину, с которой этот командлет удаляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="fcd0e-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

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

### <span data-ttu-id="fcd0e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd0e-126">CommonParameters</span></span>
<span data-ttu-id="fcd0e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fcd0e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd0e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd0e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd0e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fcd0e-129">INPUTS</span></span>

## <span data-ttu-id="fcd0e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcd0e-130">OUTPUTS</span></span>

## <span data-ttu-id="fcd0e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="fcd0e-131">NOTES</span></span>

## <span data-ttu-id="fcd0e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcd0e-132">RELATED LINKS</span></span>

[<span data-ttu-id="fcd0e-133">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fcd0e-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


