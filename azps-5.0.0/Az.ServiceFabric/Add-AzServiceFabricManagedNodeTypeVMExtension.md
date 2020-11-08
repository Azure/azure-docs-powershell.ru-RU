---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249799"
---
# <span data-ttu-id="9a8ad-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="9a8ad-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="9a8ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8ad-103">Добавьте расширение VM к типу узла.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="9a8ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a8ad-104">SYNTAX</span></span>

### <span data-ttu-id="9a8ad-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a8ad-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a8ad-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9a8ad-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a8ad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a8ad-107">DESCRIPTION</span></span>
<span data-ttu-id="9a8ad-108">Добавьте расширение VM к типу узла.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-108">Add vm extension to the node type.</span></span> <span data-ttu-id="9a8ad-109">Это приведет к добавлению расширения в ресурс "Настройка underliying виртуальных машин".</span><span class="sxs-lookup"><span data-stu-id="9a8ad-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="9a8ad-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a8ad-110">EXAMPLES</span></span>

### <span data-ttu-id="9a8ad-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a8ad-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="9a8ad-112">Эта команда добавляет расширение к типу узла.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="9a8ad-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9a8ad-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="9a8ad-114">Эта команда добавляет расширение с параметрами и защищенными параметрами в тип узла.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="9a8ad-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9a8ad-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="9a8ad-116">Эта команда добавляет расширение к типу узла с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="9a8ad-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a8ad-117">PARAMETERS</span></span>

### <span data-ttu-id="9a8ad-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a8ad-118">-AsJob</span></span>
<span data-ttu-id="9a8ad-119">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9a8ad-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9a8ad-121">Указывает, должно ли расширение использовать более новую вспомогательную версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="9a8ad-122">Однако после развертывания расширение не будет обновлять дополнительные версии, если только повторно не развернуто, даже если для этого свойства задано значение true.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-123">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="9a8ad-123">-ClusterName</span></span>
<span data-ttu-id="9a8ad-124">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8ad-125">-DefaultProfile</span></span>
<span data-ttu-id="9a8ad-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="9a8ad-127">-ForceUpdateTag</span></span>
<span data-ttu-id="9a8ad-128">Если задано значение, которое отличается от предыдущего значения, обработчик расширений будет принудительно обновляться даже в том случае, если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a8ad-129">-InputObject</span></span>
<span data-ttu-id="9a8ad-130">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="9a8ad-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a8ad-131">-Name</span></span>
<span data-ttu-id="9a8ad-132">имя расширения.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="9a8ad-133">-NodeTypeName</span></span>
<span data-ttu-id="9a8ad-134">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="9a8ad-135">-ProtectedSetting</span></span>
<span data-ttu-id="9a8ad-136">Расширение может содержать либо protectedSettings, либо protectedSettingsFromKeyVault, или вообще не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="9a8ad-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="9a8ad-138">Коллекция имен расширений, после которых необходимо подготовить это расширение.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9a8ad-139">-Publisher</span></span>
<span data-ttu-id="9a8ad-140">Имя издателя обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="9a8ad-141">Это может использовать командлет Get-AzVMImagePublisher для получения издателя.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a8ad-142">-ResourceGroupName</span></span>
<span data-ttu-id="9a8ad-143">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-144">-Параметр</span><span class="sxs-lookup"><span data-stu-id="9a8ad-144">-Setting</span></span>
<span data-ttu-id="9a8ad-145">Отформатированные общедоступные параметры JSON для расширения.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-146">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="9a8ad-146">-Type</span></span>
<span data-ttu-id="9a8ad-147">Указывает тип расширения; Пример: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="9a8ad-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="9a8ad-148">Вы можете использовать командлет Get-AzVMExtensionImageType, чтобы получить тип расширения.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9a8ad-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="9a8ad-150">Указывает версию обработчика сценария.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a8ad-151">-Confirm</span></span>
<span data-ttu-id="9a8ad-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a8ad-153">-WhatIf</span></span>
<span data-ttu-id="9a8ad-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a8ad-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8ad-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8ad-156">CommonParameters</span></span>
<span data-ttu-id="9a8ad-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a8ad-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8ad-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a8ad-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8ad-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a8ad-159">INPUTS</span></span>

### <span data-ttu-id="9a8ad-160">System. String</span><span class="sxs-lookup"><span data-stu-id="9a8ad-160">System.String</span></span>

### <span data-ttu-id="9a8ad-161">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="9a8ad-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="9a8ad-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a8ad-162">OUTPUTS</span></span>

### <span data-ttu-id="9a8ad-163">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="9a8ad-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="9a8ad-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a8ad-164">NOTES</span></span>

## <span data-ttu-id="9a8ad-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a8ad-165">RELATED LINKS</span></span>
