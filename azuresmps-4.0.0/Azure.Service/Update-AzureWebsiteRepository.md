---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075843"
---
# <span data-ttu-id="54f8a-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="54f8a-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="54f8a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="54f8a-103">Обновляет удаленные репозитории в локальном репозитории Git для всех слотов.</span><span class="sxs-lookup"><span data-stu-id="54f8a-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="54f8a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54f8a-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54f8a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="54f8a-106">Командлет **Update-AzureWebsiteRepository** обновляет удаленные репозитории в локальном репозитории Git для всех слотов.</span><span class="sxs-lookup"><span data-stu-id="54f8a-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="54f8a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54f8a-107">EXAMPLES</span></span>

### <span data-ttu-id="54f8a-108">Пример 1: обновление удаленных репозиториев веб-сайта</span><span class="sxs-lookup"><span data-stu-id="54f8a-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="54f8a-109">Обновляет удаленные репозитории в локальном репозитории Git для всех слотов MyWebsite веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="54f8a-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="54f8a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54f8a-110">PARAMETERS</span></span>

### <span data-ttu-id="54f8a-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54f8a-111">-Name</span></span>
<span data-ttu-id="54f8a-112">Имя веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="54f8a-112">The name of the website.</span></span>

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

### <span data-ttu-id="54f8a-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="54f8a-113">-Profile</span></span>
<span data-ttu-id="54f8a-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="54f8a-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54f8a-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="54f8a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54f8a-116">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="54f8a-116">-PublishingUsername</span></span>
<span data-ttu-id="54f8a-117">Имя пользователя, указанное на портале Microsoft Azure для развертывания Git.</span><span class="sxs-lookup"><span data-stu-id="54f8a-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f8a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54f8a-118">-Confirm</span></span>
<span data-ttu-id="54f8a-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54f8a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54f8a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54f8a-120">-WhatIf</span></span>
<span data-ttu-id="54f8a-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54f8a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54f8a-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54f8a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54f8a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f8a-123">CommonParameters</span></span>
<span data-ttu-id="54f8a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54f8a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f8a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f8a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f8a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54f8a-126">INPUTS</span></span>

## <span data-ttu-id="54f8a-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54f8a-127">OUTPUTS</span></span>

## <span data-ttu-id="54f8a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="54f8a-128">NOTES</span></span>

## <span data-ttu-id="54f8a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54f8a-129">RELATED LINKS</span></span>

[<span data-ttu-id="54f8a-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54f8a-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="54f8a-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54f8a-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="54f8a-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54f8a-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="54f8a-133">Остановить-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54f8a-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


