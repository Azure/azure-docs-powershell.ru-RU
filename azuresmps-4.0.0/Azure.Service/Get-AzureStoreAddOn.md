---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075547"
---
# <span data-ttu-id="998a9-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="998a9-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="998a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="998a9-102">SYNOPSIS</span></span>
<span data-ttu-id="998a9-103">Получает доступные надстройки магазина Azure.</span><span class="sxs-lookup"><span data-stu-id="998a9-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="998a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="998a9-104">SYNTAX</span></span>

### <span data-ttu-id="998a9-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="998a9-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="998a9-106">Надстройка</span><span class="sxs-lookup"><span data-stu-id="998a9-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="998a9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="998a9-107">DESCRIPTION</span></span>
<span data-ttu-id="998a9-108">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="998a9-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="998a9-109">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="998a9-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="998a9-110">Получение всех доступных надстроек для приобретения из магазина Azure или получение существующих экземпляров надстроек для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="998a9-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="998a9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="998a9-111">EXAMPLES</span></span>

### <span data-ttu-id="998a9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="998a9-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="998a9-113">В этом примере получается список всех приобретенных экземпляров надстроек для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="998a9-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="998a9-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="998a9-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="998a9-115">В этом примере получается список всех доступных надстроек для приобретения в США из магазина Azure.</span><span class="sxs-lookup"><span data-stu-id="998a9-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="998a9-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="998a9-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="998a9-117">В этом примере выполняется получение надстройки с именем MyAddOn из приобретенного экземпляра надстройки в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="998a9-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="998a9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="998a9-118">PARAMETERS</span></span>

### <span data-ttu-id="998a9-119">-Country</span><span class="sxs-lookup"><span data-stu-id="998a9-119">-Country</span></span>
<span data-ttu-id="998a9-120">Если указан, возвращает только экземпляры надстроек Azure из магазина, доступные в указанной стране.</span><span class="sxs-lookup"><span data-stu-id="998a9-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="998a9-121">Значением по умолчанию является "US".</span><span class="sxs-lookup"><span data-stu-id="998a9-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998a9-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="998a9-122">-ListAvailable</span></span>
<span data-ttu-id="998a9-123">Возвращает доступные надстройки для приобретения из магазина Azure.</span><span class="sxs-lookup"><span data-stu-id="998a9-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998a9-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="998a9-124">-Name</span></span>
<span data-ttu-id="998a9-125">Возвращает надстройку, которая соответствует указанному имени.</span><span class="sxs-lookup"><span data-stu-id="998a9-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998a9-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="998a9-126">-Profile</span></span>
<span data-ttu-id="998a9-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="998a9-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="998a9-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="998a9-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="998a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998a9-129">CommonParameters</span></span>
<span data-ttu-id="998a9-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="998a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998a9-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="998a9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998a9-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="998a9-132">INPUTS</span></span>

## <span data-ttu-id="998a9-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="998a9-133">OUTPUTS</span></span>

## <span data-ttu-id="998a9-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="998a9-134">NOTES</span></span>

## <span data-ttu-id="998a9-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="998a9-135">RELATED LINKS</span></span>

[<span data-ttu-id="998a9-136">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="998a9-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="998a9-137">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="998a9-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="998a9-138">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="998a9-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


