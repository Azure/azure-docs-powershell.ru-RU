---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 05ee02fcb1a1f03c2a9b349754009a178a1668b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566871"
---
# <span data-ttu-id="3e000-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e000-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="3e000-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e000-102">SYNOPSIS</span></span>
<span data-ttu-id="3e000-103">Создание веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3e000-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e000-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e000-104">SYNTAX</span></span>

### <span data-ttu-id="3e000-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e000-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e000-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e000-106">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e000-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e000-107">DESCRIPTION</span></span>
<span data-ttu-id="3e000-108">Командлет **New-AzureRmWebApp** создает веб-приложение Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="3e000-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="3e000-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e000-109">EXAMPLES</span></span>

### <span data-ttu-id="3e000-110">Пример 1: создание веб-приложения</span><span class="sxs-lookup"><span data-stu-id="3e000-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="3e000-111">Эта команда создает веб-приложение Azure с именем ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных (Западная часть США и т. д.).</span><span class="sxs-lookup"><span data-stu-id="3e000-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="3e000-112">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="3e000-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="3e000-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e000-113">PARAMETERS</span></span>

### <span data-ttu-id="3e000-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3e000-114">-AppServicePlan</span></span>
<span data-ttu-id="3e000-115">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="3e000-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="3e000-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="3e000-117">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="3e000-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="3e000-118">-AseName</span></span>
<span data-ttu-id="3e000-119">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="3e000-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e000-120">-AseResourceGroupName</span></span>
<span data-ttu-id="3e000-121">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="3e000-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e000-122">-AsJob</span></span>
<span data-ttu-id="3e000-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3e000-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e000-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e000-124">-DefaultProfile</span></span>
<span data-ttu-id="3e000-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e000-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="3e000-126">-GitRepositoryPath</span></span>
<span data-ttu-id="3e000-127">Путь к репозиторию GitHub, containign веб-приложение для развертывания.</span><span class="sxs-lookup"><span data-stu-id="3e000-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="3e000-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="3e000-129">Параметр "игнорировать нестандартные имена узлов"</span><span class="sxs-lookup"><span data-stu-id="3e000-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="3e000-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="3e000-131">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="3e000-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="3e000-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="3e000-133">Параметр "включить WebApp слотов источника"</span><span class="sxs-lookup"><span data-stu-id="3e000-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-134">-Location</span><span class="sxs-lookup"><span data-stu-id="3e000-134">-Location</span></span>
<span data-ttu-id="3e000-135">Поиска</span><span class="sxs-lookup"><span data-stu-id="3e000-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e000-136">-Name</span></span>
<span data-ttu-id="3e000-137">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="3e000-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e000-138">-ResourceGroupName</span></span>
<span data-ttu-id="3e000-139">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3e000-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="3e000-140">-SourceWebApp</span></span>
<span data-ttu-id="3e000-141">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="3e000-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3e000-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="3e000-143">Идентификатор ресурса с существующим профилем диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="3e000-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e000-144">-Confirm</span></span>
<span data-ttu-id="3e000-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e000-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e000-146">-WhatIf</span></span>
<span data-ttu-id="3e000-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e000-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e000-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e000-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e000-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e000-149">CommonParameters</span></span>
<span data-ttu-id="3e000-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e000-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e000-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e000-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e000-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e000-152">INPUTS</span></span>

### <span data-ttu-id="3e000-153">Семейств</span><span class="sxs-lookup"><span data-stu-id="3e000-153">Site</span></span>
<span data-ttu-id="3e000-154">Параметр "SourceWebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3e000-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3e000-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e000-155">OUTPUTS</span></span>

### <span data-ttu-id="3e000-156">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="3e000-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="3e000-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e000-157">NOTES</span></span>

## <span data-ttu-id="3e000-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e000-158">RELATED LINKS</span></span>

[<span data-ttu-id="3e000-159">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e000-159">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="3e000-160">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e000-160">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="3e000-161">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e000-161">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="3e000-162">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e000-162">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3e000-163">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3e000-163">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


