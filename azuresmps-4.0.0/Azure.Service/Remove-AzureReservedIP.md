---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076145"
---
# <span data-ttu-id="585be-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="585be-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="585be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="585be-102">SYNOPSIS</span></span>
<span data-ttu-id="585be-103">Удаляет зарезервированный IP-адрес по его имени.</span><span class="sxs-lookup"><span data-stu-id="585be-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="585be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="585be-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="585be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="585be-105">DESCRIPTION</span></span>
<span data-ttu-id="585be-106">Командлет **Remove-AzureReservedIP** удаляет зарезервированный IP-адрес по его имени.</span><span class="sxs-lookup"><span data-stu-id="585be-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="585be-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="585be-107">EXAMPLES</span></span>

### <span data-ttu-id="585be-108">Пример 1: удаление зарезервированного IP-адреса с помощью его имени</span><span class="sxs-lookup"><span data-stu-id="585be-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="585be-109">Эта команда удаляет зарезервированный IP-адрес по его имени.</span><span class="sxs-lookup"><span data-stu-id="585be-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="585be-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="585be-110">PARAMETERS</span></span>

### <span data-ttu-id="585be-111">-Force</span><span class="sxs-lookup"><span data-stu-id="585be-111">-Force</span></span>
<span data-ttu-id="585be-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="585be-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585be-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="585be-113">-InformationAction</span></span>
<span data-ttu-id="585be-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="585be-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="585be-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="585be-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="585be-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="585be-116">Continue</span></span>
- <span data-ttu-id="585be-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="585be-117">Ignore</span></span>
- <span data-ttu-id="585be-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="585be-118">Inquire</span></span>
- <span data-ttu-id="585be-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="585be-119">SilentlyContinue</span></span>
- <span data-ttu-id="585be-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="585be-120">Stop</span></span>
- <span data-ttu-id="585be-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="585be-121">Suspend</span></span>

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

### <span data-ttu-id="585be-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="585be-122">-InformationVariable</span></span>
<span data-ttu-id="585be-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="585be-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="585be-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="585be-124">-Profile</span></span>
<span data-ttu-id="585be-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="585be-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="585be-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="585be-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="585be-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="585be-127">-ReservedIPName</span></span>
<span data-ttu-id="585be-128">Задает имя зарезервированного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="585be-128">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="585be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585be-129">CommonParameters</span></span>
<span data-ttu-id="585be-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="585be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585be-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="585be-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585be-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="585be-132">INPUTS</span></span>

## <span data-ttu-id="585be-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="585be-133">OUTPUTS</span></span>

## <span data-ttu-id="585be-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="585be-134">NOTES</span></span>

## <span data-ttu-id="585be-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="585be-135">RELATED LINKS</span></span>

[<span data-ttu-id="585be-136">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="585be-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="585be-137">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="585be-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="585be-138">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="585be-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


