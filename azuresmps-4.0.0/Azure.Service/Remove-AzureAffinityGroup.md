---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076172"
---
# <span data-ttu-id="62935-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="62935-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="62935-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62935-102">SYNOPSIS</span></span>
<span data-ttu-id="62935-103">Удаляет территориальную группу в подписке.</span><span class="sxs-lookup"><span data-stu-id="62935-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="62935-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62935-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="62935-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62935-105">DESCRIPTION</span></span>
<span data-ttu-id="62935-106">Командлет **Remove-AzureAffinityGroup** удаляет территориальную группу Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="62935-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="62935-107">Вы не можете удалить территориальную группу, которая содержит каких – либо пользователей.</span><span class="sxs-lookup"><span data-stu-id="62935-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="62935-108">Сначала необходимо удалить всех участников территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="62935-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="62935-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62935-109">EXAMPLES</span></span>

### <span data-ttu-id="62935-110">Пример 1: удаление территориальной группы</span><span class="sxs-lookup"><span data-stu-id="62935-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="62935-111">Эта команда удаляет территориальную группу South01 в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="62935-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="62935-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62935-112">PARAMETERS</span></span>

### <span data-ttu-id="62935-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="62935-113">-InformationAction</span></span>
<span data-ttu-id="62935-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="62935-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="62935-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="62935-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62935-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="62935-116">Continue</span></span>
- <span data-ttu-id="62935-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="62935-117">Ignore</span></span>
- <span data-ttu-id="62935-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="62935-118">Inquire</span></span>
- <span data-ttu-id="62935-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="62935-119">SilentlyContinue</span></span>
- <span data-ttu-id="62935-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="62935-120">Stop</span></span>
- <span data-ttu-id="62935-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="62935-121">Suspend</span></span>

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

### <span data-ttu-id="62935-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="62935-122">-InformationVariable</span></span>
<span data-ttu-id="62935-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="62935-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="62935-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62935-124">-Name</span></span>
<span data-ttu-id="62935-125">Указывает имя территориальной группы, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="62935-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="62935-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="62935-126">-Profile</span></span>
<span data-ttu-id="62935-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="62935-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62935-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="62935-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62935-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62935-129">CommonParameters</span></span>
<span data-ttu-id="62935-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62935-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62935-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62935-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62935-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62935-132">INPUTS</span></span>

## <span data-ttu-id="62935-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62935-133">OUTPUTS</span></span>

## <span data-ttu-id="62935-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="62935-134">NOTES</span></span>

## <span data-ttu-id="62935-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62935-135">RELATED LINKS</span></span>

[<span data-ttu-id="62935-136">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="62935-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="62935-137">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="62935-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="62935-138">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="62935-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


