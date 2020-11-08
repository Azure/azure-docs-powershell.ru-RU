---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076415"
---
# <span data-ttu-id="369a1-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="369a1-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="369a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="369a1-102">SYNOPSIS</span></span>
<span data-ttu-id="369a1-103">Обновляет существующий экземпляр надстройки.</span><span class="sxs-lookup"><span data-stu-id="369a1-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="369a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="369a1-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="369a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="369a1-105">DESCRIPTION</span></span>
<span data-ttu-id="369a1-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="369a1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="369a1-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="369a1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="369a1-108">Этот командлет обновляет существующий экземпляр надстройки из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="369a1-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="369a1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="369a1-109">EXAMPLES</span></span>

### <span data-ttu-id="369a1-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="369a1-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="369a1-111">В этом примере обновляется надстройка с новым ИДЕНТИФИКАТОРом плана.</span><span class="sxs-lookup"><span data-stu-id="369a1-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="369a1-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="369a1-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="369a1-113">В этом примере обновляется надстройка с новым ИДЕНТИФИКАТОРом плана и кодом рекламной акции.</span><span class="sxs-lookup"><span data-stu-id="369a1-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="369a1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="369a1-114">PARAMETERS</span></span>

### <span data-ttu-id="369a1-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="369a1-115">-Name</span></span>
<span data-ttu-id="369a1-116">Указывает имя экземпляра надстройки.</span><span class="sxs-lookup"><span data-stu-id="369a1-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="369a1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="369a1-117">-PassThru</span></span>
<span data-ttu-id="369a1-118">Если указан, командлет возвращает значение true, если команда выполнена успешно, и false в случае его сбоя.</span><span class="sxs-lookup"><span data-stu-id="369a1-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="369a1-119">-Планирование</span><span class="sxs-lookup"><span data-stu-id="369a1-119">-Plan</span></span>
<span data-ttu-id="369a1-120">Указывает идентификатор плана.</span><span class="sxs-lookup"><span data-stu-id="369a1-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="369a1-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="369a1-121">-Profile</span></span>
<span data-ttu-id="369a1-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="369a1-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="369a1-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="369a1-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="369a1-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="369a1-124">-PromotionCode</span></span>
<span data-ttu-id="369a1-125">Определяет рекламный код.</span><span class="sxs-lookup"><span data-stu-id="369a1-125">Specifies the promotional code.</span></span>

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

### <span data-ttu-id="369a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369a1-126">CommonParameters</span></span>
<span data-ttu-id="369a1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="369a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369a1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="369a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369a1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="369a1-129">INPUTS</span></span>

## <span data-ttu-id="369a1-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="369a1-130">OUTPUTS</span></span>

## <span data-ttu-id="369a1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="369a1-131">NOTES</span></span>

## <span data-ttu-id="369a1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="369a1-132">RELATED LINKS</span></span>

[<span data-ttu-id="369a1-133">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="369a1-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="369a1-134">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="369a1-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="369a1-135">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="369a1-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)


