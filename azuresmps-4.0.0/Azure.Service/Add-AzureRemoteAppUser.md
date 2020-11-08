---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076381"
---
# <span data-ttu-id="3f736-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="3f736-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="3f736-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f736-102">SYNOPSIS</span></span>
<span data-ttu-id="3f736-103">Добавляет пользователя в коллекцию Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3f736-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3f736-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f736-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f736-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f736-105">DESCRIPTION</span></span>
<span data-ttu-id="3f736-106">Командлет **Add-AzureRemoteAppUser** добавляет пользователя в коллекцию Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3f736-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3f736-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f736-107">EXAMPLES</span></span>

### <span data-ttu-id="3f736-108">Пример 1: Добавление пользователя с помощью учетной записи Майкрософт</span><span class="sxs-lookup"><span data-stu-id="3f736-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="3f736-109">Эта команда добавляет учетную запись Майкрософт PattiFuller@contoso.com в коллекцию с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="3f736-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="3f736-110">Пример 2: Добавление пользователя с помощью учетной записи Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3f736-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="3f736-111">Эта команда добавляет учетную запись Azure Active Directory PattiFuller@contoso.com в коллекцию с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="3f736-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="3f736-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f736-112">PARAMETERS</span></span>

### <span data-ttu-id="3f736-113">-Alias</span><span class="sxs-lookup"><span data-stu-id="3f736-113">-Alias</span></span>
<span data-ttu-id="3f736-114">Указывает опубликованный псевдоним программы.</span><span class="sxs-lookup"><span data-stu-id="3f736-114">Specifies a published program alias.</span></span>
<span data-ttu-id="3f736-115">Этот параметр можно использовать только в режиме публикации для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="3f736-115">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="3f736-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3f736-116">-CollectionName</span></span>
<span data-ttu-id="3f736-117">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3f736-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="3f736-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="3f736-118">-Profile</span></span>
<span data-ttu-id="3f736-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3f736-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f736-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3f736-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f736-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="3f736-121">-Type</span></span>
<span data-ttu-id="3f736-122">Указывает тип пользователя.</span><span class="sxs-lookup"><span data-stu-id="3f736-122">Specifies a user type.</span></span>
<span data-ttu-id="3f736-123">Допустимые значения этого параметра: OrgId или учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3f736-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f736-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="3f736-124">-UserUpn</span></span>
<span data-ttu-id="3f736-125">Указывает имя участника-пользователя (UPN), например PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="3f736-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f736-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f736-126">CommonParameters</span></span>
<span data-ttu-id="3f736-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f736-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f736-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f736-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f736-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f736-129">INPUTS</span></span>

## <span data-ttu-id="3f736-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f736-130">OUTPUTS</span></span>

## <span data-ttu-id="3f736-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f736-131">NOTES</span></span>

## <span data-ttu-id="3f736-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f736-132">RELATED LINKS</span></span>

[<span data-ttu-id="3f736-133">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="3f736-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="3f736-134">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="3f736-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


