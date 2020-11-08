---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076316"
---
# <span data-ttu-id="b1442-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="b1442-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="b1442-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1442-102">SYNOPSIS</span></span>
<span data-ttu-id="b1442-103">Выводит список пользователей в коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b1442-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="b1442-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1442-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1442-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1442-105">DESCRIPTION</span></span>
<span data-ttu-id="b1442-106">Командлет **Get-AzureRemoteAppUser** перечисляет пользователей в коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b1442-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="b1442-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1442-107">EXAMPLES</span></span>

### <span data-ttu-id="b1442-108">Пример 1: список пользователей коллекции</span><span class="sxs-lookup"><span data-stu-id="b1442-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="b1442-109">В этой команде перечислены пользователи, у которых есть доступ к коллекции Azure RemoteApp с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="b1442-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="b1442-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1442-110">PARAMETERS</span></span>

### <span data-ttu-id="b1442-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="b1442-111">-Alias</span></span>
<span data-ttu-id="b1442-112">Указывает опубликованный псевдоним программы.</span><span class="sxs-lookup"><span data-stu-id="b1442-112">Specifies a published program alias.</span></span>
<span data-ttu-id="b1442-113">Этот параметр можно использовать только в режиме публикации для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="b1442-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="b1442-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="b1442-114">-CollectionName</span></span>
<span data-ttu-id="b1442-115">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b1442-115">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1442-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1442-116">-Profile</span></span>
<span data-ttu-id="b1442-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b1442-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1442-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1442-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1442-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="b1442-119">-UserUpn</span></span>
<span data-ttu-id="b1442-120">Указывает имя участника-пользователя (UPN) пользователя, сведения о котором нужно вывести.</span><span class="sxs-lookup"><span data-stu-id="b1442-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="b1442-121">Например, PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="b1442-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="b1442-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1442-122">CommonParameters</span></span>
<span data-ttu-id="b1442-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1442-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1442-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1442-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1442-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1442-125">INPUTS</span></span>

## <span data-ttu-id="b1442-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1442-126">OUTPUTS</span></span>

## <span data-ttu-id="b1442-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1442-127">NOTES</span></span>

## <span data-ttu-id="b1442-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1442-128">RELATED LINKS</span></span>

[<span data-ttu-id="b1442-129">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="b1442-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="b1442-130">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="b1442-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="b1442-131">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="b1442-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


