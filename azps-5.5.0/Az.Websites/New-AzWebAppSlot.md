---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242925"
---
# <span data-ttu-id="14f4f-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="14f4f-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="14f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="14f4f-103">Создает слот Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="14f4f-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="14f4f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14f4f-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14f4f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="14f4f-106">С **помощью cmdlet New-AzWebAppSlot** создается слот Azure Web App в заданной группе ресурсов, использующей указанный план и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="14f4f-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="14f4f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14f4f-107">EXAMPLES</span></span>

### <span data-ttu-id="14f4f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14f4f-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="14f4f-109">Эта команда создает слот с именем Slot001 в существующем веб-приложении ContosoSite в существующей группе ресурсов Default-Web-WestUS в центре обработки данных западной части США.</span><span class="sxs-lookup"><span data-stu-id="14f4f-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="14f4f-110">Для этой команды используется существующий план службы приложений ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="14f4f-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="14f4f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14f4f-111">PARAMETERS</span></span>

### <span data-ttu-id="14f4f-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="14f4f-112">-AppServicePlan</span></span>
<span data-ttu-id="14f4f-113">Имя плана службы или ИД плана служб приложения. Если план slot и App Services находятся в разных группах ресурсов, используйте вместо названия ИД.</span><span class="sxs-lookup"><span data-stu-id="14f4f-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="14f4f-114">ИД плана обслуживания приложения можно получить с помощью: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id возвращает ИД плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="14f4f-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="14f4f-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="14f4f-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="14f4f-116">Параметры приложения переопрепрещают параметры в hashtable</span><span class="sxs-lookup"><span data-stu-id="14f4f-116">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="14f4f-117">-AseName</span></span>
<span data-ttu-id="14f4f-118">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="14f4f-118">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f4f-119">-AseResourceGroupName</span></span>
<span data-ttu-id="14f4f-120">Имя группы ресурсов среды приложения</span><span class="sxs-lookup"><span data-stu-id="14f4f-120">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14f4f-121">-AsJob</span></span>
<span data-ttu-id="14f4f-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="14f4f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14f4f-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="14f4f-123">-ContainerImageName</span></span>
<span data-ttu-id="14f4f-124">Имя контейнера изображения и дополнительный тег, например (изображение:тег)</span><span class="sxs-lookup"><span data-stu-id="14f4f-124">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="14f4f-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="14f4f-126">Пароль регистратора частного контейнера</span><span class="sxs-lookup"><span data-stu-id="14f4f-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="14f4f-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="14f4f-128">URL-адрес сервера частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="14f4f-128">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="14f4f-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="14f4f-130">Имя пользователя частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="14f4f-130">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f4f-131">-DefaultProfile</span></span>
<span data-ttu-id="14f4f-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14f4f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14f4f-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="14f4f-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="14f4f-134">Enables/Disables container continuous deployment webhook</span><span class="sxs-lookup"><span data-stu-id="14f4f-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="14f4f-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="14f4f-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="14f4f-136">Параметр "Игнорировать пользовательские имена хостов"</span><span class="sxs-lookup"><span data-stu-id="14f4f-136">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="14f4f-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="14f4f-138">Параметр "Игнорировать источник"</span><span class="sxs-lookup"><span data-stu-id="14f4f-138">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-139">-Name</span><span class="sxs-lookup"><span data-stu-id="14f4f-139">-Name</span></span>
<span data-ttu-id="14f4f-140">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="14f4f-140">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f4f-141">-ResourceGroupName</span></span>
<span data-ttu-id="14f4f-142">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="14f4f-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="14f4f-143">-Slot</span></span>
<span data-ttu-id="14f4f-144">Название слота Webapp</span><span class="sxs-lookup"><span data-stu-id="14f4f-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="14f4f-145">-SourceWebApp</span></span>
<span data-ttu-id="14f4f-146">Объект Source WebApp</span><span class="sxs-lookup"><span data-stu-id="14f4f-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14f4f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f4f-147">CommonParameters</span></span>
<span data-ttu-id="14f4f-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f4f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f4f-149">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f4f-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f4f-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14f4f-150">INPUTS</span></span>

### <span data-ttu-id="14f4f-151">System.String</span><span class="sxs-lookup"><span data-stu-id="14f4f-151">System.String</span></span>

### <span data-ttu-id="14f4f-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="14f4f-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="14f4f-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14f4f-153">OUTPUTS</span></span>

### <span data-ttu-id="14f4f-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="14f4f-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="14f4f-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14f4f-155">NOTES</span></span>

## <span data-ttu-id="14f4f-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14f4f-156">RELATED LINKS</span></span>

[<span data-ttu-id="14f4f-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="14f4f-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="14f4f-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="14f4f-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="14f4f-159">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="14f4f-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="14f4f-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="14f4f-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="14f4f-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="14f4f-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="14f4f-162">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="14f4f-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="14f4f-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="14f4f-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="14f4f-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="14f4f-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
