---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075537"
---
# <span data-ttu-id="367d8-101">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="367d8-101">Get-AzureSubscription</span></span>

## <span data-ttu-id="367d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="367d8-102">SYNOPSIS</span></span>
<span data-ttu-id="367d8-103">Получение подписок на Azure в учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="367d8-103">Gets  Azure subscriptions in Azure account.</span></span>

## <span data-ttu-id="367d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="367d8-104">SYNTAX</span></span>

### <span data-ttu-id="367d8-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="367d8-105">ByName (Default)</span></span>
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="367d8-106">ById</span><span class="sxs-lookup"><span data-stu-id="367d8-106">ById</span></span>
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="367d8-107">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="367d8-107">Default</span></span>
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="367d8-108">Текущей</span><span class="sxs-lookup"><span data-stu-id="367d8-108">Current</span></span>
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="367d8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="367d8-109">DESCRIPTION</span></span>
<span data-ttu-id="367d8-110">Командлет **Get-AzureSubscription** получает подписки в учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="367d8-110">The **Get-AzureSubscription** cmdlet gets the subscriptions in your Azure account.</span></span>
<span data-ttu-id="367d8-111">Вы можете использовать этот командлет для получения сведений о подписке и для канала подписки на другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="367d8-111">You can use this cmdlet to get information about the subscription and to pipe the subscription to other cmdlets.</span></span>

<span data-ttu-id="367d8-112">Для **Get-AzureSubscription** требуется доступ к учетным записям Azure.</span><span class="sxs-lookup"><span data-stu-id="367d8-112">**Get-AzureSubscription** requires access to your Azure accounts.</span></span>
<span data-ttu-id="367d8-113">Перед запуском **Get-AzureSubscription** необходимо запустить командлет **Add-AzureAccount** или командлеты, которые загружают и устанавливают файл параметров публикации ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span><span class="sxs-lookup"><span data-stu-id="367d8-113">Before you run **Get-AzureSubscription** , you must run the **Add-AzureAccount** cmdlet or the cmdlets that download and install a publish settings file ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.</span></span>

<span data-ttu-id="367d8-114">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="367d8-114">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="367d8-115">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="367d8-115">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="367d8-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="367d8-116">EXAMPLES</span></span>

### <span data-ttu-id="367d8-117">Пример 1: получение всех подписок</span><span class="sxs-lookup"><span data-stu-id="367d8-117">Example 1: Get all subscriptions</span></span>
```
C:\PS>Get-AzureSubscription
```

<span data-ttu-id="367d8-118">Эта команда получает все подписки в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="367d8-118">This command gets all subscriptions in the account.</span></span>

### <span data-ttu-id="367d8-119">Пример 2: получение подписки по имени</span><span class="sxs-lookup"><span data-stu-id="367d8-119">Example 2: Get a subscription by name</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

<span data-ttu-id="367d8-120">Эта команда получает только подписку на "MyProdSubsciption".</span><span class="sxs-lookup"><span data-stu-id="367d8-120">This command gets only the "MyProdSubsciption" subscription.</span></span>

### <span data-ttu-id="367d8-121">Пример 3: получение подписки по умолчанию</span><span class="sxs-lookup"><span data-stu-id="367d8-121">Example 3: Get the default subscription</span></span>
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

<span data-ttu-id="367d8-122">Эта команда возвращает только имя подписки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="367d8-122">This command gets only the name of the default subscription.</span></span>
<span data-ttu-id="367d8-123">Команда сначала получает подписку, а затем использует метод Dot для получения свойства **SubscriptionName** подписки.</span><span class="sxs-lookup"><span data-stu-id="367d8-123">The command first gets the subscription and then uses the dot method to get the **SubscriptionName** property of the subscription.</span></span>

### <span data-ttu-id="367d8-124">Пример 4: получение свойств выбранных подписок</span><span class="sxs-lookup"><span data-stu-id="367d8-124">Example 4: Get selected subscription properties</span></span>
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

<span data-ttu-id="367d8-125">Эта команда возвращает список с именем и сертификатом текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="367d8-125">This command returns a list with the name and certificate of the current subscription.</span></span>
<span data-ttu-id="367d8-126">Для получения текущей подписки используется команда **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="367d8-126">It uses a **Get-AzureSubscription** command to get the current subscription.</span></span>
<span data-ttu-id="367d8-127">Затем он поддает подписку на команду **Format-List** , которая отображает выбранные свойства в списке.</span><span class="sxs-lookup"><span data-stu-id="367d8-127">Then it pipes the subscription to a **Format-List** command that displays the selected properties in a list.</span></span>

### <span data-ttu-id="367d8-128">Пример 5: использование альтернативного файла данных подписки</span><span class="sxs-lookup"><span data-stu-id="367d8-128">Example 5: Use an alternate subscription data file</span></span>
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

<span data-ttu-id="367d8-129">Эта команда получает подписку из файла данных подписки C:\Temp\MySubscriptions.xml.</span><span class="sxs-lookup"><span data-stu-id="367d8-129">This command gets subscriptions from  the C:\Temp\MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="367d8-130">Если вы указали альтернативный файл данных подписки при выполнении командлетов **Add-AzureAccount** или **Import-PublishSettingsFile** , используйте параметр **SubscriptionDataFile** .</span><span class="sxs-lookup"><span data-stu-id="367d8-130">Use the **SubscriptionDataFile** parameter if you specified an alternate subscription data file when you ran the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="367d8-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="367d8-131">PARAMETERS</span></span>

### <span data-ttu-id="367d8-132">-Current</span><span class="sxs-lookup"><span data-stu-id="367d8-132">-Current</span></span>
<span data-ttu-id="367d8-133">Возвращает только текущую подписку, то есть подписку, обозначенную как "Текущая".</span><span class="sxs-lookup"><span data-stu-id="367d8-133">Gets only the current subscription, that is, the subscription designated as "current."</span></span> <span data-ttu-id="367d8-134">По умолчанию **Get-AzureSubscription** получает все подписки в учетных записях Azure.</span><span class="sxs-lookup"><span data-stu-id="367d8-134">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="367d8-135">Чтобы назначить подписку "Current", используйте **текущий** параметр командлета **SELECT-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="367d8-135">To designate a subscription as "current," use the **Current** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367d8-136">-Default</span><span class="sxs-lookup"><span data-stu-id="367d8-136">-Default</span></span>
<span data-ttu-id="367d8-137">Получает только подписку по умолчанию, то есть подписку, назначенную по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="367d8-137">Gets only the default subscription, that is, the subscription designated as "default."</span></span> <span data-ttu-id="367d8-138">По умолчанию **Get-AzureSubscription** получает все подписки в учетных записях Azure.</span><span class="sxs-lookup"><span data-stu-id="367d8-138">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>
<span data-ttu-id="367d8-139">Чтобы назначить подписку по умолчанию, используйте параметр **по умолчанию** командлета **SELECT-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="367d8-139">To designate a subscription as "default," use the **Default** parameter of the **Select-AzureSubscription** cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367d8-140">-ExtendedDetails</span><span class="sxs-lookup"><span data-stu-id="367d8-140">-ExtendedDetails</span></span>
<span data-ttu-id="367d8-141">Возвращает сведения о квоте для подписки в дополнение к стандартным параметрам.</span><span class="sxs-lookup"><span data-stu-id="367d8-141">Returns quota information for the subscription, in addition to the standard settings.</span></span>

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

### <span data-ttu-id="367d8-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="367d8-142">-Profile</span></span>
<span data-ttu-id="367d8-143">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="367d8-143">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="367d8-144">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="367d8-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="367d8-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="367d8-145">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d8-146">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="367d8-146">-SubscriptionName</span></span>
<span data-ttu-id="367d8-147">Возвращает только указанную подписку.</span><span class="sxs-lookup"><span data-stu-id="367d8-147">Gets only the specified subscription.</span></span>
<span data-ttu-id="367d8-148">Введите имя подписки.</span><span class="sxs-lookup"><span data-stu-id="367d8-148">Enter the subscription name.</span></span>
<span data-ttu-id="367d8-149">Значение чувствительно к регистру.</span><span class="sxs-lookup"><span data-stu-id="367d8-149">The value is case-sensitive.</span></span>
<span data-ttu-id="367d8-150">Подстановочные знаки не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="367d8-150">Wildcard characters are not supported.</span></span>
<span data-ttu-id="367d8-151">По умолчанию **Get-AzureSubscription** получает все подписки в учетных записях Azure.</span><span class="sxs-lookup"><span data-stu-id="367d8-151">By default, **Get-AzureSubscription** gets all subscriptions in your Azure accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367d8-152">CommonParameters</span></span>
<span data-ttu-id="367d8-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="367d8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367d8-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367d8-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367d8-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="367d8-155">INPUTS</span></span>

### <span data-ttu-id="367d8-156">Ничего</span><span class="sxs-lookup"><span data-stu-id="367d8-156">None</span></span>
<span data-ttu-id="367d8-157">Вы можете передать входные данные свойству **SubscriptionName** по имени, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="367d8-157">You can pipe input to the **SubscriptionName** property by name, but not by value.</span></span>

## <span data-ttu-id="367d8-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="367d8-158">OUTPUTS</span></span>

### <span data-ttu-id="367d8-159">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="367d8-159">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureSubscription</span></span>

## <span data-ttu-id="367d8-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="367d8-160">NOTES</span></span>
* <span data-ttu-id="367d8-161">Get-AzureSubscription получает данные из файла данных подписки, создаваемого командлетами **Add-AzureAccount** и **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="367d8-161">Get-AzureSubscription gets data from the subscription data file that the **Add-AzureAccount** and **Import-PublishSettingsFile** cmdlets create.</span></span>

## <span data-ttu-id="367d8-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="367d8-162">RELATED LINKS</span></span>

[<span data-ttu-id="367d8-163">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="367d8-163">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="367d8-164">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="367d8-164">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="367d8-165">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="367d8-165">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="367d8-166">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="367d8-166">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="367d8-167">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="367d8-167">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


