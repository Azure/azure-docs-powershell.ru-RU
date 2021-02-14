---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217524"
---
# <span data-ttu-id="7a66d-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="7a66d-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="7a66d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a66d-102">SYNOPSIS</span></span>
<span data-ttu-id="7a66d-103">Удалите расширение VM из типа узла.</span><span class="sxs-lookup"><span data-stu-id="7a66d-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="7a66d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a66d-104">SYNTAX</span></span>

### <span data-ttu-id="7a66d-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a66d-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a66d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7a66d-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a66d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a66d-107">DESCRIPTION</span></span>
<span data-ttu-id="7a66d-108">Удалите расширение VM из типа узла по имени.</span><span class="sxs-lookup"><span data-stu-id="7a66d-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="7a66d-109">Используйте [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) и взгляните на свойство VmExtensions, чтобы увидеть текущее расширение для типа узла.</span><span class="sxs-lookup"><span data-stu-id="7a66d-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="7a66d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a66d-110">EXAMPLES</span></span>

### <span data-ttu-id="7a66d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a66d-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="7a66d-112">Удаление расширения из типа узла по имени.</span><span class="sxs-lookup"><span data-stu-id="7a66d-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="7a66d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7a66d-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="7a66d-114">Удаление расширения из типа узла по имени с помощью перенастройки.</span><span class="sxs-lookup"><span data-stu-id="7a66d-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="7a66d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a66d-115">PARAMETERS</span></span>

### <span data-ttu-id="7a66d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a66d-116">-AsJob</span></span>
<span data-ttu-id="7a66d-117">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7a66d-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7a66d-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7a66d-118">-ClusterName</span></span>
<span data-ttu-id="7a66d-119">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="7a66d-119">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a66d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a66d-120">-DefaultProfile</span></span>
<span data-ttu-id="7a66d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a66d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a66d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a66d-122">-InputObject</span></span>
<span data-ttu-id="7a66d-123">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="7a66d-123">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a66d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7a66d-124">-Name</span></span>
<span data-ttu-id="7a66d-125">расширение.</span><span class="sxs-lookup"><span data-stu-id="7a66d-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a66d-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="7a66d-126">-NodeTypeName</span></span>
<span data-ttu-id="7a66d-127">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="7a66d-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a66d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a66d-128">-PassThru</span></span>
<span data-ttu-id="7a66d-129">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="7a66d-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7a66d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a66d-130">-ResourceGroupName</span></span>
<span data-ttu-id="7a66d-131">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a66d-131">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a66d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a66d-132">-Confirm</span></span>
<span data-ttu-id="7a66d-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a66d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a66d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a66d-134">-WhatIf</span></span>
<span data-ttu-id="7a66d-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a66d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a66d-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a66d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a66d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a66d-137">CommonParameters</span></span>
<span data-ttu-id="7a66d-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a66d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a66d-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a66d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a66d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a66d-140">INPUTS</span></span>

### <span data-ttu-id="7a66d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7a66d-141">System.String</span></span>

## <span data-ttu-id="7a66d-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a66d-142">OUTPUTS</span></span>

### <span data-ttu-id="7a66d-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="7a66d-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="7a66d-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a66d-144">NOTES</span></span>

## <span data-ttu-id="7a66d-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a66d-145">RELATED LINKS</span></span>
