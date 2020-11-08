---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075866"
---
# <span data-ttu-id="db29e-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="db29e-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="db29e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db29e-102">SYNOPSIS</span></span>
<span data-ttu-id="db29e-103">Удаление пользователя из коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="db29e-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="db29e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db29e-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db29e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db29e-105">DESCRIPTION</span></span>
<span data-ttu-id="db29e-106">Командлет **Remove-AzureRemoteAppUser** удаляет пользователя из коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="db29e-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="db29e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db29e-107">EXAMPLES</span></span>

### <span data-ttu-id="db29e-108">Example1: Удаление пользователя из коллекции</span><span class="sxs-lookup"><span data-stu-id="db29e-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="db29e-109">Эта команда удаляет пользователя Azure ActiveDirectory PattiFuller@contoso.com из коллекции contoso.</span><span class="sxs-lookup"><span data-stu-id="db29e-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="db29e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db29e-110">PARAMETERS</span></span>

### <span data-ttu-id="db29e-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="db29e-111">-Alias</span></span>
<span data-ttu-id="db29e-112">Указывает опубликованный псевдоним программы.</span><span class="sxs-lookup"><span data-stu-id="db29e-112">Specifies a published program alias.</span></span>
<span data-ttu-id="db29e-113">Этот параметр можно использовать только в режиме публикации для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="db29e-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="db29e-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="db29e-114">-CollectionName</span></span>
<span data-ttu-id="db29e-115">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="db29e-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="db29e-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="db29e-116">-Profile</span></span>
<span data-ttu-id="db29e-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="db29e-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db29e-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db29e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db29e-119">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="db29e-119">-Type</span></span>
<span data-ttu-id="db29e-120">Указывает тип пользователя.</span><span class="sxs-lookup"><span data-stu-id="db29e-120">Specifies a user type.</span></span>
<span data-ttu-id="db29e-121">Допустимые значения этого параметра: OrgId или учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="db29e-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="db29e-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="db29e-122">-UserUpn</span></span>
<span data-ttu-id="db29e-123">Указывает имя участника-пользователя (UPN), например user@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="db29e-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

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

### <span data-ttu-id="db29e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db29e-124">CommonParameters</span></span>
<span data-ttu-id="db29e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db29e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db29e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db29e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db29e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db29e-127">INPUTS</span></span>

## <span data-ttu-id="db29e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db29e-128">OUTPUTS</span></span>

## <span data-ttu-id="db29e-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="db29e-129">NOTES</span></span>

## <span data-ttu-id="db29e-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db29e-130">RELATED LINKS</span></span>

[<span data-ttu-id="db29e-131">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="db29e-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="db29e-132">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="db29e-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


