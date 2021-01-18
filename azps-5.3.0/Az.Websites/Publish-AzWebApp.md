---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505758"
---
# <span data-ttu-id="c9ebe-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9ebe-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="c9ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ebe-103">Развертывает Azure Web App из ZIP-, JAR- или WAR-файла с помощью zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="c9ebe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c9ebe-104">SYNTAX</span></span>

### <span data-ttu-id="c9ebe-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c9ebe-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9ebe-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c9ebe-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="c9ebe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9ebe-107">DESCRIPTION</span></span>
<span data-ttu-id="c9ebe-108">С **помощью cmdlet Publish-AzWebApp** можно отправить контент в существующее приложение Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="c9ebe-109">Содержимое должно быть упаковано в ZIP-файл, если в Java используется стопка .NET, Python, Node или WAR или JAR-файл.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="c9ebe-110">Контент должен быть готовым и готовым к запуску без дополнительных действий по сборке во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="c9ebe-111">Этот cmdlet uses the Kudu zipdeploy andeploy features to deploy content.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="c9ebe-112">Подробные сведения о том, как zipdeploy и zipdeploy работают, а также о том, как правильно упаковировать веб-приложение для развертывания, можно на вики-сайте Куду.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="c9ebe-113"> https://aka.ms/kuduzipdeploy и https://aka.ms/kuduwardeploy содержат полезные сведения о zipdeploy и раздатной коде.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="c9ebe-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c9ebe-114">EXAMPLES</span></span>

### <span data-ttu-id="c9ebe-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9ebe-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="c9ebe-116">Загружает содержимое app.zip в веб-приложение MyApp, относящееся к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="c9ebe-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c9ebe-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="c9ebe-118">Загружает содержимое javaproject.war в промежуточное слот веб-приложения ContosoApp, принадлежащее группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="c9ebe-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c9ebe-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="c9ebe-120">Загружает содержимое app.zip в веб-приложение ContosoApp, принадлежащее группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="c9ebe-121">Он будет запускаться в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="c9ebe-122">Пример 4</span><span class="sxs-lookup"><span data-stu-id="c9ebe-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="c9ebe-123">Пример 5</span><span class="sxs-lookup"><span data-stu-id="c9ebe-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="c9ebe-124">Загружает содержимое java_app.jar в веб-приложение ContosoApp, принадлежащее группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="c9ebe-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9ebe-125">PARAMETERS</span></span>

### <span data-ttu-id="c9ebe-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="c9ebe-126">-ArchivePath</span></span>
<span data-ttu-id="c9ebe-127">Путь к файлу архива.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-127">The path of the archive file.</span></span> <span data-ttu-id="c9ebe-128">Поддерживаются zip, WAR и JAR.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-128">ZIP, WAR, and JAR are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9ebe-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9ebe-129">-AsJob</span></span>
<span data-ttu-id="c9ebe-130">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c9ebe-130">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9ebe-131">-Force</span><span class="sxs-lookup"><span data-stu-id="c9ebe-131">-Force</span></span>
<span data-ttu-id="c9ebe-132">Параметр "Принудительно удалить"</span><span class="sxs-lookup"><span data-stu-id="c9ebe-132">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9ebe-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ebe-133">-DefaultProfile</span></span>
<span data-ttu-id="c9ebe-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9ebe-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c9ebe-135">-Name</span></span>
<span data-ttu-id="c9ebe-136">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-136">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9ebe-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ebe-137">-ResourceGroupName</span></span>
<span data-ttu-id="c9ebe-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9ebe-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="c9ebe-139">-Slot</span></span>
<span data-ttu-id="c9ebe-140">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-140">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9ebe-141">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c9ebe-141">-WebApp</span></span>
<span data-ttu-id="c9ebe-142">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c9ebe-142">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9ebe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ebe-143">CommonParameters</span></span>
<span data-ttu-id="c9ebe-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ebe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ebe-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ebe-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ebe-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9ebe-146">INPUTS</span></span>

### <span data-ttu-id="c9ebe-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c9ebe-147">System.String</span></span>

### <span data-ttu-id="c9ebe-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c9ebe-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9ebe-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9ebe-149">OUTPUTS</span></span>

### <span data-ttu-id="c9ebe-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c9ebe-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9ebe-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c9ebe-151">NOTES</span></span>

## <span data-ttu-id="c9ebe-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9ebe-152">RELATED LINKS</span></span>
