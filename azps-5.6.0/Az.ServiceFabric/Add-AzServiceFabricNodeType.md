---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: aef628c121fa01cf07b0c70764b7d34ac10f259a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961560"
---
# <span data-ttu-id="68b92-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="68b92-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="68b92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68b92-102">SYNOPSIS</span></span>
<span data-ttu-id="68b92-103">Добавьте новый тип узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="68b92-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="68b92-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="68b92-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68b92-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68b92-105">DESCRIPTION</span></span>
<span data-ttu-id="68b92-106">Добавьте новый тип узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="68b92-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="68b92-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="68b92-107">EXAMPLES</span></span>

### <span data-ttu-id="68b92-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="68b92-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="68b92-109">Эта команда добавит новый NodeType "n2" емкостью 5 м, а имя администратора vm будет "adminName".</span><span class="sxs-lookup"><span data-stu-id="68b92-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="68b92-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68b92-110">PARAMETERS</span></span>

### <span data-ttu-id="68b92-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="68b92-111">-Capacity</span></span>
<span data-ttu-id="68b92-112">Мощность</span><span class="sxs-lookup"><span data-stu-id="68b92-112">Capacity</span></span>

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

### <span data-ttu-id="68b92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b92-113">-DefaultProfile</span></span>
<span data-ttu-id="68b92-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68b92-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b92-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="68b92-115">-DurabilityLevel</span></span>
<span data-ttu-id="68b92-116">Укажите уровень надежности NodeType.</span><span class="sxs-lookup"><span data-stu-id="68b92-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="68b92-117">-Name</span><span class="sxs-lookup"><span data-stu-id="68b92-117">-Name</span></span>
<span data-ttu-id="68b92-118">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="68b92-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="68b92-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="68b92-119">-NodeType</span></span>
<span data-ttu-id="68b92-120">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="68b92-120">The node type name</span></span>

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

### <span data-ttu-id="68b92-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b92-121">-ResourceGroupName</span></span>
<span data-ttu-id="68b92-122">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68b92-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="68b92-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="68b92-123">-Tier</span></span>
<span data-ttu-id="68b92-124">Уровень SKU VM</span><span class="sxs-lookup"><span data-stu-id="68b92-124">Vm Sku Tier</span></span>

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

### <span data-ttu-id="68b92-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="68b92-125">-VmPassword</span></span>
<span data-ttu-id="68b92-126">Пароль для входа в VM</span><span class="sxs-lookup"><span data-stu-id="68b92-126">The password for login to the Vm</span></span>

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

### <span data-ttu-id="68b92-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="68b92-127">-VmSku</span></span>
<span data-ttu-id="68b92-128">Имя SKU</span><span class="sxs-lookup"><span data-stu-id="68b92-128">The sku name</span></span>

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

### <span data-ttu-id="68b92-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="68b92-129">-VmUserName</span></span>
<span data-ttu-id="68b92-130">Имя пользователя для ведения журнала на VM</span><span class="sxs-lookup"><span data-stu-id="68b92-130">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="68b92-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68b92-131">-Confirm</span></span>
<span data-ttu-id="68b92-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68b92-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68b92-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b92-133">-WhatIf</span></span>
<span data-ttu-id="68b92-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68b92-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68b92-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="68b92-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68b92-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b92-136">CommonParameters</span></span>
<span data-ttu-id="68b92-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68b92-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b92-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68b92-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b92-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68b92-139">INPUTS</span></span>

### <span data-ttu-id="68b92-140">System.String</span><span class="sxs-lookup"><span data-stu-id="68b92-140">System.String</span></span>

### <span data-ttu-id="68b92-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="68b92-141">System.Int32</span></span>

### <span data-ttu-id="68b92-142">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="68b92-142">System.Security.SecureString</span></span>

### <span data-ttu-id="68b92-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="68b92-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="68b92-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68b92-144">OUTPUTS</span></span>

### <span data-ttu-id="68b92-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="68b92-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="68b92-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="68b92-146">NOTES</span></span>

## <span data-ttu-id="68b92-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68b92-147">RELATED LINKS</span></span>
