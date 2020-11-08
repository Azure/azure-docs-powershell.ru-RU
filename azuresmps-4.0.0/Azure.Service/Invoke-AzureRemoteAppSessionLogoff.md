---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076247"
---
# <span data-ttu-id="1aaea-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="1aaea-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="1aaea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1aaea-102">SYNOPSIS</span></span>
<span data-ttu-id="1aaea-103">Немедленно выходит за пределы сеанса Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1aaea-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="1aaea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1aaea-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aaea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aaea-105">DESCRIPTION</span></span>
<span data-ttu-id="1aaea-106">Командлет **Invoke-AzureRemoteAppSessionLogoff** немедленно завершает работу пользователя из удаленного сеанса, запущенного в Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1aaea-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="1aaea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1aaea-107">EXAMPLES</span></span>

### <span data-ttu-id="1aaea-108">Пример 1: выход из сеанса пользователя</span><span class="sxs-lookup"><span data-stu-id="1aaea-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="1aaea-109">Эта команда завершает работу пользователя, чей логин (UPN) PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="1aaea-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="1aaea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1aaea-110">PARAMETERS</span></span>

### <span data-ttu-id="1aaea-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="1aaea-111">-CollectionName</span></span>
<span data-ttu-id="1aaea-112">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1aaea-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="1aaea-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="1aaea-113">-Profile</span></span>
<span data-ttu-id="1aaea-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1aaea-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1aaea-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1aaea-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1aaea-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="1aaea-116">-UserUpn</span></span>
<span data-ttu-id="1aaea-117">Например, Specifes имя участника-пользователя (UPN) пользователя PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="1aaea-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="1aaea-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1aaea-118">-Confirm</span></span>
<span data-ttu-id="1aaea-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1aaea-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aaea-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aaea-120">-WhatIf</span></span>
<span data-ttu-id="1aaea-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1aaea-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aaea-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1aaea-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aaea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aaea-123">CommonParameters</span></span>
<span data-ttu-id="1aaea-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1aaea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aaea-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aaea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aaea-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1aaea-126">INPUTS</span></span>

## <span data-ttu-id="1aaea-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aaea-127">OUTPUTS</span></span>

## <span data-ttu-id="1aaea-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="1aaea-128">NOTES</span></span>

## <span data-ttu-id="1aaea-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1aaea-129">RELATED LINKS</span></span>

[<span data-ttu-id="1aaea-130">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="1aaea-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="1aaea-131">Разъединить — AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="1aaea-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="1aaea-132">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="1aaea-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)


