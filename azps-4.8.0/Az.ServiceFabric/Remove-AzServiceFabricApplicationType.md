---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 87557a67c8cb087b8a22ecc9cdfa59a3690057dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078722"
---
# <span data-ttu-id="d1646-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d1646-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="d1646-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1646-102">SYNOPSIS</span></span>
<span data-ttu-id="d1646-103">Удаление сервисной фабрики тип приложения из кластера.</span><span class="sxs-lookup"><span data-stu-id="d1646-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="d1646-104">Это приведет к удалению всех версий типов под этим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="d1646-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="d1646-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1646-105">SYNTAX</span></span>

### <span data-ttu-id="d1646-106">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1646-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1646-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1646-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1646-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1646-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1646-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1646-109">DESCRIPTION</span></span>
<span data-ttu-id="d1646-110">Этот командлет удаляет тип приложения из кластера и удалит все версии типа для этого ресурса, но все приложения под ним должны быть удалены перед выполнением этой команды.</span><span class="sxs-lookup"><span data-stu-id="d1646-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="d1646-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1646-111">EXAMPLES</span></span>

### <span data-ttu-id="d1646-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1646-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="d1646-113">В этом примере будет удален тип приложения "testAppType" и все его версии.</span><span class="sxs-lookup"><span data-stu-id="d1646-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="d1646-114">Если у вас есть какие – либо приложения, созданные с этим типом, команда вызовет исключение.</span><span class="sxs-lookup"><span data-stu-id="d1646-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="d1646-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1646-115">PARAMETERS</span></span>

### <span data-ttu-id="d1646-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="d1646-116">-ClusterName</span></span>
<span data-ttu-id="d1646-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="d1646-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d1646-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1646-118">-DefaultProfile</span></span>
<span data-ttu-id="d1646-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1646-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1646-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d1646-120">-Force</span></span>
<span data-ttu-id="d1646-121">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="d1646-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="d1646-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1646-122">-InputObject</span></span>
<span data-ttu-id="d1646-123">Ресурс типа приложения.</span><span class="sxs-lookup"><span data-stu-id="d1646-123">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1646-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1646-124">-Name</span></span>
<span data-ttu-id="d1646-125">Укажите имя типа приложения.</span><span class="sxs-lookup"><span data-stu-id="d1646-125">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1646-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1646-126">-PassThru</span></span>
<span data-ttu-id="d1646-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="d1646-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d1646-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1646-128">-ResourceGroupName</span></span>
<span data-ttu-id="d1646-129">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1646-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d1646-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1646-130">-ResourceId</span></span>
<span data-ttu-id="d1646-131">Значение ResourceId для типа приложения.</span><span class="sxs-lookup"><span data-stu-id="d1646-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="d1646-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1646-132">-Confirm</span></span>
<span data-ttu-id="d1646-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d1646-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1646-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1646-134">-WhatIf</span></span>
<span data-ttu-id="d1646-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d1646-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1646-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1646-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1646-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1646-137">CommonParameters</span></span>
<span data-ttu-id="d1646-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1646-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1646-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1646-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1646-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1646-140">INPUTS</span></span>

### <span data-ttu-id="d1646-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d1646-141">System.String</span></span>

### <span data-ttu-id="d1646-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="d1646-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="d1646-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1646-143">OUTPUTS</span></span>

### <span data-ttu-id="d1646-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1646-144">System.Boolean</span></span>

## <span data-ttu-id="d1646-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1646-145">NOTES</span></span>

## <span data-ttu-id="d1646-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1646-146">RELATED LINKS</span></span>
