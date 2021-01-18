---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: de512f636b0a326029981e199b13926a9fc5824a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517290"
---
# <span data-ttu-id="fee46-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="fee46-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="fee46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee46-102">SYNOPSIS</span></span>
<span data-ttu-id="fee46-103">Добавьте новый тип узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="fee46-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="fee46-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fee46-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee46-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fee46-105">DESCRIPTION</span></span>
<span data-ttu-id="fee46-106">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="fee46-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="fee46-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fee46-107">EXAMPLES</span></span>

### <span data-ttu-id="fee46-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fee46-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="fee46-109">Эта команда добавит новый NodeType "n2" емкостью 5 человек, а имя администратора vm будет "adminName".</span><span class="sxs-lookup"><span data-stu-id="fee46-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="fee46-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fee46-110">PARAMETERS</span></span>

### <span data-ttu-id="fee46-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="fee46-111">-Capacity</span></span>
<span data-ttu-id="fee46-112">Мощность</span><span class="sxs-lookup"><span data-stu-id="fee46-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee46-113">-DefaultProfile</span></span>
<span data-ttu-id="fee46-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fee46-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee46-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="fee46-115">-DurabilityLevel</span></span>
<span data-ttu-id="fee46-116">Укажите уровень надежности NodeType.</span><span class="sxs-lookup"><span data-stu-id="fee46-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases:
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee46-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fee46-117">-Name</span></span>
<span data-ttu-id="fee46-118">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="fee46-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee46-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="fee46-119">-NodeType</span></span>
<span data-ttu-id="fee46-120">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="fee46-120">The node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee46-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee46-121">-ResourceGroupName</span></span>
<span data-ttu-id="fee46-122">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fee46-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee46-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="fee46-123">-Tier</span></span>
<span data-ttu-id="fee46-124">Уровень SKU VM</span><span class="sxs-lookup"><span data-stu-id="fee46-124">Vm Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee46-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="fee46-125">-VmPassword</span></span>
<span data-ttu-id="fee46-126">Пароль для входа в VM</span><span class="sxs-lookup"><span data-stu-id="fee46-126">The password for login to the Vm</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee46-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="fee46-127">-VmSku</span></span>
<span data-ttu-id="fee46-128">Имя SKU</span><span class="sxs-lookup"><span data-stu-id="fee46-128">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee46-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="fee46-129">-VmUserName</span></span>
<span data-ttu-id="fee46-130">Имя пользователя для ведения журнала на VM</span><span class="sxs-lookup"><span data-stu-id="fee46-130">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fee46-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fee46-131">-Confirm</span></span>
<span data-ttu-id="fee46-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee46-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee46-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee46-133">-WhatIf</span></span>
<span data-ttu-id="fee46-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee46-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee46-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fee46-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee46-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee46-136">CommonParameters</span></span>
<span data-ttu-id="fee46-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee46-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee46-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fee46-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee46-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fee46-139">INPUTS</span></span>

### <span data-ttu-id="fee46-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fee46-140">System.String</span></span>

### <span data-ttu-id="fee46-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fee46-141">System.Int32</span></span>

### <span data-ttu-id="fee46-142">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="fee46-142">System.Security.SecureString</span></span>

### <span data-ttu-id="fee46-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="fee46-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="fee46-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fee46-144">OUTPUTS</span></span>

### <span data-ttu-id="fee46-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="fee46-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fee46-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fee46-146">NOTES</span></span>

## <span data-ttu-id="fee46-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fee46-147">RELATED LINKS</span></span>
