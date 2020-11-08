---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: bf66b65eb54c8ed0a7f52bc3871fd80567513f59
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074310"
---
# <span data-ttu-id="0c21d-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0c21d-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="0c21d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c21d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c21d-103">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="0c21d-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="0c21d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c21d-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c21d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c21d-105">DESCRIPTION</span></span>
<span data-ttu-id="0c21d-106">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="0c21d-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="0c21d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c21d-107">EXAMPLES</span></span>

### <span data-ttu-id="0c21d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0c21d-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="0c21d-109">Эта команда добавит новый NodeType "N2" с емкостью 5, а имя администратора ВМ — "adminName".</span><span class="sxs-lookup"><span data-stu-id="0c21d-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="0c21d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c21d-110">PARAMETERS</span></span>

### <span data-ttu-id="0c21d-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="0c21d-111">-Capacity</span></span>
<span data-ttu-id="0c21d-112">Емкости</span><span class="sxs-lookup"><span data-stu-id="0c21d-112">Capacity</span></span>

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

### <span data-ttu-id="0c21d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c21d-113">-DefaultProfile</span></span>
<span data-ttu-id="0c21d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c21d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c21d-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="0c21d-115">-DurabilityLevel</span></span>
<span data-ttu-id="0c21d-116">Укажите уровень устойчивости для NodeType.</span><span class="sxs-lookup"><span data-stu-id="0c21d-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="0c21d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0c21d-117">-Name</span></span>
<span data-ttu-id="0c21d-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="0c21d-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="0c21d-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0c21d-119">-NodeType</span></span>
<span data-ttu-id="0c21d-120">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="0c21d-120">The node type name</span></span>

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

### <span data-ttu-id="0c21d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c21d-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c21d-122">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c21d-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0c21d-123">Уровень</span><span class="sxs-lookup"><span data-stu-id="0c21d-123">-Tier</span></span>
<span data-ttu-id="0c21d-124">Уровень SKU виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="0c21d-124">Vm Sku Tier</span></span>

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

### <span data-ttu-id="0c21d-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="0c21d-125">-VmPassword</span></span>
<span data-ttu-id="0c21d-126">Пароль для входа в виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="0c21d-126">The password for login to the Vm</span></span>

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

### <span data-ttu-id="0c21d-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="0c21d-127">-VmSku</span></span>
<span data-ttu-id="0c21d-128">Имя SKU</span><span class="sxs-lookup"><span data-stu-id="0c21d-128">The sku name</span></span>

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

### <span data-ttu-id="0c21d-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="0c21d-129">-VmUserName</span></span>
<span data-ttu-id="0c21d-130">Имя пользователя для входа в VM</span><span class="sxs-lookup"><span data-stu-id="0c21d-130">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="0c21d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c21d-131">-Confirm</span></span>
<span data-ttu-id="0c21d-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0c21d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c21d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c21d-133">-WhatIf</span></span>
<span data-ttu-id="0c21d-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0c21d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c21d-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c21d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c21d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c21d-136">CommonParameters</span></span>
<span data-ttu-id="0c21d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c21d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c21d-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c21d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c21d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c21d-139">INPUTS</span></span>

### <span data-ttu-id="0c21d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0c21d-140">System.String</span></span>

### <span data-ttu-id="0c21d-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0c21d-141">System.Int32</span></span>

### <span data-ttu-id="0c21d-142">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0c21d-142">System.Security.SecureString</span></span>

### <span data-ttu-id="0c21d-143">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="0c21d-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="0c21d-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c21d-144">OUTPUTS</span></span>

### <span data-ttu-id="0c21d-145">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0c21d-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0c21d-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c21d-146">NOTES</span></span>

## <span data-ttu-id="0c21d-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c21d-147">RELATED LINKS</span></span>
