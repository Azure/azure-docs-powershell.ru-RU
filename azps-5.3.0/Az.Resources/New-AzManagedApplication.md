---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505226"
---
# <span data-ttu-id="71cb9-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="71cb9-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="71cb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="71cb9-103">Создает управляемое приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="71cb9-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="71cb9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="71cb9-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71cb9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="71cb9-106">С **его использованием** создается управляемое приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="71cb9-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="71cb9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="71cb9-107">EXAMPLES</span></span>

### <span data-ttu-id="71cb9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71cb9-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="71cb9-109">Эта команда создает управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="71cb9-109">This command creates a managed application</span></span>

## <span data-ttu-id="71cb9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71cb9-110">PARAMETERS</span></span>

### <span data-ttu-id="71cb9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71cb9-111">-ApiVersion</span></span>
<span data-ttu-id="71cb9-112">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71cb9-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="71cb9-113">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="71cb9-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="71cb9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cb9-114">-DefaultProfile</span></span>
<span data-ttu-id="71cb9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71cb9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71cb9-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="71cb9-116">-Kind</span></span>
<span data-ttu-id="71cb9-117">Тип управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="71cb9-117">The managed application kind.</span></span>
<span data-ttu-id="71cb9-118">Один из marketplace или servicecatalog</span><span class="sxs-lookup"><span data-stu-id="71cb9-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cb9-119">-Location</span><span class="sxs-lookup"><span data-stu-id="71cb9-119">-Location</span></span>
<span data-ttu-id="71cb9-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="71cb9-120">The resource location.</span></span>

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

### <span data-ttu-id="71cb9-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="71cb9-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="71cb9-122">Имя группы управляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71cb9-122">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71cb9-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71cb9-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="71cb9-124">Имя группы управляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71cb9-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71cb9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="71cb9-125">-Name</span></span>
<span data-ttu-id="71cb9-126">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="71cb9-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71cb9-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="71cb9-127">-Parameter</span></span>
<span data-ttu-id="71cb9-128">Строка параметров в формате JSON для управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="71cb9-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="71cb9-129">Это может быть путь к имени файла или URI, содержащий параметры, или параметры в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="71cb9-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71cb9-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="71cb9-130">-Plan</span></span>
<span data-ttu-id="71cb9-131">Hash table which represents managed application plan properties.</span><span class="sxs-lookup"><span data-stu-id="71cb9-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cb9-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="71cb9-132">-Pre</span></span>
<span data-ttu-id="71cb9-133">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="71cb9-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="71cb9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71cb9-134">-ResourceGroupName</span></span>
<span data-ttu-id="71cb9-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71cb9-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71cb9-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="71cb9-136">-Tag</span></span>
<span data-ttu-id="71cb9-137">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="71cb9-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71cb9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71cb9-138">-Confirm</span></span>
<span data-ttu-id="71cb9-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71cb9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71cb9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71cb9-140">-WhatIf</span></span>
<span data-ttu-id="71cb9-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71cb9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71cb9-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="71cb9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71cb9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cb9-143">CommonParameters</span></span>
<span data-ttu-id="71cb9-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71cb9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cb9-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71cb9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cb9-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71cb9-146">INPUTS</span></span>

### <span data-ttu-id="71cb9-147">System.String</span><span class="sxs-lookup"><span data-stu-id="71cb9-147">System.String</span></span>

### <span data-ttu-id="71cb9-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="71cb9-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="71cb9-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="71cb9-149">OUTPUTS</span></span>

### <span data-ttu-id="71cb9-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="71cb9-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="71cb9-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="71cb9-151">NOTES</span></span>

## <span data-ttu-id="71cb9-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71cb9-152">RELATED LINKS</span></span>
