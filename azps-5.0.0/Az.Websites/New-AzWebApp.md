---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246592"
---
# <span data-ttu-id="cef02-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cef02-101">New-AzWebApp</span></span>

## <span data-ttu-id="cef02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cef02-102">SYNOPSIS</span></span>
<span data-ttu-id="cef02-103">Создание веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="cef02-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="cef02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cef02-104">SYNTAX</span></span>

### <span data-ttu-id="cef02-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cef02-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cef02-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="cef02-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef02-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef02-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef02-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef02-108">DESCRIPTION</span></span>
<span data-ttu-id="cef02-109">Командлет **New-AzWebApp** создает веб-приложение Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="cef02-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="cef02-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cef02-110">EXAMPLES</span></span>

### <span data-ttu-id="cef02-111">Пример 1: создание веб-приложения</span><span class="sxs-lookup"><span data-stu-id="cef02-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="cef02-112">Эта команда создает веб-приложение Azure с именем ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных (Западная часть США и т. д.).</span><span class="sxs-lookup"><span data-stu-id="cef02-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="cef02-113">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="cef02-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="cef02-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cef02-114">PARAMETERS</span></span>

### <span data-ttu-id="cef02-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cef02-115">-AppServicePlan</span></span>
<span data-ttu-id="cef02-116">Имя плана служб приложений или ИД плана служб приложений. Если план служб WebApp и приложения находятся в разных группах ресурсов, используйте идентификатор вместо имени.</span><span class="sxs-lookup"><span data-stu-id="cef02-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="cef02-117">Идентификатор плана служб приложений можно получить с помощью: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. ID возвращает идентификатор плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="cef02-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="cef02-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="cef02-119">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="cef02-119">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="cef02-120">-AseName</span></span>
<span data-ttu-id="cef02-121">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="cef02-121">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef02-122">-AseResourceGroupName</span></span>
<span data-ttu-id="cef02-123">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="cef02-123">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cef02-124">-AsJob</span></span>
<span data-ttu-id="cef02-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cef02-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cef02-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="cef02-126">-ContainerImageName</span></span>
<span data-ttu-id="cef02-127">Имя и дополнительный тег в контейнере, например (изображение: тег)</span><span class="sxs-lookup"><span data-stu-id="cef02-127">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="cef02-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="cef02-129">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="cef02-129">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="cef02-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="cef02-131">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="cef02-131">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="cef02-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="cef02-133">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="cef02-133">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef02-134">-DefaultProfile</span></span>
<span data-ttu-id="cef02-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cef02-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cef02-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="cef02-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="cef02-137">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="cef02-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="cef02-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="cef02-138">-GitRepositoryPath</span></span>
<span data-ttu-id="cef02-139">Путь к репозиторию GitHub, содержащему развертываемое веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="cef02-139">Path to the GitHub repository containing the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="cef02-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="cef02-141">Параметр "игнорировать нестандартные имена узлов"</span><span class="sxs-lookup"><span data-stu-id="cef02-141">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="cef02-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="cef02-143">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="cef02-143">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="cef02-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="cef02-145">Параметр "включить WebApp слотов источника"</span><span class="sxs-lookup"><span data-stu-id="cef02-145">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-146">-Location</span><span class="sxs-lookup"><span data-stu-id="cef02-146">-Location</span></span>
<span data-ttu-id="cef02-147">Поиска</span><span class="sxs-lookup"><span data-stu-id="cef02-147">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cef02-148">-Name</span></span>
<span data-ttu-id="cef02-149">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="cef02-149">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef02-150">-ResourceGroupName</span></span>
<span data-ttu-id="cef02-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cef02-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="cef02-152">-SourceWebApp</span></span>
<span data-ttu-id="cef02-153">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="cef02-153">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cef02-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="cef02-155">Идентификатор ресурса с существующим профилем диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="cef02-155">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cef02-156">-Confirm</span></span>
<span data-ttu-id="cef02-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cef02-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef02-158">-WhatIf</span></span>
<span data-ttu-id="cef02-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cef02-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cef02-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cef02-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef02-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef02-161">CommonParameters</span></span>
<span data-ttu-id="cef02-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cef02-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef02-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef02-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef02-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cef02-164">INPUTS</span></span>

### <span data-ttu-id="cef02-165">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="cef02-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cef02-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef02-166">OUTPUTS</span></span>

### <span data-ttu-id="cef02-167">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="cef02-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cef02-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="cef02-168">NOTES</span></span>

## <span data-ttu-id="cef02-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cef02-169">RELATED LINKS</span></span>

[<span data-ttu-id="cef02-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cef02-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="cef02-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cef02-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="cef02-172">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cef02-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="cef02-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cef02-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="cef02-174">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cef02-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


