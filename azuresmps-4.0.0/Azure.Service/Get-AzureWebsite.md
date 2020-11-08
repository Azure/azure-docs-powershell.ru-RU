---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076274"
---
# <span data-ttu-id="a073f-101">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a073f-101">Get-AzureWebsite</span></span>

## <span data-ttu-id="a073f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a073f-102">SYNOPSIS</span></span>
<span data-ttu-id="a073f-103">Получение веб-сайтов Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="a073f-103">Gets Azure websites in the current subscription.</span></span>

## <span data-ttu-id="a073f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a073f-104">SYNTAX</span></span>

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a073f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a073f-105">DESCRIPTION</span></span>
<span data-ttu-id="a073f-106">Командлет **Get-AzureWebsite** получает сведения о веб-сайтах Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="a073f-106">The **Get-AzureWebsite** cmdlet gets information about Azure websites in the current subscription.</span></span>

<span data-ttu-id="a073f-107">По умолчанию **Get-AzureWebsite** получает все веб-сайты Azure в текущей подписке и возвращает объект, который предоставляет основные сведения о сайтах.</span><span class="sxs-lookup"><span data-stu-id="a073f-107">By default, **Get-AzureWebsite** gets all Azure websites in the current subscription and returns an object that provides basic information about the sites.</span></span>
<span data-ttu-id="a073f-108">При использовании параметра *Name* **Get-AzureWebsite** возвращает объект с подробными сведениями, в том числе с подробными сведениями о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a073f-108">When you use the *Name* parameter, **Get-AzureWebsite** returns an object with extensive information, including configuration details.</span></span>

<span data-ttu-id="a073f-109">Текущая подписка — это подписку, обозначенную как "Текущая".</span><span class="sxs-lookup"><span data-stu-id="a073f-109">The current subscription is the subscription that is designated as "current."</span></span> <span data-ttu-id="a073f-110">Чтобы найти текущую подписку, используйте *текущий* параметр командлета [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .</span><span class="sxs-lookup"><span data-stu-id="a073f-110">To find the current subscription, use the *Current* parameter of the [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet.</span></span>
<span data-ttu-id="a073f-111">Чтобы изменить текущую подписку, используйте командлет [SELECT-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .</span><span class="sxs-lookup"><span data-stu-id="a073f-111">To change the current subscription, use the [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) cmdlet.</span></span>

<span data-ttu-id="a073f-112">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a073f-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a073f-113">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a073f-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="a073f-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a073f-114">EXAMPLES</span></span>

### <span data-ttu-id="a073f-115">Пример 1: получение всех веб-сайтов в подписке</span><span class="sxs-lookup"><span data-stu-id="a073f-115">Example 1: Get all websites in the subscription</span></span>
```
PS C:\> Get-AzureWebsite
```

<span data-ttu-id="a073f-116">Эта команда получает все веб-сайты Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="a073f-116">This command gets all Azure websites in the current subscription.</span></span>

### <span data-ttu-id="a073f-117">Пример 2: получение веб-сайта по имени</span><span class="sxs-lookup"><span data-stu-id="a073f-117">Example 2: Get a website by name</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

<span data-ttu-id="a073f-118">Эта команда получает подробные сведения о веб-сайте ContosoWeb Azure, включая сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a073f-118">This command gets detailed information about the ContosoWeb Azure website, including configuration information.</span></span>
<span data-ttu-id="a073f-119">При использовании параметра *Name* **Get-AzureWebsite** возвращает объект **SiteWithConfig** с расширенными сведениями о веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="a073f-119">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object with extended information about the website.</span></span>

### <span data-ttu-id="a073f-120">Пример 3: получение подробных сведений обо всех веб-сайтах</span><span class="sxs-lookup"><span data-stu-id="a073f-120">Example 3: Get detailed information about all websites</span></span>
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

<span data-ttu-id="a073f-121">Эта команда получает подробные сведения обо всех веб-сайтах в подписке.</span><span class="sxs-lookup"><span data-stu-id="a073f-121">This command gets detailed information about all websites in the subscription.</span></span>
<span data-ttu-id="a073f-122">Она использует команду **Get-AzureWebsite** для получения всех веб-сайтов, а затем использует командлет **ForEach-Object** для получения каждого веб-сайта по имени.</span><span class="sxs-lookup"><span data-stu-id="a073f-122">It uses a **Get-AzureWebsite** command to get all websites and then uses the **ForEach-Object** cmdlet to get each website by name.</span></span>

### <span data-ttu-id="a073f-123">Пример 4: получение сведений о слоте развертывания</span><span class="sxs-lookup"><span data-stu-id="a073f-123">Example 4: Get information about a deployment slot</span></span>
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

<span data-ttu-id="a073f-124">Эта команда получает промежуточный слот развертывания на веб-сайте ContosoWeb.</span><span class="sxs-lookup"><span data-stu-id="a073f-124">This command gets the Staging deployment slot of the ContosoWeb website.</span></span>
<span data-ttu-id="a073f-125">Слоты развертывания позволяют тестировать разные версии веб-сайта Azure без их освобождения.</span><span class="sxs-lookup"><span data-stu-id="a073f-125">Deployment slots let you test different versions of your Azure website without releasing them to the public.</span></span>

### <span data-ttu-id="a073f-126">Пример 5: получение экземпляров веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="a073f-126">Example 5: Get website instances</span></span>
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

<span data-ttu-id="a073f-127">Команды в этом примере используют свойство Instances веб-сайта Azure для получения сведений о текущих экземплярах веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="a073f-127">The commands in this example use the Instances property of an Azure website to get information about currently running website instances.</span></span>
<span data-ttu-id="a073f-128">Свойство **Instances** Добавлено в объект **SiteWithConfig** в версии 0.8.3 модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="a073f-128">The **Instances** property was added to the **SiteWithConfig** object in version 0.8.3 of the Azure module.</span></span>

<span data-ttu-id="a073f-129">Первая команда получает идентификаторы экземпляров всех запущенных в данный момент экземпляров веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="a073f-129">The first command gets the instance IDs of all currently running instances of a website.</span></span>
<span data-ttu-id="a073f-130">Вторая команда возвращает число запущенных экземпляров веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="a073f-130">The second command gets the number of running instances of the website.</span></span>
<span data-ttu-id="a073f-131">Свойство **Count** можно использовать в любом массиве.</span><span class="sxs-lookup"><span data-stu-id="a073f-131">You can use the **Count** property on any array.</span></span>

## <span data-ttu-id="a073f-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a073f-132">PARAMETERS</span></span>

### <span data-ttu-id="a073f-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a073f-133">-Name</span></span>
<span data-ttu-id="a073f-134">Получение подробных сведений о конфигурации указанного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="a073f-134">Gets detailed configuration information about the specified website.</span></span>
<span data-ttu-id="a073f-135">Введите имя одного веб-сайта в подписке.</span><span class="sxs-lookup"><span data-stu-id="a073f-135">Enter the name of one website in the subscription.</span></span>
<span data-ttu-id="a073f-136">По умолчанию **Get-AzureWebsite** получает все веб-сайты в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="a073f-136">By default, **Get-AzureWebsite** gets all websites in the current subscription.</span></span>
<span data-ttu-id="a073f-137">Значение *Name* не поддерживает подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="a073f-137">The *Name* value does not support wildcard characters.</span></span>

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

### <span data-ttu-id="a073f-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="a073f-138">-Profile</span></span>
<span data-ttu-id="a073f-139">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a073f-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a073f-140">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a073f-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a073f-141">-Slot</span><span class="sxs-lookup"><span data-stu-id="a073f-141">-Slot</span></span>
<span data-ttu-id="a073f-142">Получает указанную область развертывания для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="a073f-142">Gets the specified deployment slot of the website.</span></span>
<span data-ttu-id="a073f-143">Введите имя гнезда, например "промежуточное хранение" или "производство".</span><span class="sxs-lookup"><span data-stu-id="a073f-143">Enter the slot name, such as "Staging" or "Production".</span></span>
<span data-ttu-id="a073f-144">Дополнительные сведения о слотах развертывания можно найти в разделе поэтапное развертывание на веб-сайтах Microsoft Azure https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .</span><span class="sxs-lookup"><span data-stu-id="a073f-144">For more information about deployment slots, see Staged Deployment on Microsoft Azure Web Siteshttps://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/.</span></span>
<span data-ttu-id="a073f-145">Чтобы добавить слот развертывания на существующий веб-сайт Azure, используйте командлет Set-AzureWebsite.</span><span class="sxs-lookup"><span data-stu-id="a073f-145">To add a deployment slot to an existing Azure website, use the Set-AzureWebsite cmdlet.</span></span>

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

### <span data-ttu-id="a073f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a073f-146">CommonParameters</span></span>
<span data-ttu-id="a073f-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a073f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a073f-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a073f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a073f-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a073f-149">INPUTS</span></span>

### <span data-ttu-id="a073f-150">Ничего</span><span class="sxs-lookup"><span data-stu-id="a073f-150">None</span></span>
<span data-ttu-id="a073f-151">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="a073f-151">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a073f-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a073f-152">OUTPUTS</span></span>

### <span data-ttu-id="a073f-153">Microsoft. WindowsAzure. Commands. Utilities. website. Services. Entities. site</span><span class="sxs-lookup"><span data-stu-id="a073f-153">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.Site</span></span>
<span data-ttu-id="a073f-154">По умолчанию **Get-AzureWebsite** возвращает массив объектов **сайта** .</span><span class="sxs-lookup"><span data-stu-id="a073f-154">By default, **Get-AzureWebsite** returns an array of **Site** objects.</span></span>

### <span data-ttu-id="a073f-155">Microsoft. WindowsAzure. Commands. Utilities. website. Services. Entities. SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="a073f-155">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.SiteWithConfig</span></span>
<span data-ttu-id="a073f-156">При использовании параметра *Name* **Get-AzureWebsite** возвращает объект **SiteWithConfig** .</span><span class="sxs-lookup"><span data-stu-id="a073f-156">When you use the *Name* parameter, **Get-AzureWebsite** returns a **SiteWithConfig** object.</span></span>

## <span data-ttu-id="a073f-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="a073f-157">NOTES</span></span>

## <span data-ttu-id="a073f-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a073f-158">RELATED LINKS</span></span>

[<span data-ttu-id="a073f-159">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a073f-159">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="a073f-160">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a073f-160">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="a073f-161">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a073f-161">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="a073f-162">Остановить-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a073f-162">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="a073f-163">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a073f-163">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


