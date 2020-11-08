---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075671"
---
# <span data-ttu-id="b1e2d-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="b1e2d-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="b1e2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e2d-103">Получает объект территориальной группы Azure.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="b1e2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1e2d-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b1e2d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1e2d-105">DESCRIPTION</span></span>
<span data-ttu-id="b1e2d-106">Командлет **Get-AzureAffinityGroup** получает территориальную группу Azure.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="b1e2d-107">Объект территориальной группы включает в себя название территориальной группы, расположение, метку, описание, а также хранилище и размещенные службы, являющиеся частью территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="b1e2d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1e2d-108">EXAMPLES</span></span>

### <span data-ttu-id="b1e2d-109">Пример 1: получение свойств территориальной группы</span><span class="sxs-lookup"><span data-stu-id="b1e2d-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="b1e2d-110">Эта команда получает свойства территориальной группы с именем South01.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="b1e2d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1e2d-111">PARAMETERS</span></span>

### <span data-ttu-id="b1e2d-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b1e2d-112">-InformationAction</span></span>
<span data-ttu-id="b1e2d-113">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b1e2d-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b1e2d-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1e2d-115">Продолжал</span><span class="sxs-lookup"><span data-stu-id="b1e2d-115">Continue</span></span>
- <span data-ttu-id="b1e2d-116">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="b1e2d-116">Ignore</span></span>
- <span data-ttu-id="b1e2d-117">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="b1e2d-117">Inquire</span></span>
- <span data-ttu-id="b1e2d-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b1e2d-118">SilentlyContinue</span></span>
- <span data-ttu-id="b1e2d-119">Остановить</span><span class="sxs-lookup"><span data-stu-id="b1e2d-119">Stop</span></span>
- <span data-ttu-id="b1e2d-120">Рвать</span><span class="sxs-lookup"><span data-stu-id="b1e2d-120">Suspend</span></span>

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

### <span data-ttu-id="b1e2d-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b1e2d-121">-InformationVariable</span></span>
<span data-ttu-id="b1e2d-122">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b1e2d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b1e2d-123">-Name</span></span>
<span data-ttu-id="b1e2d-124">Указывает имя территориальной группы, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="b1e2d-125">Имена для территориальных групп, созданных с помощью портала управления, обычно являются идентификаторами GUID.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="b1e2d-126">Порт управления показывает метку территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-126">The Management Port shows the affinity group label.</span></span>

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

### <span data-ttu-id="b1e2d-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1e2d-127">-Profile</span></span>
<span data-ttu-id="b1e2d-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1e2d-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1e2d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e2d-130">CommonParameters</span></span>
<span data-ttu-id="b1e2d-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1e2d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e2d-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1e2d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e2d-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1e2d-133">INPUTS</span></span>

## <span data-ttu-id="b1e2d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1e2d-134">OUTPUTS</span></span>

### <span data-ttu-id="b1e2d-135">AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="b1e2d-135">AffinityGroup</span></span>

## <span data-ttu-id="b1e2d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1e2d-136">NOTES</span></span>

## <span data-ttu-id="b1e2d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1e2d-137">RELATED LINKS</span></span>

[<span data-ttu-id="b1e2d-138">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="b1e2d-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="b1e2d-139">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="b1e2d-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="b1e2d-140">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="b1e2d-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


