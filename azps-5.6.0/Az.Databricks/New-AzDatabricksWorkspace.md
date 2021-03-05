---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: c49056da040e7259c1cbc0964335f157e00cbecd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962243"
---
# <span data-ttu-id="d10cb-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="d10cb-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="d10cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d10cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d10cb-103">Создание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d10cb-103">Creates a new workspace.</span></span>

## <span data-ttu-id="d10cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d10cb-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-EnableNoPublicIP] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d10cb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d10cb-105">DESCRIPTION</span></span>
<span data-ttu-id="d10cb-106">Создание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d10cb-106">Creates a new workspace.</span></span>

## <span data-ttu-id="d10cb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d10cb-107">EXAMPLES</span></span>

### <span data-ttu-id="d10cb-108">Пример 1. Создание рабочей области "Datab ветвей"</span><span class="sxs-lookup"><span data-stu-id="d10cb-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="d10cb-109">Эта команда создает рабочее пространство Datab ветвей.</span><span class="sxs-lookup"><span data-stu-id="d10cb-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="d10cb-110">Пример 2. Создание рабочей области Datab в настраиваемой виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d10cb-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="d10cb-111">Эта команда создает рабочее пространство Datab в группе ресурсов с настроенной виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="d10cb-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="d10cb-112">Пример 3. Создание рабочей области Datab ветвь шифрования</span><span class="sxs-lookup"><span data-stu-id="d10cb-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="d10cb-113">Эта команда создает рабочее пространство Datab ветвей и настраивает ее для подготовки к шифрованию.</span><span class="sxs-lookup"><span data-stu-id="d10cb-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="d10cb-114">Дополнительные параметры шифрования Update-AzDatabricksWorkspace примерах этой программы.</span><span class="sxs-lookup"><span data-stu-id="d10cb-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="d10cb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d10cb-115">PARAMETERS</span></span>

### <span data-ttu-id="d10cb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d10cb-116">-AsJob</span></span>
<span data-ttu-id="d10cb-117">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d10cb-117">Run the command as a job</span></span>

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

### <span data-ttu-id="d10cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10cb-118">-DefaultProfile</span></span>
<span data-ttu-id="d10cb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d10cb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d10cb-120">-EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="d10cb-120">-EnableNoPublicIP</span></span>
<span data-ttu-id="d10cb-121">Значение, которое будет использоваться для этого поля.</span><span class="sxs-lookup"><span data-stu-id="d10cb-121">The value which should be used for this field.</span></span>

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

### <span data-ttu-id="d10cb-122">-Location</span><span class="sxs-lookup"><span data-stu-id="d10cb-122">-Location</span></span>
<span data-ttu-id="d10cb-123">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="d10cb-123">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="d10cb-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d10cb-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="d10cb-125">Имя группы управляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d10cb-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="d10cb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d10cb-126">-Name</span></span>
<span data-ttu-id="d10cb-127">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d10cb-127">The name of the workspace.</span></span>

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

### <span data-ttu-id="d10cb-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d10cb-128">-NoWait</span></span>
<span data-ttu-id="d10cb-129">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="d10cb-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d10cb-130">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="d10cb-130">-PrepareEncryption</span></span>
<span data-ttu-id="d10cb-131">Подготовьте рабочее пространство для шифрования.</span><span class="sxs-lookup"><span data-stu-id="d10cb-131">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="d10cb-132">Включает управляемое удостоверение для учетной записи управляемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="d10cb-132">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="d10cb-133">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="d10cb-133">-PrivateSubnetName</span></span>
<span data-ttu-id="d10cb-134">Имя частной подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d10cb-134">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="d10cb-135">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="d10cb-135">-PublicSubnetName</span></span>
<span data-ttu-id="d10cb-136">Имя открытой подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d10cb-136">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="d10cb-137">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="d10cb-137">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="d10cb-138">Boolean indicating whether the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span><span class="sxs-lookup"><span data-stu-id="d10cb-138">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="d10cb-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d10cb-139">-ResourceGroupName</span></span>
<span data-ttu-id="d10cb-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d10cb-140">The name of the resource group.</span></span>
<span data-ttu-id="d10cb-141">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d10cb-141">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d10cb-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="d10cb-142">-Sku</span></span>
<span data-ttu-id="d10cb-143">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="d10cb-143">The SKU name.</span></span>

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

### <span data-ttu-id="d10cb-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d10cb-144">-SubscriptionId</span></span>
<span data-ttu-id="d10cb-145">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d10cb-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d10cb-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="d10cb-146">-Tag</span></span>
<span data-ttu-id="d10cb-147">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d10cb-147">Resource tags.</span></span>

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

### <span data-ttu-id="d10cb-148">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d10cb-148">-VirtualNetworkId</span></span>
<span data-ttu-id="d10cb-149">Это ИД виртуальной сети, в которой должен быть создан кластер datab в сети.</span><span class="sxs-lookup"><span data-stu-id="d10cb-149">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="d10cb-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d10cb-150">-Confirm</span></span>
<span data-ttu-id="d10cb-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d10cb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d10cb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d10cb-152">-WhatIf</span></span>
<span data-ttu-id="d10cb-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d10cb-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d10cb-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d10cb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d10cb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10cb-155">CommonParameters</span></span>
<span data-ttu-id="d10cb-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d10cb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10cb-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d10cb-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10cb-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d10cb-158">INPUTS</span></span>

## <span data-ttu-id="d10cb-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d10cb-159">OUTPUTS</span></span>

### <span data-ttu-id="d10cb-160">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="d10cb-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="d10cb-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d10cb-161">NOTES</span></span>

<span data-ttu-id="d10cb-162">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d10cb-162">ALIASES</span></span>

## <span data-ttu-id="d10cb-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d10cb-163">RELATED LINKS</span></span>

