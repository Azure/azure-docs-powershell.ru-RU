---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075483"
---
# <span data-ttu-id="cbdc8-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="cbdc8-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="cbdc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbdc8-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdc8-103">Удаление указанного веб-сайта из Azure.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="cbdc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbdc8-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbdc8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbdc8-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdc8-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cbdc8-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cbdc8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="cbdc8-108">Командлет **Remove-AzureWebsite** удаляет указанный веб-сайт из Azure либо с запросом подтверждения, либо без него.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="cbdc8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbdc8-109">EXAMPLES</span></span>

### <span data-ttu-id="cbdc8-110">Пример 1: Удаление текущего веб-сайта</span><span class="sxs-lookup"><span data-stu-id="cbdc8-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="cbdc8-111">В этом примере удаляется веб-сайт в Azure, связанный с текущим каталогом.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="cbdc8-112">Пример 2: удаление веб-сайта без подтверждения</span><span class="sxs-lookup"><span data-stu-id="cbdc8-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="cbdc8-113">В этом примере удаляется веб-сайт с именем личного сайта без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="cbdc8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbdc8-114">PARAMETERS</span></span>

### <span data-ttu-id="cbdc8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cbdc8-115">-Force</span></span>
<span data-ttu-id="cbdc8-116">Если указан, удаляет указанный веб-сайт без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cbdc8-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cbdc8-117">-Name</span></span>
<span data-ttu-id="cbdc8-118">Указывает имя веб-сайта, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-118">Specifies the name of the website to delete.</span></span>

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

### <span data-ttu-id="cbdc8-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="cbdc8-119">-Profile</span></span>
<span data-ttu-id="cbdc8-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cbdc8-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cbdc8-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="cbdc8-122">-Slot</span></span>
<span data-ttu-id="cbdc8-123">Указывает имя гнезда для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-123">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="cbdc8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbdc8-124">-Confirm</span></span>
<span data-ttu-id="cbdc8-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbdc8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbdc8-126">-WhatIf</span></span>
<span data-ttu-id="cbdc8-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbdc8-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbdc8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdc8-129">CommonParameters</span></span>
<span data-ttu-id="cbdc8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbdc8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdc8-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbdc8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdc8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbdc8-132">INPUTS</span></span>

## <span data-ttu-id="cbdc8-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbdc8-133">OUTPUTS</span></span>

## <span data-ttu-id="cbdc8-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbdc8-134">NOTES</span></span>

## <span data-ttu-id="cbdc8-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbdc8-135">RELATED LINKS</span></span>

[<span data-ttu-id="cbdc8-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="cbdc8-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


