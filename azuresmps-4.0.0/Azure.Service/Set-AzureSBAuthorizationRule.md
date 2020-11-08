---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075820"
---
# <span data-ttu-id="37487-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="37487-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="37487-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37487-102">SYNOPSIS</span></span>
<span data-ttu-id="37487-103">Обновляет действующее правило авторизации служебной шины.</span><span class="sxs-lookup"><span data-stu-id="37487-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="37487-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37487-104">SYNTAX</span></span>

### <span data-ttu-id="37487-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="37487-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="37487-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="37487-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37487-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37487-107">DESCRIPTION</span></span>
<span data-ttu-id="37487-108">Обновляет действующее правило авторизации служебной шины.</span><span class="sxs-lookup"><span data-stu-id="37487-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="37487-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37487-109">EXAMPLES</span></span>

### <span data-ttu-id="37487-110">Пример 1: обновление первичного ключа для правила авторизации на уровне пространства имен</span><span class="sxs-lookup"><span data-stu-id="37487-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="37487-111">Будет обновлен первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="37487-111">The primary key is renewed.</span></span>

### <span data-ttu-id="37487-112">Пример 2: обновление разрешения правила авторизации</span><span class="sxs-lookup"><span data-stu-id="37487-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="37487-113">Обновляет разрешения.</span><span class="sxs-lookup"><span data-stu-id="37487-113">Updates the permissions.</span></span>

## <span data-ttu-id="37487-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37487-114">PARAMETERS</span></span>

### <span data-ttu-id="37487-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="37487-115">-EntityName</span></span>
<span data-ttu-id="37487-116">Имя сущности, к которой нужно применить правило.</span><span class="sxs-lookup"><span data-stu-id="37487-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="37487-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="37487-117">-EntityType</span></span>
<span data-ttu-id="37487-118">Тип сущности (очередь, тема, ретрансляция, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="37487-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="37487-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37487-119">-Name</span></span>
<span data-ttu-id="37487-120">Уникальное имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="37487-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="37487-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="37487-121">-Namespace</span></span>
<span data-ttu-id="37487-122">Имя пространства имен для применения правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="37487-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="37487-123">Если не указано ни одного EntityName, правило будет находиться на уровне пространства имен.</span><span class="sxs-lookup"><span data-stu-id="37487-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="37487-124">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="37487-124">-Permission</span></span>
<span data-ttu-id="37487-125">Разрешения на авторизацию ("Отправить", "Управление", "прослушать").</span><span class="sxs-lookup"><span data-stu-id="37487-125">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37487-126">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="37487-126">-PrimaryKey</span></span>
<span data-ttu-id="37487-127">Первичный ключ подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="37487-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="37487-128">Будет создаваться, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="37487-128">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="37487-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="37487-129">-Profile</span></span>
<span data-ttu-id="37487-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="37487-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37487-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37487-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37487-132">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="37487-132">-SecondaryKey</span></span>
<span data-ttu-id="37487-133">Вторичный ключ подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="37487-133">The Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="37487-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37487-134">CommonParameters</span></span>
<span data-ttu-id="37487-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37487-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37487-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37487-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37487-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37487-137">INPUTS</span></span>

## <span data-ttu-id="37487-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37487-138">OUTPUTS</span></span>

## <span data-ttu-id="37487-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="37487-139">NOTES</span></span>

## <span data-ttu-id="37487-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37487-140">RELATED LINKS</span></span>

[<span data-ttu-id="37487-141">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="37487-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="37487-142">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="37487-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="37487-143">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="37487-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


