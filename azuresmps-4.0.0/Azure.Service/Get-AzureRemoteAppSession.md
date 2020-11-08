---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076577"
---
# <span data-ttu-id="78fad-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="78fad-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="78fad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78fad-102">SYNOPSIS</span></span>
<span data-ttu-id="78fad-103">Список всех активных и отключенных сеансов удаленных приложений Azure для коллекции.</span><span class="sxs-lookup"><span data-stu-id="78fad-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="78fad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78fad-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="78fad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78fad-105">DESCRIPTION</span></span>
<span data-ttu-id="78fad-106">Командлет **Get-AzureRemoteAppSession** перечисляет все активные и отключенные сеансы удаленных приложений Azure для коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="78fad-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="78fad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78fad-107">EXAMPLES</span></span>

### <span data-ttu-id="78fad-108">Пример 1: список всех сеансов в коллекции</span><span class="sxs-lookup"><span data-stu-id="78fad-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="78fad-109">Эта команда перечисляет все сеансы в коллекции Azure RemoteApp с именем ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="78fad-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="78fad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78fad-110">PARAMETERS</span></span>

### <span data-ttu-id="78fad-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="78fad-111">-CollectionName</span></span>
<span data-ttu-id="78fad-112">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="78fad-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="78fad-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="78fad-113">-Profile</span></span>
<span data-ttu-id="78fad-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="78fad-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78fad-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="78fad-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78fad-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="78fad-116">-UserUpn</span></span>
<span data-ttu-id="78fad-117">Указывает имя участника-пользователя (UPN) пользователя, для которого требуется получить сеансы RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="78fad-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="78fad-118">Например, имя участника-пользователя может быть представлено в следующем формате: PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="78fad-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="78fad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fad-119">CommonParameters</span></span>
<span data-ttu-id="78fad-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78fad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fad-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78fad-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fad-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78fad-122">INPUTS</span></span>

## <span data-ttu-id="78fad-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78fad-123">OUTPUTS</span></span>

## <span data-ttu-id="78fad-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="78fad-124">NOTES</span></span>

## <span data-ttu-id="78fad-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78fad-125">RELATED LINKS</span></span>

[<span data-ttu-id="78fad-126">Разъединить — AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="78fad-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="78fad-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="78fad-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="78fad-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="78fad-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


