---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075785"
---
# <span data-ttu-id="4fa20-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4fa20-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="4fa20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fa20-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa20-103">Открытие браузера на указанном веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="4fa20-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="4fa20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fa20-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4fa20-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fa20-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa20-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4fa20-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4fa20-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4fa20-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4fa20-108">Командлет **Show-AzureWebsite** откроет браузер на указанном веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="4fa20-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="4fa20-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fa20-109">EXAMPLES</span></span>

## <span data-ttu-id="4fa20-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fa20-110">PARAMETERS</span></span>

### <span data-ttu-id="4fa20-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4fa20-111">-Name</span></span>
<span data-ttu-id="4fa20-112">Указывает имя сайта, который нужно открыть в браузере.</span><span class="sxs-lookup"><span data-stu-id="4fa20-112">Specifies the name of the site to open in the browser.</span></span>

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

### <span data-ttu-id="4fa20-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="4fa20-113">-Profile</span></span>
<span data-ttu-id="4fa20-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4fa20-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4fa20-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4fa20-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4fa20-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="4fa20-116">-Slot</span></span>
<span data-ttu-id="4fa20-117">Указывает имя гнезда для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="4fa20-117">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="4fa20-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa20-118">CommonParameters</span></span>
<span data-ttu-id="4fa20-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fa20-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa20-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fa20-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa20-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fa20-121">INPUTS</span></span>

## <span data-ttu-id="4fa20-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fa20-122">OUTPUTS</span></span>

## <span data-ttu-id="4fa20-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fa20-123">NOTES</span></span>

## <span data-ttu-id="4fa20-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fa20-124">RELATED LINKS</span></span>

[<span data-ttu-id="4fa20-125">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="4fa20-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="4fa20-126">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4fa20-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="4fa20-127">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4fa20-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="4fa20-128">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4fa20-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="4fa20-129">Restarting-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4fa20-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="4fa20-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4fa20-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


