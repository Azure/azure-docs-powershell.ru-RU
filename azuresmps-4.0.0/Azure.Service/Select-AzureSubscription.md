---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075445"
---
# <span data-ttu-id="39683-101">Select-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="39683-101">Select-AzureSubscription</span></span>

## <span data-ttu-id="39683-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39683-102">SYNOPSIS</span></span>
<span data-ttu-id="39683-103">Изменение текущих и подписок Azure по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39683-103">Changes the current and default Azure subscriptions.</span></span>

## <span data-ttu-id="39683-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39683-104">SYNTAX</span></span>

### <span data-ttu-id="39683-105">SelectSubscriptionByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39683-105">SelectSubscriptionByNameParameterSet (Default)</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="39683-106">SelectDefaultSubscriptionByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="39683-106">SelectDefaultSubscriptionByNameParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="39683-107">SelectSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39683-107">SelectSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="39683-108">SelectDefaultSubscriptionByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39683-108">SelectDefaultSubscriptionByIdParameterSet</span></span>
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="39683-109">NoCurrentSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="39683-109">NoCurrentSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="39683-110">NoDefaultSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="39683-110">NoDefaultSubscriptionParameterSet</span></span>
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="39683-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39683-111">DESCRIPTION</span></span>
<span data-ttu-id="39683-112">Командлет **SELECT-AzureSubscription** задает и очищает текущие и используемые по умолчанию подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="39683-112">The **Select-AzureSubscription** cmdlet sets and clears the current and default Azure subscriptions.</span></span>

<span data-ttu-id="39683-113">"Текущая подписка" — это подписка, используемая по умолчанию в текущем сеансе Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="39683-113">The "current subscription" is the subscription that is used by default in the current Windows PowerShell session.</span></span>
<span data-ttu-id="39683-114">Подписку по умолчанию используется по умолчанию во всех сеансах Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="39683-114">The "default subscription" is used by default in all Windows PowerShell sessions.</span></span>
<span data-ttu-id="39683-115">Метка "текущая подписка" позволяет указать другую подписку, которая будет использоваться по умолчанию для текущего сеанса, не меняя "подписку по умолчанию" для всех остальных сеансов.</span><span class="sxs-lookup"><span data-stu-id="39683-115">The "current subscription" label lets you specify a different subscription to be used by default for the current session without changing the "default subscription" for all other sessions.</span></span>

<span data-ttu-id="39683-116">Назначение подписки "по умолчанию" сохраняется в файле данных подписки.</span><span class="sxs-lookup"><span data-stu-id="39683-116">The "default" subscription designation is saved in your subscription data file.</span></span>
<span data-ttu-id="39683-117">Текущее обозначение сеанса не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="39683-117">The session-specific "current" designation is not saved.</span></span>

<span data-ttu-id="39683-118">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="39683-118">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="39683-119">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="39683-119">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="39683-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39683-120">EXAMPLES</span></span>

### <span data-ttu-id="39683-121">Пример 1: Настройка текущей подписки</span><span class="sxs-lookup"><span data-stu-id="39683-121">Example 1: Set the current subscription</span></span>
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

<span data-ttu-id="39683-122">Эта команда делает "ContosoEngineering" текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="39683-122">This command makes "ContosoEngineering" the current subscription.</span></span>

### <span data-ttu-id="39683-123">Пример 2: Настройка подписки по умолчанию</span><span class="sxs-lookup"><span data-stu-id="39683-123">Example 2: Set the default subscription</span></span>
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

<span data-ttu-id="39683-124">Эта команда изменяет подписку по умолчанию на "ContosoFinance".</span><span class="sxs-lookup"><span data-stu-id="39683-124">This command changes the default subscription to "ContosoFinance."</span></span> <span data-ttu-id="39683-125">Параметр сохраняется в файле данных подписки Subscriptions.xml, а не в файле данных подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39683-125">It saves the setting in the Subscriptions.xml subscription data file, instead of the default subscription data file.</span></span>

## <span data-ttu-id="39683-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39683-126">PARAMETERS</span></span>

### <span data-ttu-id="39683-127">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="39683-127">-Account</span></span>
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

### <span data-ttu-id="39683-128">-Current</span><span class="sxs-lookup"><span data-stu-id="39683-128">-Current</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39683-129">-Default</span><span class="sxs-lookup"><span data-stu-id="39683-129">-Default</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39683-130">-Нетекущие</span><span class="sxs-lookup"><span data-stu-id="39683-130">-NoCurrent</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39683-131">-По умолчанию</span><span class="sxs-lookup"><span data-stu-id="39683-131">-NoDefault</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39683-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39683-132">-PassThru</span></span>
<span data-ttu-id="39683-133">Возвращает $True, если команда выполнена успешно, и $False в случае ее сбоя.</span><span class="sxs-lookup"><span data-stu-id="39683-133">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="39683-134">По умолчанию этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="39683-134">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="39683-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="39683-135">-Profile</span></span>
<span data-ttu-id="39683-136">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="39683-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="39683-137">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39683-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39683-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39683-138">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39683-139">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="39683-139">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39683-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39683-140">CommonParameters</span></span>
<span data-ttu-id="39683-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39683-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39683-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39683-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39683-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39683-143">INPUTS</span></span>

### <span data-ttu-id="39683-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="39683-144">None</span></span>
<span data-ttu-id="39683-145">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="39683-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="39683-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39683-146">OUTPUTS</span></span>

### <span data-ttu-id="39683-147">None и System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39683-147">None or System.Boolean</span></span>
<span data-ttu-id="39683-148">Если вы используете параметр *PassThru* , этот командлет возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="39683-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="39683-149">По умолчанию никакие выходные данные не выводятся.</span><span class="sxs-lookup"><span data-stu-id="39683-149">By default, it does not generate any output.</span></span>

## <span data-ttu-id="39683-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="39683-150">NOTES</span></span>

## <span data-ttu-id="39683-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39683-151">RELATED LINKS</span></span>

[<span data-ttu-id="39683-152">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="39683-152">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="39683-153">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="39683-153">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="39683-154">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="39683-154">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


