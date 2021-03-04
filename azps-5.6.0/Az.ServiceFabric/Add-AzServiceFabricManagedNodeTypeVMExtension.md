---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: 14138dddcd4f4b2150377726d862d953c7360a31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969816"
---
# <span data-ttu-id="664d5-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="664d5-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="664d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="664d5-102">SYNOPSIS</span></span>
<span data-ttu-id="664d5-103">Добавьте расширение VM к типу узла.</span><span class="sxs-lookup"><span data-stu-id="664d5-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="664d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="664d5-104">SYNTAX</span></span>

### <span data-ttu-id="664d5-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="664d5-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="664d5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="664d5-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="664d5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="664d5-107">DESCRIPTION</span></span>
<span data-ttu-id="664d5-108">Добавьте расширение VM к типу узла.</span><span class="sxs-lookup"><span data-stu-id="664d5-108">Add vm extension to the node type.</span></span> <span data-ttu-id="664d5-109">Расширение добавит к ресурсу, на который установлен набор масштабов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="664d5-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="664d5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="664d5-110">EXAMPLES</span></span>

### <span data-ttu-id="664d5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="664d5-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="664d5-112">Эта команда добавляет расширение к типу узла.</span><span class="sxs-lookup"><span data-stu-id="664d5-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="664d5-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="664d5-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="664d5-114">Эта команда добавляет к типу узла расширение с настройками и защищенными настройками.</span><span class="sxs-lookup"><span data-stu-id="664d5-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="664d5-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="664d5-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="664d5-116">Эта команда добавляет расширение к типу узла с помощью перенастройки.</span><span class="sxs-lookup"><span data-stu-id="664d5-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="664d5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="664d5-117">PARAMETERS</span></span>

### <span data-ttu-id="664d5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="664d5-118">-AsJob</span></span>
<span data-ttu-id="664d5-119">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="664d5-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="664d5-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="664d5-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="664d5-121">Указывает, следует ли использовать в расширении более новую версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="664d5-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="664d5-122">Однако после развертывания расширение не будет обновлять дополнительные версии, если не развернуть их снова, даже если для этого свойства установлено true.</span><span class="sxs-lookup"><span data-stu-id="664d5-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="664d5-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="664d5-123">-ClusterName</span></span>
<span data-ttu-id="664d5-124">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="664d5-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="664d5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664d5-125">-DefaultProfile</span></span>
<span data-ttu-id="664d5-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="664d5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="664d5-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="664d5-127">-ForceUpdateTag</span></span>
<span data-ttu-id="664d5-128">Если значение предоставляются и отличается от предыдущего, обработник расширения будет принудительно обновляться даже в том случае, если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="664d5-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="664d5-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="664d5-129">-InputObject</span></span>
<span data-ttu-id="664d5-130">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="664d5-130">Node Type resource</span></span>

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

### <span data-ttu-id="664d5-131">-Name</span><span class="sxs-lookup"><span data-stu-id="664d5-131">-Name</span></span>
<span data-ttu-id="664d5-132">расширение.</span><span class="sxs-lookup"><span data-stu-id="664d5-132">extension name.</span></span>

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

### <span data-ttu-id="664d5-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="664d5-133">-NodeTypeName</span></span>
<span data-ttu-id="664d5-134">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="664d5-134">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="664d5-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="664d5-135">-ProtectedSetting</span></span>
<span data-ttu-id="664d5-136">Расширение может содержать защищенные параметрыSettings или protectedSettingsFromKeyVault или не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="664d5-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="664d5-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="664d5-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="664d5-138">Набор имен расширений, после чего их нужно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="664d5-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="664d5-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="664d5-139">-Publisher</span></span>
<span data-ttu-id="664d5-140">Имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="664d5-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="664d5-141">С помощью Get-AzVMImagePublisher можно получить издателя.</span><span class="sxs-lookup"><span data-stu-id="664d5-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="664d5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="664d5-142">-ResourceGroupName</span></span>
<span data-ttu-id="664d5-143">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="664d5-143">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="664d5-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="664d5-144">-Setting</span></span>
<span data-ttu-id="664d5-145">Общедоступные параметры расширения, отформатированные Json.</span><span class="sxs-lookup"><span data-stu-id="664d5-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="664d5-146">-Type</span><span class="sxs-lookup"><span data-stu-id="664d5-146">-Type</span></span>
<span data-ttu-id="664d5-147">Тип расширения. Например: CustomScriptExtension.</span><span class="sxs-lookup"><span data-stu-id="664d5-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="664d5-148">Тип расширения можно Get-AzVMExtensionImageType с помощью Get-AzVMExtensionImageType расширения.</span><span class="sxs-lookup"><span data-stu-id="664d5-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="664d5-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="664d5-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="664d5-150">Определяет версию обработера сценариев.</span><span class="sxs-lookup"><span data-stu-id="664d5-150">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="664d5-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="664d5-151">-Confirm</span></span>
<span data-ttu-id="664d5-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="664d5-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="664d5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="664d5-153">-WhatIf</span></span>
<span data-ttu-id="664d5-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="664d5-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="664d5-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="664d5-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="664d5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664d5-156">CommonParameters</span></span>
<span data-ttu-id="664d5-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="664d5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664d5-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="664d5-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664d5-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="664d5-159">INPUTS</span></span>

### <span data-ttu-id="664d5-160">System.String</span><span class="sxs-lookup"><span data-stu-id="664d5-160">System.String</span></span>

### <span data-ttu-id="664d5-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="664d5-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="664d5-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="664d5-162">OUTPUTS</span></span>

### <span data-ttu-id="664d5-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="664d5-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="664d5-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="664d5-164">NOTES</span></span>

## <span data-ttu-id="664d5-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="664d5-165">RELATED LINKS</span></span>
