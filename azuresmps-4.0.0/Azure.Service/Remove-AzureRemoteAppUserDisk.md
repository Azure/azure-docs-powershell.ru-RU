---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076147"
---
# <span data-ttu-id="c65f7-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c65f7-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="c65f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c65f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c65f7-103">Удаляет пользовательский диск пользователя из коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c65f7-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c65f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c65f7-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c65f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c65f7-105">DESCRIPTION</span></span>
<span data-ttu-id="c65f7-106">Командлет **Remove-AzureRemoteAppUserDisk** удаляет пользовательский диск из коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c65f7-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="c65f7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c65f7-107">EXAMPLES</span></span>

### <span data-ttu-id="c65f7-108">Пример 1: удаление диска пользователя</span><span class="sxs-lookup"><span data-stu-id="c65f7-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="c65f7-109">Эта команда удаляет пользовательский диск пользователя Azure Active Directory с именем участника PattiFuller@contoso.com из коллекции Contoso01.</span><span class="sxs-lookup"><span data-stu-id="c65f7-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="c65f7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c65f7-110">PARAMETERS</span></span>

### <span data-ttu-id="c65f7-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="c65f7-111">-CollectionName</span></span>
<span data-ttu-id="c65f7-112">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c65f7-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65f7-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="c65f7-113">-Profile</span></span>
<span data-ttu-id="c65f7-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c65f7-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c65f7-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c65f7-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c65f7-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="c65f7-116">-UserUpn</span></span>
<span data-ttu-id="c65f7-117">Указывает имя участника-пользователя (UPN) пользователя, для которого этот командлет удаляет диск.</span><span class="sxs-lookup"><span data-stu-id="c65f7-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65f7-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c65f7-118">-Confirm</span></span>
<span data-ttu-id="c65f7-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c65f7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c65f7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c65f7-120">-WhatIf</span></span>
<span data-ttu-id="c65f7-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c65f7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c65f7-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c65f7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c65f7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65f7-123">CommonParameters</span></span>
<span data-ttu-id="c65f7-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c65f7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65f7-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65f7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65f7-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c65f7-126">INPUTS</span></span>

## <span data-ttu-id="c65f7-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c65f7-127">OUTPUTS</span></span>

## <span data-ttu-id="c65f7-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="c65f7-128">NOTES</span></span>

## <span data-ttu-id="c65f7-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c65f7-129">RELATED LINKS</span></span>

[<span data-ttu-id="c65f7-130">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c65f7-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


