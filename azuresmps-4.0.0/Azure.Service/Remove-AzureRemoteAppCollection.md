---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8E67D1A4-4247-4603-8D26-42D6D48FE686
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90c654432760061d5c2ba36675c958135329b225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075868"
---
# <span data-ttu-id="70f5f-101">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="70f5f-101">Remove-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="70f5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="70f5f-103">Удаляет коллекцию Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="70f5f-103">Removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="70f5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70f5f-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppCollection [-CollectionName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70f5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="70f5f-106">Командлет **Remove-AzureRemoteAppCollection** удаляет коллекцию Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="70f5f-106">The **Remove-AzureRemoteAppCollection** cmdlet removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="70f5f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70f5f-107">EXAMPLES</span></span>

## <span data-ttu-id="70f5f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70f5f-108">PARAMETERS</span></span>

### <span data-ttu-id="70f5f-109">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="70f5f-109">-CollectionName</span></span>
<span data-ttu-id="70f5f-110">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="70f5f-110">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="70f5f-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="70f5f-111">-Profile</span></span>
<span data-ttu-id="70f5f-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="70f5f-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70f5f-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="70f5f-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70f5f-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70f5f-114">-Confirm</span></span>
<span data-ttu-id="70f5f-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70f5f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f5f-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f5f-116">-WhatIf</span></span>
<span data-ttu-id="70f5f-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70f5f-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70f5f-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70f5f-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f5f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f5f-119">CommonParameters</span></span>
<span data-ttu-id="70f5f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70f5f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f5f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f5f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f5f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70f5f-122">INPUTS</span></span>

## <span data-ttu-id="70f5f-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70f5f-123">OUTPUTS</span></span>

## <span data-ttu-id="70f5f-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="70f5f-124">NOTES</span></span>

## <span data-ttu-id="70f5f-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70f5f-125">RELATED LINKS</span></span>

[<span data-ttu-id="70f5f-126">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="70f5f-126">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="70f5f-127">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="70f5f-127">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="70f5f-128">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="70f5f-128">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="70f5f-129">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="70f5f-129">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


