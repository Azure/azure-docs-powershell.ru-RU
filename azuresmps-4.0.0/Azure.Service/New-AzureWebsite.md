---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076184"
---
# <span data-ttu-id="35ebe-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="35ebe-101">New-AzureWebsite</span></span>

## <span data-ttu-id="35ebe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="35ebe-103">Создание нового веб-сайта для работы в Azure.</span><span class="sxs-lookup"><span data-stu-id="35ebe-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="35ebe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35ebe-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="35ebe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ebe-105">DESCRIPTION</span></span>
<span data-ttu-id="35ebe-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35ebe-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="35ebe-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="35ebe-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="35ebe-108">Командлет создает новый веб-сайт для работы в Azure и готовится к развертыванию с помощью GitHub.</span><span class="sxs-lookup"><span data-stu-id="35ebe-108">The cmdlet creates a new website to run in Azure and prepares for deployment through Github.</span></span>

## <span data-ttu-id="35ebe-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35ebe-109">EXAMPLES</span></span>

### <span data-ttu-id="35ebe-110">Пример 1: создание нового веб-сайта с помощью Git</span><span class="sxs-lookup"><span data-stu-id="35ebe-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="35ebe-111">В этом примере создается новый веб-сайт в Azure и локальный репозиторий Git, который можно использовать для развертывания файлов на новом веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="35ebe-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="35ebe-112">Пример 2: создание веб-сайта, интегрированного с GitHub</span><span class="sxs-lookup"><span data-stu-id="35ebe-112">Example 2: Create website integrated with Github</span></span>
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

<span data-ttu-id="35ebe-113">В этом примере создается новый веб-сайт, связанный с репозиторием GitHub с именем Моя учетная запись/myrepo.</span><span class="sxs-lookup"><span data-stu-id="35ebe-113">This example creates a new website linked to a Github repository named myaccount/myrepo.</span></span>
<span data-ttu-id="35ebe-114">Фиксация в репозитории GitHub помещается на веб-сайт в Azure.</span><span class="sxs-lookup"><span data-stu-id="35ebe-114">Commits to the Github repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="35ebe-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35ebe-115">PARAMETERS</span></span>

### <span data-ttu-id="35ebe-116">-Git</span><span class="sxs-lookup"><span data-stu-id="35ebe-116">-Git</span></span>
<span data-ttu-id="35ebe-117">Настройка локального репозитория Git и связывание его с веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="35ebe-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="35ebe-118">Если этот параметр задан, то он настраивает репозиторий Git в локальном каталоге и добавляет удаленный репозиторий с именем "Azure", который ссылается на веб-сайт в Azure.</span><span class="sxs-lookup"><span data-stu-id="35ebe-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

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

### <span data-ttu-id="35ebe-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="35ebe-119">-GitHub</span></span>
<span data-ttu-id="35ebe-120">Указывает на то, что этот командлет связывает новый веб-сайт с существующим репозиторием GitHub.</span><span class="sxs-lookup"><span data-stu-id="35ebe-120">Indicates that this cmdlet links the new website to an existing Github repository.</span></span>
<span data-ttu-id="35ebe-121">Фиксация в репозитории Giuthub помещаются на веб-сайт в Azure.</span><span class="sxs-lookup"><span data-stu-id="35ebe-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

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

### <span data-ttu-id="35ebe-122">-GithubCredentials</span><span class="sxs-lookup"><span data-stu-id="35ebe-122">-GithubCredentials</span></span>
<span data-ttu-id="35ebe-123">Указывает имя пользователя и пароль для подключения к GitHub.</span><span class="sxs-lookup"><span data-stu-id="35ebe-123">Specifies the user name and password credentials to connect to Github.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ebe-124">-GithubRepository</span><span class="sxs-lookup"><span data-stu-id="35ebe-124">-GithubRepository</span></span>
<span data-ttu-id="35ebe-125">Указывает полное имя репозитория GitHub для ссылки на этот веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="35ebe-125">Specifies the full name of the Github repository to link to this website.</span></span>
<span data-ttu-id="35ebe-126">Например, `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="35ebe-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="35ebe-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="35ebe-127">-Hostname</span></span>
<span data-ttu-id="35ebe-128">Указывает альтернативное имя узла для нового веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="35ebe-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="35ebe-129">-Location</span><span class="sxs-lookup"><span data-stu-id="35ebe-129">-Location</span></span>
<span data-ttu-id="35ebe-130">Указывает расположение центра обработки данных, на котором вы хотите развернуть веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="35ebe-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="35ebe-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35ebe-131">-Name</span></span>
<span data-ttu-id="35ebe-132">Указывает имя веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="35ebe-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="35ebe-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="35ebe-133">-Profile</span></span>
<span data-ttu-id="35ebe-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="35ebe-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="35ebe-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35ebe-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="35ebe-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="35ebe-136">-PublishingUsername</span></span>
<span data-ttu-id="35ebe-137">Указывает имя пользователя, указанное на портале Azure для развертывания Git.</span><span class="sxs-lookup"><span data-stu-id="35ebe-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="35ebe-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="35ebe-138">-Slot</span></span>
<span data-ttu-id="35ebe-139">Указывает имя гнезда для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="35ebe-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="35ebe-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ebe-140">CommonParameters</span></span>
<span data-ttu-id="35ebe-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35ebe-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ebe-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ebe-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ebe-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35ebe-143">INPUTS</span></span>

## <span data-ttu-id="35ebe-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ebe-144">OUTPUTS</span></span>

## <span data-ttu-id="35ebe-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="35ebe-145">NOTES</span></span>

## <span data-ttu-id="35ebe-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35ebe-146">RELATED LINKS</span></span>

[<span data-ttu-id="35ebe-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="35ebe-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


