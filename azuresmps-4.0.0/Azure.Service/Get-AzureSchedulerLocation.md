---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075611"
---
# <span data-ttu-id="10cf5-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="10cf5-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="10cf5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="10cf5-103">Получает доступные расположения планировщиков.</span><span class="sxs-lookup"><span data-stu-id="10cf5-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="10cf5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10cf5-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10cf5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="10cf5-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10cf5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="10cf5-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="10cf5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="10cf5-108">Командлет **Get-AzureSchedulerLocation** получает доступные расположения планировщиков.</span><span class="sxs-lookup"><span data-stu-id="10cf5-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="10cf5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10cf5-109">EXAMPLES</span></span>

### <span data-ttu-id="10cf5-110">Пример 1: получение доступных папок планировщика</span><span class="sxs-lookup"><span data-stu-id="10cf5-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="10cf5-111">Эта команда получает доступные расположения планировщиков.</span><span class="sxs-lookup"><span data-stu-id="10cf5-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="10cf5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10cf5-112">PARAMETERS</span></span>

### <span data-ttu-id="10cf5-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="10cf5-113">-Profile</span></span>
<span data-ttu-id="10cf5-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10cf5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10cf5-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10cf5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10cf5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cf5-116">CommonParameters</span></span>
<span data-ttu-id="10cf5-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10cf5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cf5-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10cf5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cf5-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10cf5-119">INPUTS</span></span>

## <span data-ttu-id="10cf5-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10cf5-120">OUTPUTS</span></span>

## <span data-ttu-id="10cf5-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="10cf5-121">NOTES</span></span>

## <span data-ttu-id="10cf5-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10cf5-122">RELATED LINKS</span></span>

[<span data-ttu-id="10cf5-123">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="10cf5-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="10cf5-124">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="10cf5-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="10cf5-125">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="10cf5-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)


