---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 2dfa72867655b95ea752c23c8605f19e7544e8e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556436"
---
# <span data-ttu-id="3b15b-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3b15b-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="3b15b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b15b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b15b-103">Создание веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3b15b-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b15b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b15b-104">SYNTAX</span></span>

### <span data-ttu-id="3b15b-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b15b-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b15b-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="3b15b-106">PrivateRegistry</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] -ContainerImageName <String> -ContainerRegistryUrl <String>
 -ContainerRegistryUser <String> -ContainerRegistryPassword <SecureString>
 [-EnableContainerContinuousDeployment] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b15b-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b15b-107">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>]
 [-EnableContainerContinuousDeployment] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-IncludeSourceWebAppSlots] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b15b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b15b-108">DESCRIPTION</span></span>
<span data-ttu-id="3b15b-109">Командлет **New-AzureRmWebApp** создает веб-приложение Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="3b15b-109">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="3b15b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b15b-110">EXAMPLES</span></span>

### <span data-ttu-id="3b15b-111">Пример 1: создание веб-приложения</span><span class="sxs-lookup"><span data-stu-id="3b15b-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="3b15b-112">Эта команда создает веб-приложение Azure с именем ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных (Западная часть США и т. д.).</span><span class="sxs-lookup"><span data-stu-id="3b15b-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="3b15b-113">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="3b15b-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="3b15b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b15b-114">PARAMETERS</span></span>

### <span data-ttu-id="3b15b-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3b15b-115">-AppServicePlan</span></span>
<span data-ttu-id="3b15b-116">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="3b15b-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="3b15b-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="3b15b-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="3b15b-118">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="3b15b-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="3b15b-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="3b15b-119">-AseName</span></span>
<span data-ttu-id="3b15b-120">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="3b15b-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="3b15b-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b15b-121">-AseResourceGroupName</span></span>
<span data-ttu-id="3b15b-122">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="3b15b-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="3b15b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b15b-123">-AsJob</span></span>
<span data-ttu-id="3b15b-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3b15b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b15b-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="3b15b-125">-ContainerImageName</span></span>
<span data-ttu-id="3b15b-126">Имя и дополнительный тег в контейнере, например (изображение: тег)</span><span class="sxs-lookup"><span data-stu-id="3b15b-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="3b15b-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="3b15b-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="3b15b-128">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="3b15b-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="3b15b-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="3b15b-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="3b15b-130">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="3b15b-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="3b15b-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="3b15b-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="3b15b-132">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="3b15b-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="3b15b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b15b-133">-DefaultProfile</span></span>
<span data-ttu-id="3b15b-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b15b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b15b-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="3b15b-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="3b15b-136">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="3b15b-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="3b15b-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="3b15b-137">-GitRepositoryPath</span></span>
<span data-ttu-id="3b15b-138">Путь к репозиторию GitHub, containign веб-приложение для развертывания.</span><span class="sxs-lookup"><span data-stu-id="3b15b-138">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="3b15b-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="3b15b-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="3b15b-140">Параметр "игнорировать нестандартные имена узлов"</span><span class="sxs-lookup"><span data-stu-id="3b15b-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="3b15b-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="3b15b-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="3b15b-142">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="3b15b-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="3b15b-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="3b15b-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="3b15b-144">Параметр "включить WebApp слотов источника"</span><span class="sxs-lookup"><span data-stu-id="3b15b-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="3b15b-145">-Location</span><span class="sxs-lookup"><span data-stu-id="3b15b-145">-Location</span></span>
<span data-ttu-id="3b15b-146">Поиска</span><span class="sxs-lookup"><span data-stu-id="3b15b-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b15b-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b15b-147">-Name</span></span>
<span data-ttu-id="3b15b-148">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="3b15b-148">WebApp Name</span></span>

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

### <span data-ttu-id="3b15b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b15b-149">-ResourceGroupName</span></span>
<span data-ttu-id="3b15b-150">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3b15b-150">Resource Group Name</span></span>

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

### <span data-ttu-id="3b15b-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="3b15b-151">-SourceWebApp</span></span>
<span data-ttu-id="3b15b-152">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="3b15b-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="3b15b-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3b15b-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="3b15b-154">Идентификатор ресурса с существующим профилем диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="3b15b-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="3b15b-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b15b-155">-Confirm</span></span>
<span data-ttu-id="3b15b-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b15b-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b15b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b15b-157">-WhatIf</span></span>
<span data-ttu-id="3b15b-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b15b-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b15b-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b15b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b15b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b15b-160">CommonParameters</span></span>
<span data-ttu-id="3b15b-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b15b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b15b-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b15b-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b15b-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b15b-163">INPUTS</span></span>

### <span data-ttu-id="3b15b-164">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="3b15b-164">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="3b15b-165">Параметры: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3b15b-165">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="3b15b-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b15b-166">OUTPUTS</span></span>

### <span data-ttu-id="3b15b-167">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="3b15b-167">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="3b15b-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b15b-168">NOTES</span></span>

## <span data-ttu-id="3b15b-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b15b-169">RELATED LINKS</span></span>

[<span data-ttu-id="3b15b-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3b15b-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="3b15b-171">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3b15b-171">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="3b15b-172">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3b15b-172">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="3b15b-173">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3b15b-173">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3b15b-174">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3b15b-174">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


