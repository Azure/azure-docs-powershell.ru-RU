---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075614"
---
# <span data-ttu-id="3b9d3-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3b9d3-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="3b9d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9d3-103">Получает правила авторизации служебной шины.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="3b9d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b9d3-104">SYNTAX</span></span>

### <span data-ttu-id="3b9d3-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="3b9d3-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3b9d3-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="3b9d3-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3b9d3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b9d3-107">DESCRIPTION</span></span>
<span data-ttu-id="3b9d3-108">Получает правила авторизации служебной шины.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="3b9d3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b9d3-109">EXAMPLES</span></span>

### <span data-ttu-id="3b9d3-110">Пример 1: получение правила авторизации на уровне пространства имен</span><span class="sxs-lookup"><span data-stu-id="3b9d3-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="3b9d3-111">Получает все доступные правила авторизации в MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="3b9d3-112">Пример 2: получение правила авторизации для очереди</span><span class="sxs-lookup"><span data-stu-id="3b9d3-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="3b9d3-113">Получает все доступные правила авторизации, MyEntity очередь на MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="3b9d3-114">Пример 3: получение правила авторизации по имени</span><span class="sxs-lookup"><span data-stu-id="3b9d3-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="3b9d3-115">Возвращает правило авторизации, именуемое MyRule на уровне MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="3b9d3-116">Пример 4: получение правила авторизации по разрешениям</span><span class="sxs-lookup"><span data-stu-id="3b9d3-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="3b9d3-117">Получает все правила авторизации, у которых есть разрешение на отправку на уровне пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="3b9d3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b9d3-118">PARAMETERS</span></span>

### <span data-ttu-id="3b9d3-119">-EntityName</span><span class="sxs-lookup"><span data-stu-id="3b9d3-119">-EntityName</span></span>
<span data-ttu-id="3b9d3-120">Имя сущности, к которой нужно применить правило.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-120">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="3b9d3-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="3b9d3-121">-EntityType</span></span>
<span data-ttu-id="3b9d3-122">Тип сущности (очередь, тема, ретрансляция, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="3b9d3-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="3b9d3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b9d3-123">-Name</span></span>
<span data-ttu-id="3b9d3-124">Уникальное имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-124">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3b9d3-125">-Namespace</span></span>
<span data-ttu-id="3b9d3-126">Имя пространства имен для применения правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="3b9d3-127">Если не указано ни одного EntityName, правило будет находиться на уровне пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-127">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="3b9d3-128">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="3b9d3-128">-Permission</span></span>
<span data-ttu-id="3b9d3-129">Разрешения на отправку данных, которые нужно отфильтровать (отправить, управлять и прослушать).</span><span class="sxs-lookup"><span data-stu-id="3b9d3-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="3b9d3-130">Используется точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="3b9d3-131">-Profile</span></span>
<span data-ttu-id="3b9d3-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b9d3-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b9d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9d3-134">CommonParameters</span></span>
<span data-ttu-id="3b9d3-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9d3-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b9d3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9d3-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b9d3-137">INPUTS</span></span>

## <span data-ttu-id="3b9d3-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b9d3-138">OUTPUTS</span></span>

## <span data-ttu-id="3b9d3-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b9d3-139">NOTES</span></span>

## <span data-ttu-id="3b9d3-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b9d3-140">RELATED LINKS</span></span>

[<span data-ttu-id="3b9d3-141">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3b9d3-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="3b9d3-142">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3b9d3-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="3b9d3-143">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3b9d3-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


