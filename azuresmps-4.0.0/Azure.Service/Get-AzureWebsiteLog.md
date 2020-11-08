---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076506"
---
# <span data-ttu-id="a68f8-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="a68f8-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="a68f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a68f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a68f8-103">Получает журналы для указанного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="a68f8-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="a68f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a68f8-104">SYNTAX</span></span>

### <span data-ttu-id="a68f8-105">Копирован</span><span class="sxs-lookup"><span data-stu-id="a68f8-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a68f8-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="a68f8-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a68f8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a68f8-107">DESCRIPTION</span></span>
<span data-ttu-id="a68f8-108">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a68f8-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a68f8-109">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a68f8-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a68f8-110">Получает журнал для указанного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="a68f8-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="a68f8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a68f8-111">EXAMPLES</span></span>

### <span data-ttu-id="a68f8-112">Пример 1: запуск потоковой передачи журнала</span><span class="sxs-lookup"><span data-stu-id="a68f8-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="a68f8-113">В этом примере начинается потоковая передача журнала для всех журналов приложений.</span><span class="sxs-lookup"><span data-stu-id="a68f8-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="a68f8-114">Пример 2: запуск потоковой передачи журнала для журналов HTTP</span><span class="sxs-lookup"><span data-stu-id="a68f8-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="a68f8-115">В этом примере начинается потоковая передача журнала для журналов HTTP.</span><span class="sxs-lookup"><span data-stu-id="a68f8-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="a68f8-116">Пример 3: запуск потоковой передачи журнала для журналов ошибок</span><span class="sxs-lookup"><span data-stu-id="a68f8-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="a68f8-117">В этом примере начинается потоковая передача журнала и отображаются только журналы ошибок.</span><span class="sxs-lookup"><span data-stu-id="a68f8-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="a68f8-118">Пример 4: отображение журналов avaiable</span><span class="sxs-lookup"><span data-stu-id="a68f8-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="a68f8-119">В этом примере перечислены все доступные пути журналов на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="a68f8-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="a68f8-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a68f8-120">PARAMETERS</span></span>

### <span data-ttu-id="a68f8-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="a68f8-121">-ListPath</span></span>
<span data-ttu-id="a68f8-122">Указывает, следует ли отображать пути к журналу.</span><span class="sxs-lookup"><span data-stu-id="a68f8-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a68f8-123">-Сообщение</span><span class="sxs-lookup"><span data-stu-id="a68f8-123">-Message</span></span>
<span data-ttu-id="a68f8-124">Указывает строку, которая будет использоваться для фильтрации сообщения журнала.</span><span class="sxs-lookup"><span data-stu-id="a68f8-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="a68f8-125">Будут возвращены только журналы, содержащие эту строку.</span><span class="sxs-lookup"><span data-stu-id="a68f8-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a68f8-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a68f8-126">-Name</span></span>
<span data-ttu-id="a68f8-127">Имя веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="a68f8-127">The name of the website.</span></span>

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

### <span data-ttu-id="a68f8-128">-Path</span><span class="sxs-lookup"><span data-stu-id="a68f8-128">-Path</span></span>
<span data-ttu-id="a68f8-129">Путь, из которого будет получен журнал.</span><span class="sxs-lookup"><span data-stu-id="a68f8-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="a68f8-130">По умолчанию он является корневым, то есть включает все пути.</span><span class="sxs-lookup"><span data-stu-id="a68f8-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a68f8-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="a68f8-131">-Profile</span></span>
<span data-ttu-id="a68f8-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a68f8-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a68f8-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a68f8-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a68f8-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="a68f8-134">-Slot</span></span>
<span data-ttu-id="a68f8-135">Указывает имя гнезда.</span><span class="sxs-lookup"><span data-stu-id="a68f8-135">Specifies the slot name.</span></span>

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

### <span data-ttu-id="a68f8-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="a68f8-136">-Tail</span></span>
<span data-ttu-id="a68f8-137">Указывает, следует ли передавать журналы.</span><span class="sxs-lookup"><span data-stu-id="a68f8-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a68f8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68f8-138">CommonParameters</span></span>
<span data-ttu-id="a68f8-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a68f8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68f8-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68f8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68f8-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a68f8-141">INPUTS</span></span>

## <span data-ttu-id="a68f8-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a68f8-142">OUTPUTS</span></span>

## <span data-ttu-id="a68f8-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="a68f8-143">NOTES</span></span>

## <span data-ttu-id="a68f8-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a68f8-144">RELATED LINKS</span></span>

[<span data-ttu-id="a68f8-145">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a68f8-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="a68f8-146">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a68f8-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="a68f8-147">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a68f8-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="a68f8-148">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a68f8-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


