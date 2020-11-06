---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569148"
---
# <span data-ttu-id="b216c-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b216c-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="b216c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b216c-102">SYNOPSIS</span></span>
<span data-ttu-id="b216c-103">Создание веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b216c-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b216c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b216c-104">SYNTAX</span></span>

### <span data-ttu-id="b216c-105">S1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b216c-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b216c-106">S2</span><span class="sxs-lookup"><span data-stu-id="b216c-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b216c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b216c-107">DESCRIPTION</span></span>
<span data-ttu-id="b216c-108">Командлет **New-AzureRmWebApp** создает веб-приложение Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="b216c-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="b216c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b216c-109">EXAMPLES</span></span>

### <span data-ttu-id="b216c-110">Пример 1: создание веб-приложения</span><span class="sxs-lookup"><span data-stu-id="b216c-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="b216c-111">Эта команда создает веб-приложение Azure с именем ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных (Западная часть США и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b216c-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="b216c-112">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b216c-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="b216c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b216c-113">PARAMETERS</span></span>

### <span data-ttu-id="b216c-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b216c-114">-AppServicePlan</span></span>
<span data-ttu-id="b216c-115">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="b216c-115">App Service Plan Name</span></span>

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

### <span data-ttu-id="b216c-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="b216c-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="b216c-117">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="b216c-117">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="b216c-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="b216c-118">-AseName</span></span>
<span data-ttu-id="b216c-119">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="b216c-119">App Service Environment Name</span></span>

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

### <span data-ttu-id="b216c-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b216c-120">-AseResourceGroupName</span></span>
<span data-ttu-id="b216c-121">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="b216c-121">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="b216c-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="b216c-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="b216c-123">Параметр "игнорировать нестандартные имена узлов"</span><span class="sxs-lookup"><span data-stu-id="b216c-123">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="b216c-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="b216c-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="b216c-125">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="b216c-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="b216c-126">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="b216c-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="b216c-127">Параметр "включить WebApp слотов источника"</span><span class="sxs-lookup"><span data-stu-id="b216c-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b216c-128">-Location</span><span class="sxs-lookup"><span data-stu-id="b216c-128">-Location</span></span>
<span data-ttu-id="b216c-129">Поиска</span><span class="sxs-lookup"><span data-stu-id="b216c-129">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b216c-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b216c-130">-Name</span></span>
<span data-ttu-id="b216c-131">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="b216c-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b216c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b216c-132">-ResourceGroupName</span></span>
<span data-ttu-id="b216c-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b216c-133">Resource Group Name</span></span>

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

### <span data-ttu-id="b216c-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="b216c-134">-SourceWebApp</span></span>
<span data-ttu-id="b216c-135">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="b216c-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b216c-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="b216c-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="b216c-137">Идентификатор профиля диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="b216c-137">Traffic Manager Profile Id</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b216c-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="b216c-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="b216c-139">Имя профиля диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="b216c-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b216c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b216c-140">-DefaultProfile</span></span>
<span data-ttu-id="b216c-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b216c-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b216c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b216c-142">CommonParameters</span></span>
<span data-ttu-id="b216c-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b216c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b216c-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b216c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b216c-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b216c-145">INPUTS</span></span>

### <span data-ttu-id="b216c-146">Семейств</span><span class="sxs-lookup"><span data-stu-id="b216c-146">Site</span></span>
<span data-ttu-id="b216c-147">Параметр "SourceWebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b216c-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b216c-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b216c-148">OUTPUTS</span></span>

## <span data-ttu-id="b216c-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b216c-149">NOTES</span></span>

## <span data-ttu-id="b216c-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b216c-150">RELATED LINKS</span></span>

[<span data-ttu-id="b216c-151">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b216c-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="b216c-152">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b216c-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="b216c-153">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b216c-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="b216c-154">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b216c-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="b216c-155">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b216c-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


