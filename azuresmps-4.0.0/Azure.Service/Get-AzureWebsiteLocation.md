---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076272"
---
# <span data-ttu-id="98b82-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="98b82-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="98b82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98b82-102">SYNOPSIS</span></span>
<span data-ttu-id="98b82-103">Получение всех доступных местоположений веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="98b82-103">Gets all available website locations.</span></span>

## <span data-ttu-id="98b82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98b82-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="98b82-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98b82-105">DESCRIPTION</span></span>
<span data-ttu-id="98b82-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="98b82-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="98b82-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="98b82-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="98b82-108">Возвращает все доступные расположения веб-сайтов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="98b82-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="98b82-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98b82-109">EXAMPLES</span></span>

### <span data-ttu-id="98b82-110">Пример 1: получение всех доступных местоположений</span><span class="sxs-lookup"><span data-stu-id="98b82-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="98b82-111">В этом примере получается список всех доступных местоположений веб-сайтов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="98b82-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="98b82-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98b82-112">PARAMETERS</span></span>

### <span data-ttu-id="98b82-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="98b82-113">-Profile</span></span>
<span data-ttu-id="98b82-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="98b82-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98b82-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="98b82-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98b82-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b82-116">CommonParameters</span></span>
<span data-ttu-id="98b82-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98b82-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b82-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b82-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b82-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98b82-119">INPUTS</span></span>

## <span data-ttu-id="98b82-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98b82-120">OUTPUTS</span></span>

## <span data-ttu-id="98b82-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="98b82-121">NOTES</span></span>

## <span data-ttu-id="98b82-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98b82-122">RELATED LINKS</span></span>

[<span data-ttu-id="98b82-123">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="98b82-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)


