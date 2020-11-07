---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: 2c489a0d041e982b6a870102db73268b7abe5392
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729119"
---
# <span data-ttu-id="dd505-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="dd505-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="dd505-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd505-102">SYNOPSIS</span></span>
<span data-ttu-id="dd505-103">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="dd505-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="dd505-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd505-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd505-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd505-105">DESCRIPTION</span></span>
<span data-ttu-id="dd505-106">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="dd505-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="dd505-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd505-107">EXAMPLES</span></span>

### <span data-ttu-id="dd505-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd505-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="dd505-109">Эта команда добавит новый NodeType "N2" с емкостью 5, а имя администратора ВМ — "adminName".</span><span class="sxs-lookup"><span data-stu-id="dd505-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="dd505-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd505-110">PARAMETERS</span></span>

### <span data-ttu-id="dd505-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="dd505-111">-Capacity</span></span>
<span data-ttu-id="dd505-112">Емкости</span><span class="sxs-lookup"><span data-stu-id="dd505-112">Capacity</span></span>

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

### <span data-ttu-id="dd505-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd505-113">-DefaultProfile</span></span>
<span data-ttu-id="dd505-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd505-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd505-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="dd505-115">-DurabilityLevel</span></span>
<span data-ttu-id="dd505-116">Укажите уровень устойчивости для NodeType.</span><span class="sxs-lookup"><span data-stu-id="dd505-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="dd505-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd505-117">-Name</span></span>
<span data-ttu-id="dd505-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="dd505-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="dd505-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="dd505-119">-NodeType</span></span>
<span data-ttu-id="dd505-120">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="dd505-120">The node type name.</span></span>

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

### <span data-ttu-id="dd505-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd505-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd505-122">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd505-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="dd505-123">Уровень</span><span class="sxs-lookup"><span data-stu-id="dd505-123">-Tier</span></span>
<span data-ttu-id="dd505-124">Уровень SKU ВМ.</span><span class="sxs-lookup"><span data-stu-id="dd505-124">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="dd505-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="dd505-125">-VmPassword</span></span>
<span data-ttu-id="dd505-126">Пароль для входа на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="dd505-126">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="dd505-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="dd505-127">-VmSku</span></span>
<span data-ttu-id="dd505-128">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="dd505-128">The sku name.</span></span>

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

### <span data-ttu-id="dd505-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="dd505-129">-VmUserName</span></span>
<span data-ttu-id="dd505-130">Имя пользователя для входа в VM.</span><span class="sxs-lookup"><span data-stu-id="dd505-130">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="dd505-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd505-131">-Confirm</span></span>
<span data-ttu-id="dd505-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd505-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd505-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd505-133">-WhatIf</span></span>
<span data-ttu-id="dd505-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd505-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd505-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd505-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd505-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd505-136">CommonParameters</span></span>
<span data-ttu-id="dd505-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd505-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd505-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd505-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd505-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd505-139">INPUTS</span></span>

### <span data-ttu-id="dd505-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dd505-140">System.String</span></span>

### <span data-ttu-id="dd505-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dd505-141">System.Int32</span></span>

### <span data-ttu-id="dd505-142">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="dd505-142">System.Security.SecureString</span></span>

### <span data-ttu-id="dd505-143">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="dd505-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="dd505-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd505-144">OUTPUTS</span></span>

### <span data-ttu-id="dd505-145">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="dd505-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="dd505-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd505-146">NOTES</span></span>

## <span data-ttu-id="dd505-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd505-147">RELATED LINKS</span></span>
