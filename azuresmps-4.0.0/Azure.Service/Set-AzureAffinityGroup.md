---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076431"
---
# <span data-ttu-id="80cc9-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="80cc9-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="80cc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="80cc9-103">Изменяет свойства территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="80cc9-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="80cc9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80cc9-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="80cc9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80cc9-105">DESCRIPTION</span></span>
<span data-ttu-id="80cc9-106">Командлет **Set-AzureAffinityGroup** изменяет свойства территориальной группы Azure.</span><span class="sxs-lookup"><span data-stu-id="80cc9-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="80cc9-107">Вы можете изменить метку и описание.</span><span class="sxs-lookup"><span data-stu-id="80cc9-107">You can change the label and the description.</span></span>

## <span data-ttu-id="80cc9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80cc9-108">EXAMPLES</span></span>

### <span data-ttu-id="80cc9-109">Пример 1: изменение территориальной группы</span><span class="sxs-lookup"><span data-stu-id="80cc9-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="80cc9-110">Эта команда изменяет метку территориальной группы с именем South01 на SouthUSProduction, она также изменяет описание.</span><span class="sxs-lookup"><span data-stu-id="80cc9-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="80cc9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80cc9-111">PARAMETERS</span></span>

### <span data-ttu-id="80cc9-112">-Описание</span><span class="sxs-lookup"><span data-stu-id="80cc9-112">-Description</span></span>
<span data-ttu-id="80cc9-113">Задает описание территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="80cc9-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="80cc9-114">Описание может иметь длину до 1024 символов.</span><span class="sxs-lookup"><span data-stu-id="80cc9-114">The description can be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80cc9-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="80cc9-115">-InformationAction</span></span>
<span data-ttu-id="80cc9-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="80cc9-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80cc9-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="80cc9-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80cc9-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="80cc9-118">Continue</span></span>
- <span data-ttu-id="80cc9-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="80cc9-119">Ignore</span></span>
- <span data-ttu-id="80cc9-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="80cc9-120">Inquire</span></span>
- <span data-ttu-id="80cc9-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="80cc9-121">SilentlyContinue</span></span>
- <span data-ttu-id="80cc9-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="80cc9-122">Stop</span></span>
- <span data-ttu-id="80cc9-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="80cc9-123">Suspend</span></span>

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

### <span data-ttu-id="80cc9-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="80cc9-124">-InformationVariable</span></span>
<span data-ttu-id="80cc9-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="80cc9-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="80cc9-126">-Label</span><span class="sxs-lookup"><span data-stu-id="80cc9-126">-Label</span></span>
<span data-ttu-id="80cc9-127">Указывает метку для территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="80cc9-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="80cc9-128">Метка может иметь длину до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="80cc9-128">The label can be up to 100 characters long.</span></span>

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

### <span data-ttu-id="80cc9-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80cc9-129">-Name</span></span>
<span data-ttu-id="80cc9-130">Указывает имя территориальной группы, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="80cc9-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="80cc9-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="80cc9-131">-Profile</span></span>
<span data-ttu-id="80cc9-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="80cc9-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80cc9-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="80cc9-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80cc9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80cc9-134">CommonParameters</span></span>
<span data-ttu-id="80cc9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80cc9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80cc9-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80cc9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80cc9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80cc9-137">INPUTS</span></span>

## <span data-ttu-id="80cc9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80cc9-138">OUTPUTS</span></span>

## <span data-ttu-id="80cc9-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="80cc9-139">NOTES</span></span>

## <span data-ttu-id="80cc9-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80cc9-140">RELATED LINKS</span></span>

[<span data-ttu-id="80cc9-141">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="80cc9-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="80cc9-142">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="80cc9-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="80cc9-143">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="80cc9-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


