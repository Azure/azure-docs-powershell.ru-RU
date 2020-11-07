---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728324"
---
# <span data-ttu-id="59972-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="59972-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="59972-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59972-102">SYNOPSIS</span></span>
<span data-ttu-id="59972-103">Развертывает веб-приложение Azure из почтового файла, использующего zipdeploy, в формате ZIP, JAR или WAR.</span><span class="sxs-lookup"><span data-stu-id="59972-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="59972-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59972-104">SYNTAX</span></span>

### <span data-ttu-id="59972-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="59972-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59972-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="59972-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59972-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59972-107">DESCRIPTION</span></span>
<span data-ttu-id="59972-108">Командлет **Publish-AzWebApp** отправляет содержимое в существующее веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="59972-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="59972-109">Содержимое должно упаковываться в ZIP-файл, если используются стеки, такие как .NET, Python или Node, или WAR-файл, если используется Java.</span><span class="sxs-lookup"><span data-stu-id="59972-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="59972-110">Содержимое должно быть предварительно собрано и готово к выполнению без дополнительных шагов сборки во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="59972-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="59972-111">Этот командлет использует функции KUDU zipdeploy и wardeploy для развертывания содержимого.</span><span class="sxs-lookup"><span data-stu-id="59972-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="59972-112">Сведения о том, как работают zipdeploy и wardeploy, и как правильно упаковать веб-приложение для развертывания, можно на вики-сайте KUDU.</span><span class="sxs-lookup"><span data-stu-id="59972-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="59972-113"> https://aka.ms/kuduzipdeploy и https://aka.ms/kuduwardeploy содержат полезные сведения о zipdeploy и wardeploy.</span><span class="sxs-lookup"><span data-stu-id="59972-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="59972-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59972-114">EXAMPLES</span></span>

### <span data-ttu-id="59972-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59972-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="59972-116">Передает содержимое app.zip в веб-приложение MyApp, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="59972-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="59972-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="59972-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="59972-118">Передает содержимое javaproject. war в промежуточный слот веб-приложения с именем ContosoApp, которое принадлежит группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="59972-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="59972-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="59972-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="59972-120">Передает содержимое app.zip в веб-приложение с именем ContosoApp, которое принадлежит к группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="59972-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="59972-121">Командлет будет запущен в фоновом задании.</span><span class="sxs-lookup"><span data-stu-id="59972-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="59972-122">Пример 4</span><span class="sxs-lookup"><span data-stu-id="59972-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

<span data-ttu-id="59972-123">Передает содержимое java_app. jar в веб-приложение с именем ContosoApp, которое принадлежит к группе ресурсов ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="59972-123">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="59972-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59972-124">PARAMETERS</span></span>

### <span data-ttu-id="59972-125">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="59972-125">-ArchivePath</span></span>
<span data-ttu-id="59972-126">Путь к файлу архива.</span><span class="sxs-lookup"><span data-stu-id="59972-126">The path of the archive file.</span></span> <span data-ttu-id="59972-127">Поддерживаются ZIP, WAR и JAR.</span><span class="sxs-lookup"><span data-stu-id="59972-127">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="59972-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59972-128">-AsJob</span></span>
<span data-ttu-id="59972-129">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="59972-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59972-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59972-130">-DefaultProfile</span></span>
<span data-ttu-id="59972-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59972-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59972-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59972-132">-Name</span></span>
<span data-ttu-id="59972-133">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="59972-133">The name of the web app.</span></span>

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

### <span data-ttu-id="59972-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59972-134">-ResourceGroupName</span></span>
<span data-ttu-id="59972-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59972-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="59972-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="59972-136">-Slot</span></span>
<span data-ttu-id="59972-137">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="59972-137">The name of the web app slot.</span></span>

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

### <span data-ttu-id="59972-138">-WebApp</span><span class="sxs-lookup"><span data-stu-id="59972-138">-WebApp</span></span>
<span data-ttu-id="59972-139">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="59972-139">The web app object</span></span>

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

### <span data-ttu-id="59972-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59972-140">CommonParameters</span></span>
<span data-ttu-id="59972-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59972-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59972-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59972-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59972-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59972-143">INPUTS</span></span>

### <span data-ttu-id="59972-144">System. String</span><span class="sxs-lookup"><span data-stu-id="59972-144">System.String</span></span>

### <span data-ttu-id="59972-145">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="59972-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="59972-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59972-146">OUTPUTS</span></span>

### <span data-ttu-id="59972-147">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="59972-147">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="59972-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="59972-148">NOTES</span></span>

## <span data-ttu-id="59972-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59972-149">RELATED LINKS</span></span>
