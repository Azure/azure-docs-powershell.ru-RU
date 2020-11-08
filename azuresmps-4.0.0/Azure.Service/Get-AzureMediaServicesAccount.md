---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076335"
---
# <span data-ttu-id="92031-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="92031-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="92031-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92031-102">SYNOPSIS</span></span>
<span data-ttu-id="92031-103">Получает доступные учетные записи служб мультимедиа Azure.</span><span class="sxs-lookup"><span data-stu-id="92031-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="92031-104">**Примечание.** Эта версия устарела, ознакомьтесь с [более новой версией](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="92031-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="92031-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92031-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="92031-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92031-106">DESCRIPTION</span></span>
<span data-ttu-id="92031-107">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="92031-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="92031-108">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="92031-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="92031-109">Чтобы вывести все учетные записи, используйте `Get-AzureMediaServicesAccount` командлет.</span><span class="sxs-lookup"><span data-stu-id="92031-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="92031-110">Чтобы получить более подробные сведения об определенной учетной записи, используйте `Get-AzureMediaServicesAccount -Name YourAccountName` командлет.</span><span class="sxs-lookup"><span data-stu-id="92031-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="92031-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92031-111">EXAMPLES</span></span>

### <span data-ttu-id="92031-112">Пример 1: список всех учетных записей служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="92031-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="92031-113">Эта команда перечисляет все доступные учетные записи служб мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="92031-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="92031-114">Пример 2: получение подробных сведений об учетной записи служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="92031-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="92031-115">Эта команда отображает свойства учетной записи служб мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="92031-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="92031-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92031-116">PARAMETERS</span></span>

### <span data-ttu-id="92031-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92031-117">-Name</span></span>
<span data-ttu-id="92031-118">Имя учетной записи службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="92031-118">The Media Services account name.</span></span>

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

### <span data-ttu-id="92031-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="92031-119">-Profile</span></span>
<span data-ttu-id="92031-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92031-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92031-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92031-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92031-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92031-122">CommonParameters</span></span>
<span data-ttu-id="92031-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92031-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92031-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92031-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92031-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92031-125">INPUTS</span></span>

## <span data-ttu-id="92031-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92031-126">OUTPUTS</span></span>

## <span data-ttu-id="92031-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="92031-127">NOTES</span></span>

## <span data-ttu-id="92031-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92031-128">RELATED LINKS</span></span>

[<span data-ttu-id="92031-129">Использование Azure PowerShell для служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="92031-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


