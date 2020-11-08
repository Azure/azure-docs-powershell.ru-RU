---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075939"
---
# <span data-ttu-id="8b32c-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="8b32c-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="8b32c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b32c-102">SYNOPSIS</span></span>
<span data-ttu-id="8b32c-103">Замена слота производства для веб-сайта другим слотом.</span><span class="sxs-lookup"><span data-stu-id="8b32c-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="8b32c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b32c-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b32c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b32c-105">DESCRIPTION</span></span>
<span data-ttu-id="8b32c-106">Командлет **switch-AzureWebsiteSlot** заменяет рабочее гнездо для веб-сайта другим слотом.</span><span class="sxs-lookup"><span data-stu-id="8b32c-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="8b32c-107">Это работает на веб-сайтах с двумя разъемами.</span><span class="sxs-lookup"><span data-stu-id="8b32c-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="8b32c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b32c-108">EXAMPLES</span></span>

### <span data-ttu-id="8b32c-109">Пример 1: переключение слотов веб-сайта</span><span class="sxs-lookup"><span data-stu-id="8b32c-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="8b32c-110">Переключите слот резервного MyWebsite веб-сайта Azure в производственную ячейку.</span><span class="sxs-lookup"><span data-stu-id="8b32c-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="8b32c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b32c-111">PARAMETERS</span></span>

### <span data-ttu-id="8b32c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="8b32c-112">-Force</span></span>
<span data-ttu-id="8b32c-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8b32c-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b32c-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b32c-114">-Name</span></span>
<span data-ttu-id="8b32c-115">Имя веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="8b32c-115">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b32c-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="8b32c-116">-Profile</span></span>
<span data-ttu-id="8b32c-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8b32c-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8b32c-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b32c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8b32c-119">-Slot1</span><span class="sxs-lookup"><span data-stu-id="8b32c-119">-Slot1</span></span>
<span data-ttu-id="8b32c-120">Задает первый слот.</span><span class="sxs-lookup"><span data-stu-id="8b32c-120">Specifies the first slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b32c-121">-Slot2</span><span class="sxs-lookup"><span data-stu-id="8b32c-121">-Slot2</span></span>
<span data-ttu-id="8b32c-122">Определяет вторую ячейку.</span><span class="sxs-lookup"><span data-stu-id="8b32c-122">Specifies the second slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b32c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b32c-123">-Confirm</span></span>
<span data-ttu-id="8b32c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b32c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b32c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b32c-125">-WhatIf</span></span>
<span data-ttu-id="8b32c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b32c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b32c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b32c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b32c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b32c-128">CommonParameters</span></span>
<span data-ttu-id="8b32c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b32c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b32c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b32c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b32c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b32c-131">INPUTS</span></span>

## <span data-ttu-id="8b32c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b32c-132">OUTPUTS</span></span>

## <span data-ttu-id="8b32c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b32c-133">NOTES</span></span>

## <span data-ttu-id="8b32c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b32c-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b32c-135">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8b32c-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="8b32c-136">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8b32c-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="8b32c-137">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8b32c-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="8b32c-138">Остановить-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8b32c-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


