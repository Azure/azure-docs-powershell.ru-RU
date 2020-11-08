---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075987"
---
# <span data-ttu-id="fbf87-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbf87-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="fbf87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbf87-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf87-103">Создает новое правило авторизации служебной шины.</span><span class="sxs-lookup"><span data-stu-id="fbf87-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="fbf87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbf87-104">SYNTAX</span></span>

### <span data-ttu-id="fbf87-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="fbf87-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fbf87-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="fbf87-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fbf87-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbf87-107">DESCRIPTION</span></span>
<span data-ttu-id="fbf87-108">Командлет **New-AzureSBAuthorizationRule** создает правило авторизации служебной шины.</span><span class="sxs-lookup"><span data-stu-id="fbf87-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="fbf87-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbf87-109">EXAMPLES</span></span>

### <span data-ttu-id="fbf87-110">Пример 1: Создание правила авторизации с помощью созданного первичного ключа</span><span class="sxs-lookup"><span data-stu-id="fbf87-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="fbf87-111">Создает новое правило авторизации на уровне пространства имен с разрешением Send.</span><span class="sxs-lookup"><span data-stu-id="fbf87-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="fbf87-112">Пример 2: Создание правила авторизации, предоставляя первичный ключ</span><span class="sxs-lookup"><span data-stu-id="fbf87-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="fbf87-113">Создает новое правило авторизации на уровне очереди MyEntity со всеми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="fbf87-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="fbf87-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbf87-114">PARAMETERS</span></span>

### <span data-ttu-id="fbf87-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="fbf87-115">-EntityName</span></span>
<span data-ttu-id="fbf87-116">Указывает имя сущности, к которой нужно применить правило.</span><span class="sxs-lookup"><span data-stu-id="fbf87-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf87-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="fbf87-117">-EntityType</span></span>
<span data-ttu-id="fbf87-118">Указывает тип сущности.</span><span class="sxs-lookup"><span data-stu-id="fbf87-118">Specifies the entity type.</span></span>
<span data-ttu-id="fbf87-119">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="fbf87-119">Valid values are:</span></span>
  
- <span data-ttu-id="fbf87-120">Поместить</span><span class="sxs-lookup"><span data-stu-id="fbf87-120">Queue</span></span>
- <span data-ttu-id="fbf87-121">Разделе</span><span class="sxs-lookup"><span data-stu-id="fbf87-121">Topic</span></span>
- <span data-ttu-id="fbf87-122">Сылки</span><span class="sxs-lookup"><span data-stu-id="fbf87-122">Relay</span></span>
- <span data-ttu-id="fbf87-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="fbf87-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf87-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fbf87-124">-Name</span></span>
<span data-ttu-id="fbf87-125">Определяет уникальное имя правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="fbf87-125">Specifies the unique authorization rule name.</span></span>

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

### <span data-ttu-id="fbf87-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fbf87-126">-Namespace</span></span>
<span data-ttu-id="fbf87-127">Задает имя пространства имен для применения правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="fbf87-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="fbf87-128">Если не указано ни одного *EntityName* , правило будет находиться на уровне пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fbf87-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="fbf87-129">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="fbf87-129">-Permission</span></span>
<span data-ttu-id="fbf87-130">Разрешения на авторизацию ("Отправить", "Управление", "прослушать").</span><span class="sxs-lookup"><span data-stu-id="fbf87-130">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="fbf87-131">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="fbf87-131">-PrimaryKey</span></span>
<span data-ttu-id="fbf87-132">Задает первичный ключ подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="fbf87-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="fbf87-133">Будет создаваться, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="fbf87-133">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="fbf87-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="fbf87-134">-Profile</span></span>
<span data-ttu-id="fbf87-135">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fbf87-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fbf87-136">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbf87-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fbf87-137">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="fbf87-137">-SecondaryKey</span></span>
<span data-ttu-id="fbf87-138">Задает вторичный ключ подписи для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="fbf87-138">Specifies the Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="fbf87-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf87-139">CommonParameters</span></span>
<span data-ttu-id="fbf87-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbf87-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf87-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbf87-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf87-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbf87-142">INPUTS</span></span>

## <span data-ttu-id="fbf87-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbf87-143">OUTPUTS</span></span>

## <span data-ttu-id="fbf87-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbf87-144">NOTES</span></span>

## <span data-ttu-id="fbf87-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbf87-145">RELATED LINKS</span></span>

[<span data-ttu-id="fbf87-146">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbf87-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="fbf87-147">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbf87-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="fbf87-148">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbf87-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


