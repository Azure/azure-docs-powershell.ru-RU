---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076020"
---
# <span data-ttu-id="045e2-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="045e2-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="045e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="045e2-102">SYNOPSIS</span></span>
<span data-ttu-id="045e2-103">Отменяет публикацию удаленного приложения RemoteApp для Azure.</span><span class="sxs-lookup"><span data-stu-id="045e2-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="045e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="045e2-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="045e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="045e2-105">DESCRIPTION</span></span>
<span data-ttu-id="045e2-106">Командлет **UNPUBLISH-AzureRemoteAppProgram** отменяет публикацию программы RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="045e2-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="045e2-107">После отмены публикации программы она станет недоступна для пользователей коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="045e2-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="045e2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="045e2-108">EXAMPLES</span></span>

## <span data-ttu-id="045e2-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="045e2-109">PARAMETERS</span></span>

### <span data-ttu-id="045e2-110">-Alias</span><span class="sxs-lookup"><span data-stu-id="045e2-110">-Alias</span></span>
<span data-ttu-id="045e2-111">Задает массив псевдонимов программ, которые нужно отменять публикацию.</span><span class="sxs-lookup"><span data-stu-id="045e2-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="045e2-112">С помощью **Get-AzureRemoteAppProgram** можно получить псевдоним программы для отмены публикации.</span><span class="sxs-lookup"><span data-stu-id="045e2-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="045e2-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="045e2-113">-CollectionName</span></span>
<span data-ttu-id="045e2-114">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="045e2-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="045e2-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="045e2-115">-Profile</span></span>
<span data-ttu-id="045e2-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="045e2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="045e2-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="045e2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="045e2-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="045e2-118">-Confirm</span></span>
<span data-ttu-id="045e2-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="045e2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="045e2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="045e2-120">-WhatIf</span></span>
<span data-ttu-id="045e2-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="045e2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="045e2-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="045e2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="045e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045e2-123">CommonParameters</span></span>
<span data-ttu-id="045e2-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="045e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045e2-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="045e2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045e2-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="045e2-126">INPUTS</span></span>

## <span data-ttu-id="045e2-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="045e2-127">OUTPUTS</span></span>

## <span data-ttu-id="045e2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="045e2-128">NOTES</span></span>

## <span data-ttu-id="045e2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="045e2-129">RELATED LINKS</span></span>

[<span data-ttu-id="045e2-130">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="045e2-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="045e2-131">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="045e2-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)


