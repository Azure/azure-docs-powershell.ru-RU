---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076001"
---
# <span data-ttu-id="19188-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="19188-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="19188-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19188-102">SYNOPSIS</span></span>
<span data-ttu-id="19188-103">Обновляет ключи учетной записи служб мультимедиа Azure.</span><span class="sxs-lookup"><span data-stu-id="19188-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="19188-104">**Примечание.** Эта версия устарела, ознакомьтесь с [более новой версией](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="19188-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="19188-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19188-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19188-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19188-106">DESCRIPTION</span></span>
<span data-ttu-id="19188-107">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="19188-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="19188-108">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="19188-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="19188-109">Командлет **New-AzureMediaServicesKey** обновляет первичный или вторичный ключ для указанной учетной записи служб мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="19188-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="19188-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19188-110">EXAMPLES</span></span>

### <span data-ttu-id="19188-111">Пример 1: обновление ключа учетной записи служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="19188-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="19188-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19188-112">PARAMETERS</span></span>

### <span data-ttu-id="19188-113">-Force</span><span class="sxs-lookup"><span data-stu-id="19188-113">-Force</span></span>
<span data-ttu-id="19188-114">Указывает на то, что создание ключа не подтверждено.</span><span class="sxs-lookup"><span data-stu-id="19188-114">Indicates that the key generation is not confirmed.</span></span>

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

### <span data-ttu-id="19188-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="19188-115">-KeyType</span></span>
<span data-ttu-id="19188-116">Указывает тип ключа служб мультимедиа; Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="19188-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="19188-117">Главная</span><span class="sxs-lookup"><span data-stu-id="19188-117">Primary</span></span>
- <span data-ttu-id="19188-118">Запас</span><span class="sxs-lookup"><span data-stu-id="19188-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19188-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19188-119">-Name</span></span>
<span data-ttu-id="19188-120">Указывает имя учетной записи служб мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="19188-120">Specifies the name of the Media Services account.</span></span>

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

### <span data-ttu-id="19188-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="19188-121">-Profile</span></span>
<span data-ttu-id="19188-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="19188-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19188-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19188-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19188-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19188-124">-Confirm</span></span>
<span data-ttu-id="19188-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19188-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19188-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19188-126">-WhatIf</span></span>
<span data-ttu-id="19188-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19188-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19188-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19188-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19188-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19188-129">CommonParameters</span></span>
<span data-ttu-id="19188-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19188-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19188-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19188-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19188-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19188-132">INPUTS</span></span>

## <span data-ttu-id="19188-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19188-133">OUTPUTS</span></span>

## <span data-ttu-id="19188-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="19188-134">NOTES</span></span>

## <span data-ttu-id="19188-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19188-135">RELATED LINKS</span></span>

[<span data-ttu-id="19188-136">Использование Azure PowerShell для служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="19188-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


