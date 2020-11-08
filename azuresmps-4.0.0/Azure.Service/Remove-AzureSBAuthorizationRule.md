---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076131"
---
# <span data-ttu-id="677ac-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="677ac-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="677ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="677ac-102">SYNOPSIS</span></span>
<span data-ttu-id="677ac-103">Удаление существующего правила авторизации служебной шины.</span><span class="sxs-lookup"><span data-stu-id="677ac-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="677ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="677ac-104">SYNTAX</span></span>

### <span data-ttu-id="677ac-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="677ac-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="677ac-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="677ac-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="677ac-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="677ac-107">DESCRIPTION</span></span>
<span data-ttu-id="677ac-108">Удаление существующего правила авторизации служебной шины.</span><span class="sxs-lookup"><span data-stu-id="677ac-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="677ac-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="677ac-109">EXAMPLES</span></span>

### <span data-ttu-id="677ac-110">Пример 1: Удаление правила авторизации на уровне пространства имен</span><span class="sxs-lookup"><span data-stu-id="677ac-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="677ac-111">Удаляет правило авторизации MyRule из MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="677ac-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="677ac-112">Пример 2: Удаление правила авторизации для очереди</span><span class="sxs-lookup"><span data-stu-id="677ac-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="677ac-113">Удаляет правило авторизации, именуемое MyRule, для очереди MyEntity в MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="677ac-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="677ac-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="677ac-114">PARAMETERS</span></span>

### <span data-ttu-id="677ac-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="677ac-115">-EntityName</span></span>
<span data-ttu-id="677ac-116">Имя сущности, к которой нужно применить правило.</span><span class="sxs-lookup"><span data-stu-id="677ac-116">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677ac-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="677ac-117">-EntityType</span></span>
<span data-ttu-id="677ac-118">Тип сущности (очередь, тема, ретрансляция, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="677ac-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677ac-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="677ac-119">-Name</span></span>
<span data-ttu-id="677ac-120">Уникальное имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="677ac-120">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677ac-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="677ac-121">-Namespace</span></span>
<span data-ttu-id="677ac-122">Имя пространства имен для применения правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="677ac-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="677ac-123">Если не указано ни одного EntityName, правило будет находиться на уровне пространства имен.</span><span class="sxs-lookup"><span data-stu-id="677ac-123">If no EntityName provided the rule will be on the namespace level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677ac-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="677ac-124">-PassThru</span></span>
<span data-ttu-id="677ac-125">Указывает на то, что этот командлет возвращает объект, представляющий элемент, на котором оно работает.</span><span class="sxs-lookup"><span data-stu-id="677ac-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="677ac-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="677ac-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677ac-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="677ac-127">-Profile</span></span>
<span data-ttu-id="677ac-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="677ac-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="677ac-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="677ac-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="677ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677ac-130">CommonParameters</span></span>
<span data-ttu-id="677ac-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="677ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677ac-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="677ac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677ac-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="677ac-133">INPUTS</span></span>

## <span data-ttu-id="677ac-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="677ac-134">OUTPUTS</span></span>

## <span data-ttu-id="677ac-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="677ac-135">NOTES</span></span>

## <span data-ttu-id="677ac-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="677ac-136">RELATED LINKS</span></span>

[<span data-ttu-id="677ac-137">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="677ac-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="677ac-138">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="677ac-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="677ac-139">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="677ac-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


