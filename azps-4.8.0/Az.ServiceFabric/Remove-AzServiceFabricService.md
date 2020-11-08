---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1475296638cec105713eaa390bcce6552e5502ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078724"
---
# <span data-ttu-id="4a007-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4a007-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="4a007-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a007-102">SYNOPSIS</span></span>
<span data-ttu-id="4a007-103">Удаление службы из кластера.</span><span class="sxs-lookup"><span data-stu-id="4a007-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="4a007-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a007-104">SYNTAX</span></span>

### <span data-ttu-id="4a007-105">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a007-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a007-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a007-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a007-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a007-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a007-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a007-108">DESCRIPTION</span></span>
<span data-ttu-id="4a007-109">Этот командлет удаляет службу из формы кластера.</span><span class="sxs-lookup"><span data-stu-id="4a007-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="4a007-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a007-110">EXAMPLES</span></span>

### <span data-ttu-id="4a007-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a007-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="4a007-112">В этом примере будет удалена служба "testApp ~ testService1".</span><span class="sxs-lookup"><span data-stu-id="4a007-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="4a007-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a007-113">PARAMETERS</span></span>

### <span data-ttu-id="4a007-114">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="4a007-114">-ApplicationName</span></span>
<span data-ttu-id="4a007-115">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="4a007-115">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a007-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="4a007-116">-ClusterName</span></span>
<span data-ttu-id="4a007-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="4a007-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4a007-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a007-118">-DefaultProfile</span></span>
<span data-ttu-id="4a007-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a007-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a007-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4a007-120">-Force</span></span>
<span data-ttu-id="4a007-121">Удалить без запроса.</span><span class="sxs-lookup"><span data-stu-id="4a007-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="4a007-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a007-122">-InputObject</span></span>
<span data-ttu-id="4a007-123">Ресурс службы.</span><span class="sxs-lookup"><span data-stu-id="4a007-123">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a007-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a007-124">-Name</span></span>
<span data-ttu-id="4a007-125">Укажите имя службы.</span><span class="sxs-lookup"><span data-stu-id="4a007-125">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a007-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a007-126">-PassThru</span></span>
<span data-ttu-id="4a007-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="4a007-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4a007-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a007-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a007-129">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a007-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4a007-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a007-130">-ResourceId</span></span>
<span data-ttu-id="4a007-131">ResourceId (ИД) для службы.</span><span class="sxs-lookup"><span data-stu-id="4a007-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="4a007-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a007-132">-Confirm</span></span>
<span data-ttu-id="4a007-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4a007-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a007-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a007-134">-WhatIf</span></span>
<span data-ttu-id="4a007-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4a007-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a007-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4a007-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a007-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a007-137">CommonParameters</span></span>
<span data-ttu-id="4a007-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a007-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a007-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a007-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a007-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a007-140">INPUTS</span></span>

### <span data-ttu-id="4a007-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4a007-141">System.String</span></span>

### <span data-ttu-id="4a007-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="4a007-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="4a007-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a007-143">OUTPUTS</span></span>

### <span data-ttu-id="4a007-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a007-144">System.Boolean</span></span>

## <span data-ttu-id="4a007-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a007-145">NOTES</span></span>

## <span data-ttu-id="4a007-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a007-146">RELATED LINKS</span></span>
