---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075737"
---
# <span data-ttu-id="87bf8-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="87bf8-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="87bf8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="87bf8-103">Обновляет коллекцию RemoteApp Azure с новым образом шаблона.</span><span class="sxs-lookup"><span data-stu-id="87bf8-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="87bf8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87bf8-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87bf8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="87bf8-106">Командлет **Update-AzureRemoteAppCollection** обновляет коллекцию Azure RemoteApp с помощью нового образа шаблона.</span><span class="sxs-lookup"><span data-stu-id="87bf8-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="87bf8-107">После завершения обновления пользователи с существующими сеансами выйдет через один час, прежде чем они будут автоматически выходить. При повторном входе они подключаются к недавно обновленной коллекции.</span><span class="sxs-lookup"><span data-stu-id="87bf8-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="87bf8-108">Чтобы принудительно вынудить пользователей выйти сразу после обновления коллекции, укажите параметр *ForceLogoffWhenUpdateComplete* .</span><span class="sxs-lookup"><span data-stu-id="87bf8-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="87bf8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87bf8-109">EXAMPLES</span></span>

## <span data-ttu-id="87bf8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87bf8-110">PARAMETERS</span></span>

### <span data-ttu-id="87bf8-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="87bf8-111">-CollectionName</span></span>
<span data-ttu-id="87bf8-112">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="87bf8-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="87bf8-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="87bf8-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="87bf8-114">Указывает на то, что этот командлет регистрирует пользователей из существующих сеансов сразу после завершения обновления.</span><span class="sxs-lookup"><span data-stu-id="87bf8-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="87bf8-115">После повторного входа пользователей они подключаются к недавно обновленной коллекции.</span><span class="sxs-lookup"><span data-stu-id="87bf8-115">When users sign in again, they connect to the newly updated collection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87bf8-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="87bf8-116">-ImageName</span></span>
<span data-ttu-id="87bf8-117">Указывает имя образа шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="87bf8-117">Specifies the name of an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="87bf8-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="87bf8-118">-Profile</span></span>
<span data-ttu-id="87bf8-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="87bf8-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87bf8-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87bf8-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87bf8-121">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="87bf8-121">-SubnetName</span></span>
<span data-ttu-id="87bf8-122">Указывает имя подсети, в которую нужно переместить коллекцию.</span><span class="sxs-lookup"><span data-stu-id="87bf8-122">Specifies the name of the subnet into which to move the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87bf8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87bf8-123">-Confirm</span></span>
<span data-ttu-id="87bf8-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87bf8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87bf8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87bf8-125">-WhatIf</span></span>
<span data-ttu-id="87bf8-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87bf8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87bf8-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87bf8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87bf8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87bf8-128">CommonParameters</span></span>
<span data-ttu-id="87bf8-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87bf8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87bf8-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87bf8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87bf8-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87bf8-131">INPUTS</span></span>

## <span data-ttu-id="87bf8-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87bf8-132">OUTPUTS</span></span>

## <span data-ttu-id="87bf8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="87bf8-133">NOTES</span></span>

## <span data-ttu-id="87bf8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87bf8-134">RELATED LINKS</span></span>

[<span data-ttu-id="87bf8-135">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="87bf8-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="87bf8-136">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="87bf8-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="87bf8-137">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="87bf8-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)


