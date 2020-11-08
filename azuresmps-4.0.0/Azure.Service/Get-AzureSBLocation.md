---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076312"
---
# <span data-ttu-id="02964-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="02964-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="02964-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02964-102">SYNOPSIS</span></span>
<span data-ttu-id="02964-103">Возвращает расположение служебной шины.</span><span class="sxs-lookup"><span data-stu-id="02964-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="02964-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02964-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="02964-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02964-105">DESCRIPTION</span></span>
<span data-ttu-id="02964-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02964-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="02964-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="02964-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="02964-108">Командлет **Get-AzureSBLocation** возвращает расположение, из которого доступна служебная шина.</span><span class="sxs-lookup"><span data-stu-id="02964-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="02964-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02964-109">EXAMPLES</span></span>

### <span data-ttu-id="02964-110">Пример 1: получение места для служебной шины</span><span class="sxs-lookup"><span data-stu-id="02964-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="02964-111">В этом примере показано, как получается место служебной шины.</span><span class="sxs-lookup"><span data-stu-id="02964-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="02964-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02964-112">PARAMETERS</span></span>

### <span data-ttu-id="02964-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="02964-113">-Profile</span></span>
<span data-ttu-id="02964-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="02964-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02964-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="02964-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02964-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02964-116">CommonParameters</span></span>
<span data-ttu-id="02964-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02964-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02964-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02964-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02964-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02964-119">INPUTS</span></span>

## <span data-ttu-id="02964-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02964-120">OUTPUTS</span></span>

## <span data-ttu-id="02964-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="02964-121">NOTES</span></span>

## <span data-ttu-id="02964-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02964-122">RELATED LINKS</span></span>

[<span data-ttu-id="02964-123">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="02964-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)


