---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: f50baca10d3079ac800b694670ce2b4c8c85fc84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066151"
---
# <span data-ttu-id="9f009-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="9f009-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="9f009-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f009-102">SYNOPSIS</span></span>
<span data-ttu-id="9f009-103">Удаление служебной фабрики версия типа приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="9f009-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="9f009-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f009-104">SYNTAX</span></span>

### <span data-ttu-id="9f009-105">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f009-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f009-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f009-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f009-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f009-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f009-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f009-108">DESCRIPTION</span></span>
<span data-ttu-id="9f009-109">Этот командлет удалит фабрику служб, версию типа приложения, из кластера.</span><span class="sxs-lookup"><span data-stu-id="9f009-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="9f009-110">Перед выполнением этой команды необходимо удалить все приложения из этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="9f009-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="9f009-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f009-111">EXAMPLES</span></span>

### <span data-ttu-id="9f009-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f009-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="9f009-113">В этом примере будет удалена версия "v1" в разделе Type "testAppType".</span><span class="sxs-lookup"><span data-stu-id="9f009-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="9f009-114">В этом ресурсе есть какое бы то ни было приложение, в результате чего команда создаст исключение.</span><span class="sxs-lookup"><span data-stu-id="9f009-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="9f009-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f009-115">PARAMETERS</span></span>

### <span data-ttu-id="9f009-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="9f009-116">-ClusterName</span></span>
<span data-ttu-id="9f009-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="9f009-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f009-118">-DefaultProfile</span></span>
<span data-ttu-id="9f009-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f009-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f009-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9f009-120">-Force</span></span>
<span data-ttu-id="9f009-121">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="9f009-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="9f009-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f009-122">-InputObject</span></span>
<span data-ttu-id="9f009-123">Ресурс версии типа приложения.</span><span class="sxs-lookup"><span data-stu-id="9f009-123">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f009-124">-Name</span></span>
<span data-ttu-id="9f009-125">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="9f009-125">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f009-126">-PassThru</span></span>
<span data-ttu-id="9f009-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="9f009-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9f009-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f009-128">-ResourceGroupName</span></span>
<span data-ttu-id="9f009-129">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f009-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f009-130">-ResourceId</span></span>
<span data-ttu-id="9f009-131">Значение ResourceId для версии типа приложения.</span><span class="sxs-lookup"><span data-stu-id="9f009-131">Arm ResourceId of the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-132">-Version</span><span class="sxs-lookup"><span data-stu-id="9f009-132">-Version</span></span>
<span data-ttu-id="9f009-133">Укажите версию типа приложения.</span><span class="sxs-lookup"><span data-stu-id="9f009-133">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f009-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f009-134">-Confirm</span></span>
<span data-ttu-id="9f009-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f009-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f009-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f009-136">-WhatIf</span></span>
<span data-ttu-id="9f009-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f009-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f009-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f009-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f009-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f009-139">CommonParameters</span></span>
<span data-ttu-id="9f009-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f009-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f009-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f009-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f009-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f009-142">INPUTS</span></span>

### <span data-ttu-id="9f009-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9f009-143">System.String</span></span>

### <span data-ttu-id="9f009-144">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="9f009-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="9f009-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f009-145">OUTPUTS</span></span>

### <span data-ttu-id="9f009-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f009-146">System.Boolean</span></span>

## <span data-ttu-id="9f009-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f009-147">NOTES</span></span>

## <span data-ttu-id="9f009-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f009-148">RELATED LINKS</span></span>
