---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076201"
---
# <span data-ttu-id="e58a3-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="e58a3-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="e58a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e58a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e58a3-103">Покупает новый экземпляр надстройки.</span><span class="sxs-lookup"><span data-stu-id="e58a3-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="e58a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e58a3-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e58a3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e58a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e58a3-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e58a3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e58a3-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e58a3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e58a3-108">Покупает новый экземпляр надстройки из магазина Azure.</span><span class="sxs-lookup"><span data-stu-id="e58a3-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="e58a3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e58a3-109">EXAMPLES</span></span>

### <span data-ttu-id="e58a3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e58a3-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="e58a3-111">В этом примере демонстрируется добавление надстройки с именем MyAddOn и PlanId в области "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="e58a3-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="e58a3-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e58a3-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="e58a3-113">В этом примере для приобретения надстройки используется код рекламной акции.</span><span class="sxs-lookup"><span data-stu-id="e58a3-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="e58a3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e58a3-114">PARAMETERS</span></span>

### <span data-ttu-id="e58a3-115">-Надстройка</span><span class="sxs-lookup"><span data-stu-id="e58a3-115">-AddOn</span></span>
<span data-ttu-id="e58a3-116">Указывает идентификатор надстройки.</span><span class="sxs-lookup"><span data-stu-id="e58a3-116">Specifies the add-on ID.</span></span>

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

### <span data-ttu-id="e58a3-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e58a3-117">-Location</span></span>
<span data-ttu-id="e58a3-118">Задает расположение экземпляра надстройки.</span><span class="sxs-lookup"><span data-stu-id="e58a3-118">Specifies the add-on instance location.</span></span>

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

### <span data-ttu-id="e58a3-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e58a3-119">-Name</span></span>
<span data-ttu-id="e58a3-120">Указывает имя экземпляра надстройки.</span><span class="sxs-lookup"><span data-stu-id="e58a3-120">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="e58a3-121">-Планирование</span><span class="sxs-lookup"><span data-stu-id="e58a3-121">-Plan</span></span>
<span data-ttu-id="e58a3-122">Указывает идентификатор плана.</span><span class="sxs-lookup"><span data-stu-id="e58a3-122">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="e58a3-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="e58a3-123">-Profile</span></span>
<span data-ttu-id="e58a3-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e58a3-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e58a3-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e58a3-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e58a3-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="e58a3-126">-PromotionCode</span></span>
<span data-ttu-id="e58a3-127">Указывает код продвижения, применяемый к покупке.</span><span class="sxs-lookup"><span data-stu-id="e58a3-127">Specifies a promotion code to apply to the purchase.</span></span>

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

### <span data-ttu-id="e58a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e58a3-128">CommonParameters</span></span>
<span data-ttu-id="e58a3-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e58a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e58a3-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e58a3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e58a3-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e58a3-131">INPUTS</span></span>

## <span data-ttu-id="e58a3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e58a3-132">OUTPUTS</span></span>

## <span data-ttu-id="e58a3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e58a3-133">NOTES</span></span>

## <span data-ttu-id="e58a3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e58a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="e58a3-135">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="e58a3-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="e58a3-136">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="e58a3-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="e58a3-137">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="e58a3-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


