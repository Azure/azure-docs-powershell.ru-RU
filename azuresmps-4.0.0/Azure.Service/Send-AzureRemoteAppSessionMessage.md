---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076433"
---
# <span data-ttu-id="ca97e-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="ca97e-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="ca97e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca97e-102">SYNOPSIS</span></span>
<span data-ttu-id="ca97e-103">Отправляет пользователю сообщение.</span><span class="sxs-lookup"><span data-stu-id="ca97e-103">Sends a message to a user.</span></span>

## <span data-ttu-id="ca97e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca97e-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ca97e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca97e-105">DESCRIPTION</span></span>
<span data-ttu-id="ca97e-106">Командлет **Send-AzureRemoteAppSessionMessage** отправляет сообщение пользователю, который подключен к сеансу RemoteApp из Azure.</span><span class="sxs-lookup"><span data-stu-id="ca97e-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="ca97e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca97e-107">EXAMPLES</span></span>

### <span data-ttu-id="ca97e-108">Пример 1: Отправка сообщения пользователю</span><span class="sxs-lookup"><span data-stu-id="ca97e-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="ca97e-109">Эта команда отправляет пользователю сообщение о том, что имя участника-пользователя PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="ca97e-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="ca97e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca97e-110">PARAMETERS</span></span>

### <span data-ttu-id="ca97e-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="ca97e-111">-CollectionName</span></span>
<span data-ttu-id="ca97e-112">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ca97e-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="ca97e-113">-Сообщение</span><span class="sxs-lookup"><span data-stu-id="ca97e-113">-Message</span></span>
<span data-ttu-id="ca97e-114">Указывает сообщение для отправки.</span><span class="sxs-lookup"><span data-stu-id="ca97e-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca97e-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="ca97e-115">-Profile</span></span>
<span data-ttu-id="ca97e-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ca97e-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca97e-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ca97e-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ca97e-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="ca97e-118">-UserUpn</span></span>
<span data-ttu-id="ca97e-119">Указывает имя участника-пользователя (UPN), например PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="ca97e-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="ca97e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca97e-120">CommonParameters</span></span>
<span data-ttu-id="ca97e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca97e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca97e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca97e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca97e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca97e-123">INPUTS</span></span>

## <span data-ttu-id="ca97e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca97e-124">OUTPUTS</span></span>

## <span data-ttu-id="ca97e-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca97e-125">NOTES</span></span>

## <span data-ttu-id="ca97e-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca97e-126">RELATED LINKS</span></span>

[<span data-ttu-id="ca97e-127">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="ca97e-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="ca97e-128">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="ca97e-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="ca97e-129">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="ca97e-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


