---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222769"
---
# <span data-ttu-id="3054f-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3054f-101">New-AzWebApp</span></span>

## <span data-ttu-id="3054f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3054f-102">SYNOPSIS</span></span>
<span data-ttu-id="3054f-103">Создает Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3054f-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="3054f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3054f-104">SYNTAX</span></span>

### <span data-ttu-id="3054f-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3054f-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3054f-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="3054f-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3054f-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="3054f-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3054f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3054f-108">DESCRIPTION</span></span>
<span data-ttu-id="3054f-109">С **помощью cmdlet New-AzWebApp** в заданной группе ресурсов создается приложение Azure Web App, использующее указанный план и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="3054f-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="3054f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3054f-110">EXAMPLES</span></span>

### <span data-ttu-id="3054f-111">Пример 1. Создание веб-приложения</span><span class="sxs-lookup"><span data-stu-id="3054f-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="3054f-112">Эта команда создает azure Web App ContosoSite в существующей группе ресурсов Default-Web-WestUS в центре обработки данных West US.</span><span class="sxs-lookup"><span data-stu-id="3054f-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="3054f-113">Для этой команды используется существующий план службы приложений ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="3054f-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="3054f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3054f-114">PARAMETERS</span></span>

### <span data-ttu-id="3054f-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3054f-115">-AppServicePlan</span></span>
<span data-ttu-id="3054f-116">Имя плана службы или ИД плана служб приложения. Если веб-приложения и план обслуживания приложений находятся в разных группах ресурсов, используйте вместо названия ИД.</span><span class="sxs-lookup"><span data-stu-id="3054f-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="3054f-117">ИД плана обслуживания приложения можно получить с помощью: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id возвращает ИД плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="3054f-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="3054f-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="3054f-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="3054f-119">Параметры приложения переопределяют hashTable</span><span class="sxs-lookup"><span data-stu-id="3054f-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="3054f-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="3054f-120">-AseName</span></span>
<span data-ttu-id="3054f-121">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="3054f-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="3054f-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3054f-122">-AseResourceGroupName</span></span>
<span data-ttu-id="3054f-123">Имя группы ресурсов среды приложения</span><span class="sxs-lookup"><span data-stu-id="3054f-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="3054f-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3054f-124">-AsJob</span></span>
<span data-ttu-id="3054f-125">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3054f-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3054f-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="3054f-126">-ContainerImageName</span></span>
<span data-ttu-id="3054f-127">Имя контейнера изображения и дополнительный тег, например (image:tag)</span><span class="sxs-lookup"><span data-stu-id="3054f-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="3054f-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="3054f-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="3054f-129">Пароль регистратора частного контейнера</span><span class="sxs-lookup"><span data-stu-id="3054f-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="3054f-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="3054f-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="3054f-131">URL-адрес сервера частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="3054f-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="3054f-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="3054f-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="3054f-133">Имя пользователя частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="3054f-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="3054f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3054f-134">-DefaultProfile</span></span>
<span data-ttu-id="3054f-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3054f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3054f-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="3054f-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="3054f-137">Enables/Disables container continuous deployment webhook</span><span class="sxs-lookup"><span data-stu-id="3054f-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="3054f-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="3054f-138">-GitRepositoryPath</span></span>
<span data-ttu-id="3054f-139">Путь к репозиторию GitHub, содержащего веб-приложение для развертывания.</span><span class="sxs-lookup"><span data-stu-id="3054f-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="3054f-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="3054f-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="3054f-141">Параметр "Игнорировать пользовательские имена хостов"</span><span class="sxs-lookup"><span data-stu-id="3054f-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="3054f-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="3054f-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="3054f-143">Параметр "Игнорировать источник"</span><span class="sxs-lookup"><span data-stu-id="3054f-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="3054f-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="3054f-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="3054f-145">Параметр "Включить исходные ячейки Для веб-приложения WebApp"</span><span class="sxs-lookup"><span data-stu-id="3054f-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="3054f-146">-Location</span><span class="sxs-lookup"><span data-stu-id="3054f-146">-Location</span></span>
<span data-ttu-id="3054f-147">Расположение</span><span class="sxs-lookup"><span data-stu-id="3054f-147">Location</span></span>

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

### <span data-ttu-id="3054f-148">-Name</span><span class="sxs-lookup"><span data-stu-id="3054f-148">-Name</span></span>
<span data-ttu-id="3054f-149">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="3054f-149">WebApp Name</span></span>

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

### <span data-ttu-id="3054f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3054f-150">-ResourceGroupName</span></span>
<span data-ttu-id="3054f-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3054f-151">Resource Group Name</span></span>

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

### <span data-ttu-id="3054f-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="3054f-152">-SourceWebApp</span></span>
<span data-ttu-id="3054f-153">Объект Source WebApp</span><span class="sxs-lookup"><span data-stu-id="3054f-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="3054f-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3054f-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="3054f-155">ИД ресурса существующего профиля диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="3054f-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="3054f-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3054f-156">-Confirm</span></span>
<span data-ttu-id="3054f-157">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3054f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3054f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3054f-158">-WhatIf</span></span>
<span data-ttu-id="3054f-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3054f-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3054f-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3054f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3054f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3054f-161">CommonParameters</span></span>
<span data-ttu-id="3054f-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3054f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3054f-163">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3054f-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3054f-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3054f-164">INPUTS</span></span>

### <span data-ttu-id="3054f-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="3054f-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3054f-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3054f-166">OUTPUTS</span></span>

### <span data-ttu-id="3054f-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="3054f-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3054f-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3054f-168">NOTES</span></span>

## <span data-ttu-id="3054f-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3054f-169">RELATED LINKS</span></span>

[<span data-ttu-id="3054f-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3054f-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3054f-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3054f-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="3054f-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3054f-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="3054f-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3054f-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="3054f-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3054f-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


