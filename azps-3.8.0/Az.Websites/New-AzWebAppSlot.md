---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065963"
---
# <span data-ttu-id="6f2ee-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6f2ee-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="6f2ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f2ee-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2ee-103">Создание слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2ee-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="6f2ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f2ee-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f2ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2ee-105">DESCRIPTION</span></span>
<span data-ttu-id="6f2ee-106">Командлет **New-AzWebAppSlot** создает слот веб-приложения Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="6f2ee-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="6f2ee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f2ee-107">EXAMPLES</span></span>

### <span data-ttu-id="6f2ee-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f2ee-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="6f2ee-109">Эта команда создает слот с именем Slot001 под существующими именами веб-приложений ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="6f2ee-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="6f2ee-110">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="6f2ee-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="6f2ee-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f2ee-111">PARAMETERS</span></span>

### <span data-ttu-id="6f2ee-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6f2ee-112">-AppServicePlan</span></span>
<span data-ttu-id="6f2ee-113">Имя плана служб приложений или ИД плана служб приложений. Если план обслуживания слотов и приложений находятся в разных группах ресурсов, используйте идентификатор вместо имени.</span><span class="sxs-lookup"><span data-stu-id="6f2ee-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="6f2ee-114">Идентификатор плана служб приложений можно получить с помощью: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. ID возвращает идентификатор плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="6f2ee-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="6f2ee-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="6f2ee-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="6f2ee-116">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="6f2ee-116">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="6f2ee-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="6f2ee-117">-AseName</span></span>
<span data-ttu-id="6f2ee-118">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="6f2ee-118">App Service Environment Name</span></span>

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

### <span data-ttu-id="6f2ee-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f2ee-119">-AseResourceGroupName</span></span>
<span data-ttu-id="6f2ee-120">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="6f2ee-120">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="6f2ee-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f2ee-121">-AsJob</span></span>
<span data-ttu-id="6f2ee-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6f2ee-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f2ee-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="6f2ee-123">-ContainerImageName</span></span>
<span data-ttu-id="6f2ee-124">Имя и дополнительный тег в контейнере, например (изображение: тег)</span><span class="sxs-lookup"><span data-stu-id="6f2ee-124">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="6f2ee-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="6f2ee-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="6f2ee-126">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="6f2ee-126">Private Container Registry Password</span></span>

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

### <span data-ttu-id="6f2ee-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="6f2ee-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="6f2ee-128">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="6f2ee-128">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="6f2ee-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="6f2ee-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="6f2ee-130">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="6f2ee-130">Private Container Registry Username</span></span>

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

### <span data-ttu-id="6f2ee-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2ee-131">-DefaultProfile</span></span>
<span data-ttu-id="6f2ee-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2ee-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f2ee-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="6f2ee-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="6f2ee-134">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="6f2ee-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="6f2ee-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="6f2ee-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="6f2ee-136">Параметр "пропускать пользовательские HostName"</span><span class="sxs-lookup"><span data-stu-id="6f2ee-136">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="6f2ee-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="6f2ee-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="6f2ee-138">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="6f2ee-138">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="6f2ee-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f2ee-139">-Name</span></span>
<span data-ttu-id="6f2ee-140">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="6f2ee-140">Webapp Name</span></span>

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

### <span data-ttu-id="6f2ee-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f2ee-141">-ResourceGroupName</span></span>
<span data-ttu-id="6f2ee-142">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6f2ee-142">Resource Group Name</span></span>

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

### <span data-ttu-id="6f2ee-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="6f2ee-143">-Slot</span></span>
<span data-ttu-id="6f2ee-144">Название гнезда webapp</span><span class="sxs-lookup"><span data-stu-id="6f2ee-144">Webapp Slot Name</span></span>

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

### <span data-ttu-id="6f2ee-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="6f2ee-145">-SourceWebApp</span></span>
<span data-ttu-id="6f2ee-146">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="6f2ee-146">Source WebApp Object</span></span>

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

### <span data-ttu-id="6f2ee-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2ee-147">CommonParameters</span></span>
<span data-ttu-id="6f2ee-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f2ee-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2ee-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f2ee-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2ee-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f2ee-150">INPUTS</span></span>

### <span data-ttu-id="6f2ee-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6f2ee-151">System.String</span></span>

### <span data-ttu-id="6f2ee-152">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="6f2ee-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6f2ee-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2ee-153">OUTPUTS</span></span>

### <span data-ttu-id="6f2ee-154">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="6f2ee-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6f2ee-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f2ee-155">NOTES</span></span>

## <span data-ttu-id="6f2ee-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f2ee-156">RELATED LINKS</span></span>

[<span data-ttu-id="6f2ee-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6f2ee-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="6f2ee-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6f2ee-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="6f2ee-159">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6f2ee-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="6f2ee-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6f2ee-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="6f2ee-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6f2ee-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="6f2ee-162">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6f2ee-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="6f2ee-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6f2ee-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="6f2ee-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6f2ee-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
