---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075686"
---
# <span data-ttu-id="25008-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="25008-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="25008-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25008-102">SYNOPSIS</span></span>
<span data-ttu-id="25008-103">Отключение сеанса RemoteApp для Azure.</span><span class="sxs-lookup"><span data-stu-id="25008-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="25008-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25008-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="25008-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25008-105">DESCRIPTION</span></span>
<span data-ttu-id="25008-106">Командлет **Disconnect-AzureRemoteAppSession** отключает сеанс приложения RemoteApp для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="25008-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="25008-107">Клиент пользователя отключается из сеанса Azure RemoteApp, но программы пользователя продолжают работать.</span><span class="sxs-lookup"><span data-stu-id="25008-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="25008-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25008-108">EXAMPLES</span></span>

### <span data-ttu-id="25008-109">Пример 1: Отключение сеанса пользователя</span><span class="sxs-lookup"><span data-stu-id="25008-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="25008-110">Эта команда отключает сеанс Azure RemoteApp в коллекции ContosoApps для пользователя, чей логин (UPN) PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="25008-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="25008-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25008-111">PARAMETERS</span></span>

### <span data-ttu-id="25008-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="25008-112">-CollectionName</span></span>
<span data-ttu-id="25008-113">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="25008-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="25008-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="25008-114">-Profile</span></span>
<span data-ttu-id="25008-115">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="25008-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25008-116">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25008-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25008-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="25008-117">-UserUpn</span></span>
<span data-ttu-id="25008-118">Указывает имя участника-пользователя (UPN), например PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="25008-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25008-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25008-119">CommonParameters</span></span>
<span data-ttu-id="25008-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25008-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25008-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25008-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25008-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25008-122">INPUTS</span></span>

## <span data-ttu-id="25008-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25008-123">OUTPUTS</span></span>

## <span data-ttu-id="25008-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="25008-124">NOTES</span></span>

## <span data-ttu-id="25008-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25008-125">RELATED LINKS</span></span>

[<span data-ttu-id="25008-126">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="25008-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="25008-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="25008-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="25008-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="25008-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


