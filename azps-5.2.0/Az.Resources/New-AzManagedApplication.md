---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403860"
---
# <span data-ttu-id="56909-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="56909-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="56909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56909-102">SYNOPSIS</span></span>
<span data-ttu-id="56909-103">Создает управляемое приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="56909-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="56909-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56909-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56909-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56909-105">DESCRIPTION</span></span>
<span data-ttu-id="56909-106">С **его использованием** создается управляемое приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="56909-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="56909-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56909-107">EXAMPLES</span></span>

### <span data-ttu-id="56909-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56909-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="56909-109">Эта команда создает управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="56909-109">This command creates a managed application</span></span>

## <span data-ttu-id="56909-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56909-110">PARAMETERS</span></span>

### <span data-ttu-id="56909-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="56909-111">-ApiVersion</span></span>
<span data-ttu-id="56909-112">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56909-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="56909-113">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="56909-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="56909-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56909-114">-DefaultProfile</span></span>
<span data-ttu-id="56909-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56909-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56909-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="56909-116">-Kind</span></span>
<span data-ttu-id="56909-117">Тип управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="56909-117">The managed application kind.</span></span>
<span data-ttu-id="56909-118">Один из marketplace или servicecatalog</span><span class="sxs-lookup"><span data-stu-id="56909-118">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="56909-119">-Location</span><span class="sxs-lookup"><span data-stu-id="56909-119">-Location</span></span>
<span data-ttu-id="56909-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="56909-120">The resource location.</span></span>

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

### <span data-ttu-id="56909-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="56909-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="56909-122">Имя группы управляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56909-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="56909-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56909-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="56909-124">Имя группы управляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56909-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="56909-125">-Name</span><span class="sxs-lookup"><span data-stu-id="56909-125">-Name</span></span>
<span data-ttu-id="56909-126">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="56909-126">The managed application name.</span></span>

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

### <span data-ttu-id="56909-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="56909-127">-Parameter</span></span>
<span data-ttu-id="56909-128">Строка параметров в формате JSON для управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="56909-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="56909-129">Это может быть путь к имени файла или URI, содержащий параметры, или параметры в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="56909-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="56909-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="56909-130">-Plan</span></span>
<span data-ttu-id="56909-131">Hash table which represents managed application plan properties.</span><span class="sxs-lookup"><span data-stu-id="56909-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="56909-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="56909-132">-Pre</span></span>
<span data-ttu-id="56909-133">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="56909-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="56909-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56909-134">-ResourceGroupName</span></span>
<span data-ttu-id="56909-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56909-135">The resource group name.</span></span>

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

### <span data-ttu-id="56909-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="56909-136">-Tag</span></span>
<span data-ttu-id="56909-137">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="56909-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="56909-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56909-138">-Confirm</span></span>
<span data-ttu-id="56909-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="56909-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56909-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56909-140">-WhatIf</span></span>
<span data-ttu-id="56909-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56909-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56909-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56909-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56909-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56909-143">CommonParameters</span></span>
<span data-ttu-id="56909-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56909-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56909-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56909-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56909-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56909-146">INPUTS</span></span>

### <span data-ttu-id="56909-147">System.String</span><span class="sxs-lookup"><span data-stu-id="56909-147">System.String</span></span>

### <span data-ttu-id="56909-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="56909-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="56909-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56909-149">OUTPUTS</span></span>

### <span data-ttu-id="56909-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="56909-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="56909-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56909-151">NOTES</span></span>

## <span data-ttu-id="56909-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56909-152">RELATED LINKS</span></span>
