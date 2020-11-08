---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235321"
---
# <span data-ttu-id="c917e-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="c917e-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="c917e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c917e-102">SYNOPSIS</span></span>
<span data-ttu-id="c917e-103">Удалите расширение VM из типа узла.</span><span class="sxs-lookup"><span data-stu-id="c917e-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="c917e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c917e-104">SYNTAX</span></span>

### <span data-ttu-id="c917e-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c917e-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c917e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c917e-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c917e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c917e-107">DESCRIPTION</span></span>
<span data-ttu-id="c917e-108">Удалите расширение VM из типа узла по имени.</span><span class="sxs-lookup"><span data-stu-id="c917e-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="c917e-109">С помощью [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) и просмотрите свойство VmExtensions, чтобы увидеть текущее расширение типа узла.</span><span class="sxs-lookup"><span data-stu-id="c917e-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="c917e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c917e-110">EXAMPLES</span></span>

### <span data-ttu-id="c917e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c917e-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="c917e-112">Удаление расширения из типа узла по имени.</span><span class="sxs-lookup"><span data-stu-id="c917e-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="c917e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c917e-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="c917e-114">Удаление расширения из типа узла по названию с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="c917e-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="c917e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c917e-115">PARAMETERS</span></span>

### <span data-ttu-id="c917e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c917e-116">-AsJob</span></span>
<span data-ttu-id="c917e-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c917e-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c917e-118">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="c917e-118">-ClusterName</span></span>
<span data-ttu-id="c917e-119">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="c917e-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c917e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c917e-120">-DefaultProfile</span></span>
<span data-ttu-id="c917e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c917e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c917e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c917e-122">-InputObject</span></span>
<span data-ttu-id="c917e-123">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="c917e-123">Node type resource</span></span>

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

### <span data-ttu-id="c917e-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c917e-124">-Name</span></span>
<span data-ttu-id="c917e-125">имя расширения.</span><span class="sxs-lookup"><span data-stu-id="c917e-125">extension name.</span></span>

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

### <span data-ttu-id="c917e-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="c917e-126">-NodeTypeName</span></span>
<span data-ttu-id="c917e-127">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="c917e-127">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="c917e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c917e-128">-PassThru</span></span>
<span data-ttu-id="c917e-129">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="c917e-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c917e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c917e-130">-ResourceGroupName</span></span>
<span data-ttu-id="c917e-131">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c917e-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c917e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c917e-132">-Confirm</span></span>
<span data-ttu-id="c917e-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c917e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c917e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c917e-134">-WhatIf</span></span>
<span data-ttu-id="c917e-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c917e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c917e-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c917e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c917e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c917e-137">CommonParameters</span></span>
<span data-ttu-id="c917e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c917e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c917e-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c917e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c917e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c917e-140">INPUTS</span></span>

### <span data-ttu-id="c917e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c917e-141">System.String</span></span>

## <span data-ttu-id="c917e-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c917e-142">OUTPUTS</span></span>

### <span data-ttu-id="c917e-143">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="c917e-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="c917e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="c917e-144">NOTES</span></span>

## <span data-ttu-id="c917e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c917e-145">RELATED LINKS</span></span>
