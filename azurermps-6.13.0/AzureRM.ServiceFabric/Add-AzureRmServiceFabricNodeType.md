---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 573dd2f4681ae140fbe98de5d9a7e9df4e2dc764
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562599"
---
# <span data-ttu-id="1cef9-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="1cef9-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="1cef9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1cef9-102">SYNOPSIS</span></span>
<span data-ttu-id="1cef9-103">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="1cef9-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cef9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1cef9-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cef9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cef9-105">DESCRIPTION</span></span>
<span data-ttu-id="1cef9-106">Добавление нового типа узла в существующий кластер.</span><span class="sxs-lookup"><span data-stu-id="1cef9-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="1cef9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1cef9-107">EXAMPLES</span></span>

### <span data-ttu-id="1cef9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1cef9-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="1cef9-109">Эта команда добавит новый NodeType "N2" с емкостью 5, а имя администратора ВМ — "adminName".</span><span class="sxs-lookup"><span data-stu-id="1cef9-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="1cef9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1cef9-110">PARAMETERS</span></span>

### <span data-ttu-id="1cef9-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="1cef9-111">-Capacity</span></span>
<span data-ttu-id="1cef9-112">Емкости</span><span class="sxs-lookup"><span data-stu-id="1cef9-112">Capacity</span></span>

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

### <span data-ttu-id="1cef9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cef9-113">-DefaultProfile</span></span>
<span data-ttu-id="1cef9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cef9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cef9-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="1cef9-115">-DurabilityLevel</span></span>
<span data-ttu-id="1cef9-116">Укажите уровень устойчивости для NodeType.</span><span class="sxs-lookup"><span data-stu-id="1cef9-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="1cef9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1cef9-117">-Name</span></span>
<span data-ttu-id="1cef9-118">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="1cef9-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1cef9-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="1cef9-119">-NodeType</span></span>
<span data-ttu-id="1cef9-120">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="1cef9-120">The node type name.</span></span>

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

### <span data-ttu-id="1cef9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cef9-121">-ResourceGroupName</span></span>
<span data-ttu-id="1cef9-122">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1cef9-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1cef9-123">Уровень</span><span class="sxs-lookup"><span data-stu-id="1cef9-123">-Tier</span></span>
<span data-ttu-id="1cef9-124">Уровень SKU ВМ.</span><span class="sxs-lookup"><span data-stu-id="1cef9-124">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="1cef9-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="1cef9-125">-VmPassword</span></span>
<span data-ttu-id="1cef9-126">Пароль для входа на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="1cef9-126">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="1cef9-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="1cef9-127">-VmSku</span></span>
<span data-ttu-id="1cef9-128">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="1cef9-128">The sku name.</span></span>

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

### <span data-ttu-id="1cef9-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="1cef9-129">-VmUserName</span></span>
<span data-ttu-id="1cef9-130">Имя пользователя для входа в VM.</span><span class="sxs-lookup"><span data-stu-id="1cef9-130">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="1cef9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cef9-131">-Confirm</span></span>
<span data-ttu-id="1cef9-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1cef9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cef9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cef9-133">-WhatIf</span></span>
<span data-ttu-id="1cef9-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1cef9-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cef9-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1cef9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cef9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cef9-136">CommonParameters</span></span>
<span data-ttu-id="1cef9-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1cef9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cef9-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cef9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cef9-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1cef9-139">INPUTS</span></span>

### <span data-ttu-id="1cef9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1cef9-140">System.String</span></span>
<span data-ttu-id="1cef9-141">Параметры: NodeType (ByValue), Tier (ByValue), VmSku (ByValue), VmUserName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1cef9-141">Parameters: NodeType (ByValue), Tier (ByValue), VmSku (ByValue), VmUserName (ByValue)</span></span>

### <span data-ttu-id="1cef9-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1cef9-142">System.Int32</span></span>
<span data-ttu-id="1cef9-143">Параметры: Capacity (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1cef9-143">Parameters: Capacity (ByValue)</span></span>

### <span data-ttu-id="1cef9-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1cef9-144">System.Security.SecureString</span></span>
<span data-ttu-id="1cef9-145">Параметры: VmPassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1cef9-145">Parameters: VmPassword (ByValue)</span></span>

### <span data-ttu-id="1cef9-146">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="1cef9-146">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="1cef9-147">Параметры: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1cef9-147">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="1cef9-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cef9-148">OUTPUTS</span></span>

### <span data-ttu-id="1cef9-149">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="1cef9-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1cef9-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="1cef9-150">NOTES</span></span>

## <span data-ttu-id="1cef9-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cef9-151">RELATED LINKS</span></span>
