---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075877"
---
# <span data-ttu-id="1bc27-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="1bc27-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="1bc27-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1bc27-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc27-103">Опубликуйте веб-проект Visual Studio на веб-сайте Microsoft Azure с помощью функции WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1bc27-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="1bc27-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1bc27-104">SYNTAX</span></span>

### <span data-ttu-id="1bc27-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="1bc27-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1bc27-106">Упаковать</span><span class="sxs-lookup"><span data-stu-id="1bc27-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1bc27-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bc27-107">DESCRIPTION</span></span>
<span data-ttu-id="1bc27-108">Опубликуйте веб-проект Visual Studio на веб-сайте Microsoft Azure с помощью функции WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1bc27-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="1bc27-109">Он может либо взять пакет веб-развертывания, либо опубликовать напрямую, а также выполнить построение проекта и публикацию с помощью веб-проекта Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1bc27-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="1bc27-110">Кроме того, он может заменить строки соединения в Web.config во время публикации.</span><span class="sxs-lookup"><span data-stu-id="1bc27-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="1bc27-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1bc27-111">EXAMPLES</span></span>

### <span data-ttu-id="1bc27-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1bc27-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="1bc27-113">Создание веб-проекта Visual Studio с конфигурацией "Отладка" (это означает использование Web.Debug.config) и публикация на веб-сайте Microsoft Azure с помощью функции WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1bc27-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1bc27-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1bc27-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="1bc27-115">Опубликуйте ZIP-файл пакета WebDeploy на сайте Microsoft Azure с помощью функции WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1bc27-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1bc27-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1bc27-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="1bc27-117">Опубликуйте папку пакета WebDeploy на веб-сайте Microsoft Azure с помощью функции WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1bc27-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1bc27-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="1bc27-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="1bc27-119">Создайте веб-проект Visual Studio, перезапишите строку подключения DefaultConnection в Web.config и опубликуйте ее на веб-сайте Microsoft Azure с помощью функции WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1bc27-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1bc27-120">Пример 5</span><span class="sxs-lookup"><span data-stu-id="1bc27-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="1bc27-121">Создайте веб-проект Visual Studio, перезапишите строку подключения DefaultConnection в Web.config и опубликуйте ее на веб-сайте Microsoft Azure с помощью функции WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1bc27-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="1bc27-122">Обратите внимание, что-DefaultConnection — это динамический параметр, который добавляется путем синтаксического анализа Web.config.</span><span class="sxs-lookup"><span data-stu-id="1bc27-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="1bc27-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1bc27-123">PARAMETERS</span></span>

### <span data-ttu-id="1bc27-124">-Configuration</span><span class="sxs-lookup"><span data-stu-id="1bc27-124">-Configuration</span></span>
<span data-ttu-id="1bc27-125">Конфигурация, используемая для построения проекта веб-приложения Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1bc27-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc27-126">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1bc27-126">-ConnectionString</span></span>
<span data-ttu-id="1bc27-127">Строки соединения, которые следует использовать для развертывания.</span><span class="sxs-lookup"><span data-stu-id="1bc27-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc27-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="1bc27-128">-DoNotDelete</span></span>
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

### <span data-ttu-id="1bc27-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1bc27-129">-Name</span></span>
<span data-ttu-id="1bc27-130">Имя веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="1bc27-130">The web site name.</span></span>

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

### <span data-ttu-id="1bc27-131">-Package</span><span class="sxs-lookup"><span data-stu-id="1bc27-131">-Package</span></span>
<span data-ttu-id="1bc27-132">Папка пакета WebDeploy для ZIP-файла, который должен быть опубликован в проекте Visual Studio Web Application.</span><span class="sxs-lookup"><span data-stu-id="1bc27-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc27-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="1bc27-133">-Profile</span></span>
<span data-ttu-id="1bc27-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1bc27-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1bc27-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1bc27-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1bc27-136">-ProjectFile</span><span class="sxs-lookup"><span data-stu-id="1bc27-136">-ProjectFile</span></span>
<span data-ttu-id="1bc27-137">Проект веб-приложения Visual Studio, который нужно опубликовать.</span><span class="sxs-lookup"><span data-stu-id="1bc27-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc27-138">-SetParametersFile</span><span class="sxs-lookup"><span data-stu-id="1bc27-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bc27-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="1bc27-139">-SkipAppData</span></span>
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

### <span data-ttu-id="1bc27-140">-Slot</span><span class="sxs-lookup"><span data-stu-id="1bc27-140">-Slot</span></span>
<span data-ttu-id="1bc27-141">Название слота веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="1bc27-141">The web site slot name.</span></span>

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

### <span data-ttu-id="1bc27-142">-Маркеры</span><span class="sxs-lookup"><span data-stu-id="1bc27-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc27-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc27-143">CommonParameters</span></span>
<span data-ttu-id="1bc27-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1bc27-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc27-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc27-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc27-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1bc27-146">INPUTS</span></span>

## <span data-ttu-id="1bc27-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bc27-147">OUTPUTS</span></span>

## <span data-ttu-id="1bc27-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="1bc27-148">NOTES</span></span>

## <span data-ttu-id="1bc27-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bc27-149">RELATED LINKS</span></span>

[<span data-ttu-id="1bc27-150">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1bc27-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="1bc27-151">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1bc27-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="1bc27-152">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1bc27-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="1bc27-153">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1bc27-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


