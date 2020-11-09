---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312824"
---
# <span data-ttu-id="0dc75-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="0dc75-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="0dc75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0dc75-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc75-103">Создает новую рабочую область.</span><span class="sxs-lookup"><span data-stu-id="0dc75-103">Creates a new workspace.</span></span>

## <span data-ttu-id="0dc75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0dc75-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0dc75-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0dc75-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc75-106">Создает новую рабочую область.</span><span class="sxs-lookup"><span data-stu-id="0dc75-106">Creates a new workspace.</span></span>

## <span data-ttu-id="0dc75-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0dc75-107">EXAMPLES</span></span>

### <span data-ttu-id="0dc75-108">Пример 1: создание рабочей области для кирпичей</span><span class="sxs-lookup"><span data-stu-id="0dc75-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="0dc75-109">Эта команда создает рабочую область кирпичей.</span><span class="sxs-lookup"><span data-stu-id="0dc75-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="0dc75-110">Пример 2: создание рабочей области "кирпичи" с настроенной виртуальной сетью</span><span class="sxs-lookup"><span data-stu-id="0dc75-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="0dc75-111">Эта команда создает рабочую область кирпичей с настроенной виртуальной сетью в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0dc75-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="0dc75-112">Пример 3: создание рабочей области данных с включенным шифрованием</span><span class="sxs-lookup"><span data-stu-id="0dc75-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="0dc75-113">Эта команда создает рабочую область модуля данных и задает ее для подготовки к шифрованию.</span><span class="sxs-lookup"><span data-stu-id="0dc75-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="0dc75-114">Дополнительные параметры шифрования можно найти в примерах Update-AzDatabricksWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0dc75-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="0dc75-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0dc75-115">PARAMETERS</span></span>

### <span data-ttu-id="0dc75-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dc75-116">-AsJob</span></span>
<span data-ttu-id="0dc75-117">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0dc75-117">Run the command as a job</span></span>

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

### <span data-ttu-id="0dc75-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc75-118">-DefaultProfile</span></span>
<span data-ttu-id="0dc75-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc75-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-120">-Location</span><span class="sxs-lookup"><span data-stu-id="0dc75-120">-Location</span></span>
<span data-ttu-id="0dc75-121">Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="0dc75-121">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc75-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="0dc75-123">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0dc75-123">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0dc75-124">-Name</span></span>
<span data-ttu-id="0dc75-125">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0dc75-125">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-126">-Wait</span><span class="sxs-lookup"><span data-stu-id="0dc75-126">-NoWait</span></span>
<span data-ttu-id="0dc75-127">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="0dc75-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0dc75-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="0dc75-128">-PrepareEncryption</span></span>
<span data-ttu-id="0dc75-129">Подготовьте рабочую область к шифрованию.</span><span class="sxs-lookup"><span data-stu-id="0dc75-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="0dc75-130">Включает управляемое удостоверение для управляемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0dc75-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="0dc75-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="0dc75-131">-PrivateSubnetName</span></span>
<span data-ttu-id="0dc75-132">Имя частной подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0dc75-132">The name of the Private Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="0dc75-133">-PublicSubnetName</span></span>
<span data-ttu-id="0dc75-134">Имя общедоступной подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0dc75-134">The name of a Public Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="0dc75-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="0dc75-136">Логическое значение, указывающее, будет ли включена корневая файловая система DBFS с дополнительным уровнем шифрования с управляемыми ключами платформы для данных на других платформах.</span><span class="sxs-lookup"><span data-stu-id="0dc75-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="0dc75-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc75-137">-ResourceGroupName</span></span>
<span data-ttu-id="0dc75-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0dc75-138">The name of the resource group.</span></span>
<span data-ttu-id="0dc75-139">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="0dc75-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="0dc75-140">-Sku</span></span>
<span data-ttu-id="0dc75-141">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="0dc75-141">The SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0dc75-142">-SubscriptionId</span></span>
<span data-ttu-id="0dc75-143">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0dc75-143">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="0dc75-144">-Tag</span></span>
<span data-ttu-id="0dc75-145">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0dc75-145">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0dc75-146">-VirtualNetworkId</span></span>
<span data-ttu-id="0dc75-147">ИДЕНТИФИКАТОР виртуальной сети, в которой должен быть создан этот кластер модуля данных.</span><span class="sxs-lookup"><span data-stu-id="0dc75-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc75-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dc75-148">-Confirm</span></span>
<span data-ttu-id="0dc75-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0dc75-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dc75-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc75-150">-WhatIf</span></span>
<span data-ttu-id="0dc75-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0dc75-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dc75-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0dc75-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dc75-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc75-153">CommonParameters</span></span>
<span data-ttu-id="0dc75-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0dc75-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc75-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0dc75-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc75-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0dc75-156">INPUTS</span></span>

## <span data-ttu-id="0dc75-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0dc75-157">OUTPUTS</span></span>

### <span data-ttu-id="0dc75-158">Microsoft. Azure. PowerShell. командлеты. кирпичи. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="0dc75-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="0dc75-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="0dc75-159">NOTES</span></span>

<span data-ttu-id="0dc75-160">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0dc75-160">ALIASES</span></span>

## <span data-ttu-id="0dc75-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0dc75-161">RELATED LINKS</span></span>

