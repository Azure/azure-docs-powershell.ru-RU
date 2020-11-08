---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076512"
---
# <span data-ttu-id="66893-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="66893-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="66893-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66893-102">SYNOPSIS</span></span>
<span data-ttu-id="66893-103">Возвращает планы для веб-хостинга Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="66893-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="66893-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66893-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="66893-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66893-105">DESCRIPTION</span></span>
<span data-ttu-id="66893-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="66893-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="66893-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="66893-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="66893-108">Командлет **Get-AzureWebHostingPlan** получает планы веб-хостинга Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="66893-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="66893-109">По умолчанию **Get-AzureWebHostingPlan** получает все планы размещения Azure в текущей подписке и возвращает объект, который предоставляет базовые сведения о планах.</span><span class="sxs-lookup"><span data-stu-id="66893-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="66893-110">При использовании параметров *Space* и *Name* функция **Get-AzureWebHostingPlan** Возвращает определенный объект плана размещения.</span><span class="sxs-lookup"><span data-stu-id="66893-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="66893-111">Чтобы найти текущую подписку, используйте *текущий* параметр командлета **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="66893-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="66893-112">Чтобы изменить текущую подписку, используйте командлет **SELECT-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="66893-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="66893-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66893-113">EXAMPLES</span></span>

### <span data-ttu-id="66893-114">Пример 1: получение всех планов размещения веб-сайтов в подписке</span><span class="sxs-lookup"><span data-stu-id="66893-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="66893-115">Эта команда получает все планы размещения веб-сайтов Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="66893-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="66893-116">Пример 2: получение определенного плана размещения на веб-сайте в подписке</span><span class="sxs-lookup"><span data-stu-id="66893-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="66893-117">Эта команда получает план размещения веб-сайта с именем Default0 в пространстве имен westeuropewebspace в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="66893-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="66893-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66893-118">PARAMETERS</span></span>

### <span data-ttu-id="66893-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66893-119">-Name</span></span>
<span data-ttu-id="66893-120">Указывает имя плана в подписке.</span><span class="sxs-lookup"><span data-stu-id="66893-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="66893-121">По умолчанию этот командлет получает все планы в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="66893-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="66893-122">Этот параметр не поддерживает подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="66893-122">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="66893-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="66893-123">-Profile</span></span>
<span data-ttu-id="66893-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="66893-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66893-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66893-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66893-126">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="66893-126">-WebSpaceName</span></span>
<span data-ttu-id="66893-127">Указывает имя веб-пространства в подписке.</span><span class="sxs-lookup"><span data-stu-id="66893-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="66893-128">По умолчанию этот командлет получает все сайты в указанном веб-пространстве.</span><span class="sxs-lookup"><span data-stu-id="66893-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="66893-129">Этот параметр не поддерживает подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="66893-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66893-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66893-130">CommonParameters</span></span>
<span data-ttu-id="66893-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66893-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66893-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66893-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66893-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66893-133">INPUTS</span></span>

###  
<span data-ttu-id="66893-134">Вы можете передать входные данные этому командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="66893-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="66893-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66893-135">OUTPUTS</span></span>

### <span data-ttu-id="66893-136">Microsoft. WindowsAzure. Commands. Utilities. website. Services. Entities. WebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="66893-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="66893-137">По умолчанию **Get-AzureWebHostingPlan** возвращает массив объектов **WebHostingPlan** .</span><span class="sxs-lookup"><span data-stu-id="66893-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="66893-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="66893-138">NOTES</span></span>

## <span data-ttu-id="66893-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66893-139">RELATED LINKS</span></span>

