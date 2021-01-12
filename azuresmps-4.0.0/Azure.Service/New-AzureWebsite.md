---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110484"
---
# <span data-ttu-id="ae6ad-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ae6ad-101">New-AzureWebsite</span></span>

## <span data-ttu-id="ae6ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae6ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6ad-103">Создайте веб-сайт, который будет работать в Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="ae6ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae6ad-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae6ad-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae6ad-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6ad-106">В этой статье описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ae6ad-107">Чтобы получить версию модуля, который вы используете, в консоли Azure PowerShell введите `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ae6ad-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ae6ad-108">С помощью этой команды можно создать веб-сайт, который будет работать в Azure, и подготовиться к развертыванию через GitHub.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-108">The cmdlet creates a new website to run in Azure and prepares for deployment through GitHub.</span></span>

## <span data-ttu-id="ae6ad-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae6ad-109">EXAMPLES</span></span>

### <span data-ttu-id="ae6ad-110">Пример 1. Создание веб-сайта с помощью Git</span><span class="sxs-lookup"><span data-stu-id="ae6ad-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="ae6ad-111">В этом примере создается новый веб-сайт в Azure и локальный репозиторий GIT, который можно использовать для развертывания файлов на новом веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="ae6ad-112">Пример 2. Создание веб-сайта, интегрированного с GitHub</span><span class="sxs-lookup"><span data-stu-id="ae6ad-112">Example 2: Create website integrated with GitHub</span></span>
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

<span data-ttu-id="ae6ad-113">В этом примере создается новый веб-сайт, связанный с репозиторием GitHub с именем myaccount/myrepo.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-113">This example creates a new website linked to a GitHub repository named myaccount/myrepo.</span></span>
<span data-ttu-id="ae6ad-114">Обязательства для репозитория GitHub перенадвигаются на веб-сайт в Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-114">Commits to the GitHub repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="ae6ad-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae6ad-115">PARAMETERS</span></span>

### <span data-ttu-id="ae6ad-116">-Git</span><span class="sxs-lookup"><span data-stu-id="ae6ad-116">-Git</span></span>
<span data-ttu-id="ae6ad-117">Настраивает локальный репозиторий GIT и связывает его с веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="ae6ad-118">При этом настраивается репозиторий GIT в локальном каталоге и добавляется удаленный репозиторий azure, который ссылется на веб-сайт в Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

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

### <span data-ttu-id="ae6ad-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="ae6ad-119">-GitHub</span></span>
<span data-ttu-id="ae6ad-120">Указывает на то, что этот cmdlet связывает новый веб-сайт с существующим репозиторием GitHub.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-120">Indicates that this cmdlet links the new website to an existing GitHub repository.</span></span>
<span data-ttu-id="ae6ad-121">Обязательства для репозитория Giuthub перенадвигаются на веб-сайт в Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

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

### <span data-ttu-id="ae6ad-122">-GitHubCredentials</span><span class="sxs-lookup"><span data-stu-id="ae6ad-122">-GitHubCredentials</span></span>
<span data-ttu-id="ae6ad-123">Указывает имя пользователя и учетные данные для подключения к GitHub.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-123">Specifies the user name and password credentials to connect to GitHub.</span></span>

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

### <span data-ttu-id="ae6ad-124">-GitHubRepository</span><span class="sxs-lookup"><span data-stu-id="ae6ad-124">-GitHubRepository</span></span>
<span data-ttu-id="ae6ad-125">Указывает полное имя репозитория GitHub, связываемого с этим веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-125">Specifies the full name of the GitHub repository to link to this website.</span></span>
<span data-ttu-id="ae6ad-126">Например, `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="ae6ad-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="ae6ad-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="ae6ad-127">-Hostname</span></span>
<span data-ttu-id="ae6ad-128">Указывает альтернативное имя для нового веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="ae6ad-129">-Location</span><span class="sxs-lookup"><span data-stu-id="ae6ad-129">-Location</span></span>
<span data-ttu-id="ae6ad-130">Указывает расположение центра обработки данных, в котором вы хотите развернуть веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="ae6ad-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ae6ad-131">-Name</span></span>
<span data-ttu-id="ae6ad-132">Указывает имя веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="ae6ad-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="ae6ad-133">-Profile</span></span>
<span data-ttu-id="ae6ad-134">Определяет профиль Azure, с которого этот cmdlet будет читать данные.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae6ad-135">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae6ad-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="ae6ad-136">-PublishingUsername</span></span>
<span data-ttu-id="ae6ad-137">Указывает имя пользователя, указанное на портале Azure для развертывания Git.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="ae6ad-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="ae6ad-138">-Slot</span></span>
<span data-ttu-id="ae6ad-139">Указывает название слота для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="ae6ad-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6ad-140">CommonParameters</span></span>
<span data-ttu-id="ae6ad-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6ad-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6ad-142">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6ad-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6ad-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae6ad-143">INPUTS</span></span>

## <span data-ttu-id="ae6ad-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae6ad-144">OUTPUTS</span></span>

## <span data-ttu-id="ae6ad-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae6ad-145">NOTES</span></span>

## <span data-ttu-id="ae6ad-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae6ad-146">RELATED LINKS</span></span>

[<span data-ttu-id="ae6ad-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ae6ad-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


